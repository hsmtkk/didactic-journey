<template>
    <v-navigation-drawer v-model="drawer">
        <v-sheet color="grey-lighten-4" class="pa-4">
            <v-avatar class="mb-4" color="grey-darken-1" size="64"></v-avatar>

            <div>john@google.com</div>
        </v-sheet>

        <v-divider></v-divider>

        <v-list>
            <v-list-item v-for="[icon, text, path] in links" :key="icon" :prepend-icon="icon" :title="text" :to="path"
                link></v-list-item>
        </v-list>
    </v-navigation-drawer>
</template>

<script setup lang="ts">
const drawer = ref(null)
const links = [
    ['mdi-inbox-arrow-down', 'Inbox', "/"],
    ['mdi-send', 'Send', "/about"],
    ['mdi-delete', 'Trash', "/about"],
    ['mdi-alert-octagon', 'Spam', "about"],
]
</script>