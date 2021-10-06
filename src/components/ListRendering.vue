<template>
  <!-- 리스트 렌더링 -->
  <button @click="listHandler">
    button
  </button>
  <ul>
    <li
      v-for="(f, i) in fruits"
      :key="f">
      {{ f }}-{{ i+1 }}
    </li>
  </ul>
  <ul>
    <li
      v-for="{id, name} in newFruits"
      :key="id">
      {{ name }}-{{ id }}
    </li>
  </ul>
</template>

<script>
import shortid from 'shortid'

export default {
    data() {
        return {
            // 리스트 렌더링
            fruits: [ 'Apple', 'Banana', 'Cherry'],
        }
    },
    methods: {
    // 리스트 렌더링
      listHandler() {
        this.fruits.push('Orange')
      },
    },
    computed: {
      newFruits() {
        return this.fruits.map(fruit => ({
          id: shortid.generate(),
          name: fruit
        }))
      }
    },
}
</script>