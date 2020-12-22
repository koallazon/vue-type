<template>
    <v-app>
        <v-main>
            <v-container fluid class="d-flex">
                <v-list class="d-flex">
                    <v-list-item>
                        <router-link to="/">Home</router-link>
                    </v-list-item>
                    <v-list-item>
                        <router-link to="/about">About</router-link>
                    </v-list-item>
                </v-list>
                <v-spacer />
                <v-btn>button</v-btn>
            </v-container>
                <router-view />
        </v-main>
    </v-app>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'
@Component
export default class LayoutNormal extends Vue {
}
</script>

<style scoped>

</style>
