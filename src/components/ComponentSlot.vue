<template>
  <MyBtnSlot>Slot</MyBtnSlot>
  <MyBtnSlot />
  <MyBtnSlot>
    <template
      #icon>
      <span>(B)</span>
    </template>
    <template
      #text>
      <span>Banana</span>
    </template>
  </MyBtnSlot>
</template>

<script>
import MyBtnSlot from '~/components/MyBtnSlot'
export default {
    components: {
        MyBtnSlot
    }
}
</script>