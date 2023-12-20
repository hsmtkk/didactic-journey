<template>
    <v-main>
        <p>Your ID is {{ id }}</p>

        <v-container class="py-8 px-6" fluid>
            <v-row>
                <v-col v-for="card in cards" :key="card" cols="12">
                    <v-card>
                        <v-list lines="two">
                            <v-list-subheader :title="card"></v-list-subheader>

                            <template v-for="n in 6" :key="n">
                                <v-list-item>
                                    <template v-slot:prepend>
                                        <v-avatar color="grey-darken-1"></v-avatar>
                                    </template>

                                    <v-list-item-subtitle>blah blah blah</v-list-item-subtitle>
                                </v-list-item>

                                <v-divider v-if="n !== 6" :key="`divider-${n}`" inset></v-divider>
                            </template>
                        </v-list>
                    </v-card>
                </v-col>
            </v-row>
        </v-container>

        <v-textarea append-inner-icon="mdi-comment" class="mx-2" label="メッセージを送信する" rows="3" auto-grow>
        </v-textarea>
    </v-main>
</template>

<script setup lang="ts">
const route = useRoute()

const id = route.params.id

const cards = ["Today"]
</script>