<template>
  <!-- 폼 입력 바인딩 -->
  <p>즉각 반응</p>
  <h1>{{ msg }}</h1>
  <input
    type="text"
    :value="msg" 
    @input="inputHandler" />
  <input
    type="text"
    :value="msg" 
    @input="msg = $event.target.value" />
  <input
    type="text"
    v-model="msg" />
  <h1>{{ checked }}</h1>
  <input
    type="checkbox"
    v-model="checked" />
  <p>tap또는 enter입력시 변화</p>
  <input
    type="text"
    :value="msg"
    @change="msg = $event.target.value" />
  <input
    type="text"
    v-model.lazy="msg" />
  <p>타입 지정</p>
  <input
    type="text"
    v-model.number="msg" />
  <input
    type="text"
    v-model.trim="msg" />
</template>

<script>
export default {
    data() {
        return {
            msg: 123,
            checked: false,
        }
    },
    methods: {
        inputHandler(event) {
        console.log(event.target.value)
        this.msg = event.target.value
      }
    },
    watch: {
      msg() {
        console.log(typeof this.msg)
      }
    }
}
</script>