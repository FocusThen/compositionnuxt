<template>
  <main class="container">
    <ul>
      <li @click="alertUnit" v-for="(item, index) in theList" :key="index">
        {{ item }}
      </li>
    </ul>
  </main>
</template>

<script lang="ts">
import { defineComponent, ref } from '@vue/composition-api'

export default defineComponent({
  setup() {
    const theList = ['test1', 'test2', 'test3']

    const alertUnit = (e: any) => {
      alert(e.target.textContent)
    }

    return { theList, alertUnit }
  },
})
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
li {
  font-size: 50px;
}
</style>
