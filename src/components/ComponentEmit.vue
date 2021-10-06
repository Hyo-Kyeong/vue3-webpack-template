<template>
  <MyBtn
    @click="log"
    @change-msg="logMsg">
    Emit
  </MyBtn>
  <MyBtn @heropy="log">
    Emit
  </MyBtn>
</template>

<script>
import MyBtn from '~/components/MyBtn'
export default {
    components: {
        MyBtn
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