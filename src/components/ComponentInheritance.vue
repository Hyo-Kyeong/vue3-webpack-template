<template>
  <!-- 컴포넌트 속성 상속 -->
  <!-- 최상위 요소에 class상속 - 최상위 요소가 2개 이상일 경우 상속X -->
  <MyBtnInherit
    class="heropy"
    sytle="color: red;"
    title="hello world">
    Inherit
  </MyBtnInherit>
</template>

<script>
import MyBtnInherit from '~/components/MyBtnInherit'
export default {
    components: {
        MyBtnInherit
    },
}
</script>