<template>
    <v-app>
        <v-main>
            <v-container class="justify-center align-center fill-height">
                <v-text-field outlined placeholder="login"></v-text-field>
                <v-btn @click="test">test</v-btn>
            </v-container>
        </v-main>
    </v-app>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'
@Component
export default class LayoutAuth extends Vue {
  async test () {
    const ref = this.$firebase.firestore().collection('video').doc('001')
    await ref.set({ a: 1111 })
    const doc = await ref.get()
    console.log(doc.data())
  }
}
</script>

<style scoped>

</style>
