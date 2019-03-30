<template>
  <p>
    <!--you can pass in a smaller width and height as props-->
    <app-icon-base width="12" height="12" icon-name="write">
      <app-icon-write/>
    </app-icon-base>
    <!--or you can use the default, which is 18-->
    <app-icon-base icon-name="write">
      <app-icon-write/>
    </app-icon-base>
    <!--or make it a little bigger too :) -->
    <app-icon-base width="30" height="30" icon-name="write">
      <app-icon-write/>
    </app-icon-base>
    <br>You can make inline icons of any size by passing props.
  </p>
</template>

<script>
import AppIconBase from "./AppIconBase.vue";
import AppIconWrite from "./AppIconWrite.vue";

export default {
  components: {
    AppIconBase,
    AppIconWrite
  }
};
</script>

<style scoped>
</style>