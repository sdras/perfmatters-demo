<template>
  <div>
    <button @click="$emit('changeShowing')">
      <span v-if="isShowing">Estelle doesn't love you :(</span>
      <span v-else>Estelle loves you!</span>
    </button>
    <input v-model="hairColor" type="color" id="hair" name="hair">
    <label for="hair">Hair</label>
  </div>
</template>

<script>
export default {
  props: {
    isShowing: {
      type: Boolean,
      default: false
    }
  }
};
</script>

<style scoped>
</style>