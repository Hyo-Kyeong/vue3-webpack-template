<template>
  <!-- 이벤트 수식어 -->
  <a
    href="https://naver.com"
    target="_blank"
    @click="preventHandler">
    NAVER
  </a>
  <!-- html 기능 사용 X -->
  <a
    href="https://naver.com"
    target="_blank"
    @click.prevent="preventHandler">
    NAVER_prevent
  </a>
  <!-- 핸들러 한 번만 실행 -->
  <a
    href="https://naver.com"
    target="_blank"
    @click.once="handlerA">
    NAVER_once
  </a>
  <a
    href="https://naver.com"
    target="_blank"
    @click.prevent.once="handlerA">
    NAVER_prevent_once
  </a>
  <!-- 이벤트 버블링: 자식->부모 순으로 둘 다 실행됨 -->
  <div
    class="parent"
    @click="handlerA">
    <div
      class="child"
      @click="handlerB">
    </div>
    <div
      class="child"
      @click.stop="handlerB">
    </div>
  </div>
  <!-- 이벤트 캡쳐링: 부모->자식 순으로 둘 다 실행됨 -->
  <div
    class="parent"
    @click.capture.stop="handlerA">
    <div
      class="child"
      @click="handlerB">
    </div>
    <div
      class="child"
      @click.stop="handlerB">
    </div>
  </div>
  <!-- self: 정확히 해당 영역만 클릭했을 때 handler발생 -->
  <div
    class="parent"
    @click.self="handlerA">
    <div
      class="child">
    </div>
  </div>
  <!-- passive: handler로직과 wheel동작을 독립적으로 시행 -->
  <div
    class="p"
    @wheel.passive="eventHandler('wheel', event)">
    <div
      class="c">
    </div>
  </div>
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
      handlerB(event) {
        // 이벤트 버블링 방지
        event.stopPropagation()
        console.log('B')
      },
      // 이벤트 수식어
      preventHandler(event) {
        event.preventDefault()
        console.log('ABC!')
      },
    },
}
</script>

<style scoped lang="scss">
  .parent {
    width: 200px;
    height: 200px;
    background-color: royalblue;
    margin: 10px;
    padding: 10px;
    .child {
      width: 100px;
      height: 100px;
      background-color: orange;
    }
  }
  .p {
    width: 200px;
    height: 100px;
    background-color: red;
    margin: 10px;
    padding: 10px;
    overflow: auto;
    .c {
      width: 100px;
      height: 2000px;
      background-color: greenyellow;
    }
  }
</style>