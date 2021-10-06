<template>
  <div
    :class="{ large }"
    :style="{ backgroundColor: color }"
    class="btn">
    <slot></slot>
  </div>
  <h1
    :class="$attrs.class"
    :style="$attrs.style">
    h1 attrs
  </h1>
  <h1 v-bind="$attrs">
    h1 bind
  </h1>
  <h1 @click="$emit('click')">
    Emit click
  </h1>
  <h1 @click="$emit('heropy')">
    Emit heropy
  </h1>
  <h1 @dblclick="$emit('heropy', $event)">
    double Emit heropy
  </h1>
  <input
    type="text"
    v-model="msg" />
</template>

<script>
export default {
    props: {
        color: {
            type: String,
            default: 'gray'
        },
        large: {
            type: Boolean,
            default: false
        },
        text: {
            type: String,
            default: 'Apple'
        }
    },
    data() {
        return {
            msg: ''
        }
    },
    //inheritAttrs: false,
    created() {
        console.log(this.$attrs)
    },
    emits: [
        'click',
        'heropy'
    ],
    watch: {
        msg() {
            this.$emt('changeMsg', this.msg)
        }
    }
}
</script>
<style scoped lang="scss">
    .btn {
        display: inline-block;
        margin: 4px;
        padding: 6px 12px;
        border-radius: 4px;
        background-color: gray;
        color: white;
        cursor: pointer;
        &.large {
            font-size: 20px;
            padding: 10px 20px;
        }
    }
</style>