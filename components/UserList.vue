<template>
    <v-app-bar extended>

        <v-app-bar-title>ユーザー一覧</v-app-bar-title>

        <v-spacer></v-spacer>

        <v-btn icon="mdi-dots-vertical">
        </v-btn>
    </v-app-bar>

    <v-main>
        <v-container>
            <v-row>
                <v-col v-for="n in   24  " :key="n" cols="4">
                    <NuxtLink v-bind:to="{ name: 'chat-id', params: { id: n } }">
                        <v-avatar color="grey lighten-2" size="128"></v-avatar>
                    </NuxtLink>
                </v-col>
            </v-row>
        </v-container>
    </v-main>
</template>