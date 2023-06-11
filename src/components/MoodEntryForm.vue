<template>
    <div class="mood-entry-form">
      <h2>How are you feeling today?</h2>
      <h4>Select your mood and click 'Submit'</h4>
  
      <div class="mood-options">
        <button
          v-for="moodOption in moodOptions"
          :key="moodOption.id"
          :class="{ 'selected': selectedMood === moodOption.value }"
          @click="selectMood(moodOption.value)"
        >
          {{ moodOption.label }}
        </button>
      </div>
  
      <button 
        class="submit-button"
        @click="submitForm">Submit</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'MoodEntryForm',
    data() {
      return {
        selectedMood: '', // Stores selected mood
        moodOptions: [
          { id: 1, label: 'Happy', value: 'happy' },
          { id: 2, label: 'Excited', value: 'excited' },
          { id: 3, label: 'Proud', value: 'proud' },
          { id: 4, label: 'Sad', value: 'sad' },
          { id: 5, label: 'Afraid', value: 'afraid' },
          { id: 6, label: 'Embarassed', value: 'embarassed' },
          { id: 7, label: 'Anxious', value: 'anxious' },
          { id: 8, label: 'Angry', value: 'angry' },
          { id: 9, label: 'Bored', value: 'bored' },
        ],
      };
    },
    methods: {
      selectMood(mood) {
        this.selectedMood = mood;
      },
      submitForm() {
        if (this.selectedMood) {
          const newMoodEntry = {
            id: Date.now(), // ID for the mood entry
            date: new Date().toISOString().split('T')[0], // Get current date
            mood: this.selectedMood,
          };
          
          // Add the new mood entry to the mood history array
          this.$emit('add-mood-entry', newMoodEntry);

          // Reset the selected mood
          this.selectedMood = '';
        }
      },
  },
};
</script>
  
<style lang="scss" scoped>
  @import '@/scss/styles.scss';
</style>