<template lang="pug">
#app
  Footer
  Pagination
</template>

<script lang="ts">
import Vue from 'vue'
import Footer from '@/components/Footer.vue'
import Pagination from '@/components/Pagination.vue'
import Component from 'vue-class-component'

@Component({ components: { Footer, Pagination } })
export default class App extends Vue {}
</script>

<style>
html {
  background-color: black !important;
}
</style>
