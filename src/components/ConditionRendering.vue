<template>
  <!-- 조건부 렌더링 -->
  <button @click="handler">
    click me!
  </button>
  <!-- 초기 렌더링 비용 높, 항상 html에 존재 style display요소로 관리 -->
  <h1 v-show="isShow">
    v-show
  </h1>
  <!-- 전환 비용 높 -->
  <h1 v-if="isShow">
    v-if
  </h1>
  <h1 v-else-if="count > 3">
    Count > 3
  </h1>
  <h1 v-else>
    Good~
  </h1>
  <template v-if="isShow">
    <!-- 클래스 바인딩 -->
    <h1>Title</h1>
    <p>Paragraph 1</p>
    <p>Paragraph 2</p>
  </template>
  <br />
</template>

<script>
export default {
    data() {
        return {
             // 조건부 렌더링
            isShow: true,
            count: 0,
        }
    },
    methods: {
        // 조건부 렌더링
      handler() {
        this.isShow = !this.isShow
        this.count += 1
      },
    }
}
</script>