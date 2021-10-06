<template>
  <!-- 컴포넌트 기초 -->
  <MyBtn /><MyBtn color="royalblue" /><MyBtn
    large
    color="greenYellow" /><MyBtn />
  <br />
  <MyBtn text="Banana" /><MyBtn :color="btnColor" /><MyBtn /><MyBtn />
  <br />
  <MyBtn>Banana</MyBtn><MyBtn><span style="color: red">Banana</span></MyBtn>
</template>

<script>
import MyBtn from '~/components/MyBtn'

export default {
    components: {
        MyBtn
    },
    data() {
        return {
          btnColor: '#000'
        }
    },
}
</script>