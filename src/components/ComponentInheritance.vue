<template>
  <!-- 컴포넌트 속성 상속 -->
  <!-- 최상위 요소에 class상속 - 최상위 요소가 2개 이상일 경우 상속X -->
  <MyBtn
    class="heropy"
    sytle="color: red;"
    title="hello world">
    Inherit
  </MyBtn>
</template>

<script>
import MyBtn from '~/components/MyBtn'
export default {
    components: {
        MyBtn
    },
}
</script>