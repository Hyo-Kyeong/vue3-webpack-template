<template>
  <!-- 키 수식어 -->
  <input
    type="text"
    @keydown="keyHandler" />
  <input
    type="text"
    @keydown.ctrl.shift.a="keyHandler" />
</template>

<script>
export default {
    data() {
        
    },
    methods: {
        // 키 수식어
      keyHandler(event) {
        console.log(event)
        if(event.key === 'Enter') {
          console.log('Enter!!')
        }
      },
    }
}
</script>