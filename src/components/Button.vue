<template lang="html">
    <button @click="btnClick(1)">按钮</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Button',
  props: {
    btnType: {
      required: true,
      type: String,
    },
  },
  setup(props) {
    console.log('props');

    const btnClick = (num: number, e: Event) => {
      // console.log(this); // 这个this、、、
      console.log(arguments);
      console.log(num);
      console.log(e);
    };
    return {
      btnClick,
    };
  },
});
</script>

<style lang="scss">
</style>