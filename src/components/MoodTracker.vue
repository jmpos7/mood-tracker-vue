<template>
    <h1>Mood Tracker</h1>
    <div class="mood-tracker">
      <MoodEntryForm @add-mood-entry="handleAddMoodEntry" />
      <MoodHistory :moodHistory="moodHistory" />
    </div>
</template>
  
<script>
import MoodEntryForm from '@/components/MoodEntryForm.vue';
import MoodHistory from '@/components/MoodHistory.vue';

export default {
  name: 'MoodTracker',
  components: {
    MoodEntryForm,
    MoodHistory,
  },
  data() {
    return {
      moodHistory: [],
    };
  },
  methods: {
    handleAddMoodEntry(newMoodEntry) {
      this.moodHistory.push(newMoodEntry);
    },
  },
};
</script>

  
<style lang="scss" scoped>
@import '@/scss/styles.scss';
</style>