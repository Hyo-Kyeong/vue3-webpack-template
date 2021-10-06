<template>
  <!-- 이벤트 핸들링 -->
  <button @click="eventHandler('hi', $event)">
    Click me 1
  </button>
  <button @click="eventHandler('what', $event)">
    Click me 2
  </button>
  <button @click="handlerA(), handlerB()">
    Click me!
  </button>
</template>

<script>
export default {

    methods: {
        // 이벤트 핸들링
      eventHandler(msg, event) {
        console.log(msg)
        console.log(event)
      },
      handlerA() {
        console.log('A')
      },
      handlerB() {
        console.log('B')
      },
    }
}
</script>