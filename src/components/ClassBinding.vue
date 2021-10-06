<template>
  <!-- 클래스-바인딩 -->
  <h1
    :class="{ active: isActive }"
    @click="activate">
    Hello?!{{ isActive }}
  </h1>
  <h1
    :style="{color: color, fontSize: fontSize}"
    @click="changeStyle">
    Hello?!
  </h1>
  <h1
    :style="[fontStyle, backgroundStyle]"
    @click="changeStyle2">
    Hello?!
  </h1>
  <br />
</template>

<script>
export default {
    data() {
         return {
          // 클래스-바인딩
            isActive: false,
            color: 'orange',
            fontSize: '30px',
            fontStyle: {
              color: 'orange',
              fontSize: '30px'
            },
            backgroundStyle: {
              backgroundColor: 'black'
            },
         }
    },
    methods: {
        // 클래스-바인딩
      activate() {
        this.isActive = true
      },
      changeStyle() {
        this.color = 'red'
        this.fontSize = '50px'
      },
      changeStyle2() {
        this.fontStyle.color = 'red'
        this.fontStyle.fontSize = '50px'
      },
    }
}
</script>

<style lang="scss" scoped>
    .active {
        color: red;
        font-weight: bold;
    }
</style>