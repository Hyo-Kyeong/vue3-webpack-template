<template>
  <RefsHello ref="refshello" />
  <h1
    id="hello"
    ref="hello">
    REFS!
  </h1>
</template>

<script>
import RefsHello from '~/components/RefsHello'
export default {
  components: {
    RefsHello
  },
  // html이 mount되어야 사용가능하므로 created에서는 undefined
  created() {
    console.log('created', this.$refs.hello)
  },
  mounted() {
      const h1El = document.querySelector('#hello')
      console.log('h1El text', h1El.textContent)
      console.log('refs text', this.$refs.hello.textContent)
      console.log('refs el', this.$refs.refshello.$el)
      console.log('refs refs', this.$refs.refshello.$refs.good)
  },
}
</script>