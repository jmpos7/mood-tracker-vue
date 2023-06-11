<template>
  <div id="app">
    <MoodTracker />
  </div>
</template>

<script>
import MoodTracker from './components/MoodTracker.vue';
export default {
  name: 'App',
  components: {
    MoodTracker,
  },
};
</script>

<style lang="scss" scoped>
@import '@/scss/styles.scss';
</style>

