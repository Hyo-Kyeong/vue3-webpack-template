<template>
  <MyBtnEmit
    @click="log"
    @change-msg="logMsg">
    Emit
  </MyBtnEmit>
  <br /><br />
  <h1>heroypy</h1>
  <MyBtnEmit @heropy="log">
    Emit
  </MyBtnEmit>
</template>

<script>
import MyBtnEmit from '~/components/MyBtnEmit'
export default {
    components: {
        MyBtnEmit
    },
    methods: {
        log() {
            console.log('Click!!')
        },
        logEvent(event) {
            console.log('click!')
            console.log(event)
        },
        logMsg(msg) {
            console.log(msg)
        }
    }
}
</script>