<template>
  <div class="mood-history">
    <h2>Mood History</h2>
    <p v-if="moodHistory.length === 0">
      No mood history.
    </p>
    <table v-else>
      <thead>
        <tr>
          <th>Date</th>
          <th>Mood</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="mood in moodHistory" :key="mood.id">
          <td>{{ formatDate(mood.date) }}</td>
          <td>{{ mood.mood }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'MoodHistory',
  props: {
    moodHistory: {
      type: Array,
      required: true,
    },
  },
  methods: {
    formatDate(date) {
      const options = {
        year: 'numeric',
        month: 'long',
        day: 'numeric',
      };
      return new Date(date).toLocaleDateString('en-US', options);
    },
  },
};
</script>

<style lang="scss" scoped>
@import '@/scss/styles.scss';
</style>
