<template>
  <!-- 반응성 X -->
  <button @click="message = 'Good?'">
    Click!
  </button>
  <h1>ComponentProvide: {{ message }}</h1>
  <Parent />
</template>

<script>
import Parent from '~/components/Parent'
import { computed } from 'vue'
export default {
    components: {
        Parent
    },
    data() {
        return {
            message: 'Component Provide-Inject'
        }
    },
    provide() {
        return {
            msg: computed(() => {
                return this.message
            })
        }
    }
}
</script>