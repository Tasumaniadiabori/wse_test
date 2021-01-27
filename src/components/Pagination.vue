<template lang="pug">
.pagination-background
  .pagination-container
    button.number(
      v-for='(n, i) in 10',
      @click='activePage = n',
      :class='activePage === n ? "active" : "inactive"',
      v-if='currentPages(n)'
    ) {{ n }}
    span.number.hidden(v-if='activePage < 8') ...
    button.number(
      @click='activePage = 11',
      :class='activePage === 11 ? "active" : "inactive"'
    ) 11
</template>

<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'

@Component
export default class Pagination extends Vue {
  activePage = 1
  currentPages(n: number) {
    return (
      (this.activePage <= 2 && n <= 4) ||
      (this.activePage >= 8 && n >= 6) ||
      (this.activePage - n > -3 && this.activePage - n < 2)
    )
  }
}
</script>
<style>
.pagination-background {
  width: 300px;
  height: 40px;
  background: #fefeff;
  border: 1px solid rgba(196, 196, 205, 0.4);
  box-sizing: border-box;
  border-radius: 8px;
}
.pagination-container {
  display: flex;
  flex: 1;
  flex-direction: row;
  max-width: 100%;
  align-items: center;
  justify-content: space-between;
  padding: 3px 4px 0px 4px;
}
.active {
  width: 38px;
  height: 32px;
  background: #ffc5e4;
  border-radius: 5px;
}
.inactive {
  width: 41px;
  height: 32px;
  box-sizing: border-box;
  border-radius: 5px;
}
.inactive:hover {
  border: 1px solid #ff93cd;
}
.number {
  font-family: Manrope;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 20px;
  color: #222226;
}
.hidden {
  display: flex;
  width: 41px;
  height: 32px;
  justify-content: center;
  align-items: center;
}
</style>
