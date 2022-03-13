<template>
  <div
    class="detail"
    :style="{
      background:
        'linear-gradient(rgba(0, 0, 0, 0.45), rgba(0, 0, 0, 0.45)), url(\'/images/' +
        resort.image +
        '\')',
    }"
  >
    <h1>Details for {{ resort.name }} Resort</h1>
    <p>Adult Ticket Price: {{ resort.ticketPrice }}</p>
    <p>{{ resort.lifts }} lifts</p>
    <p>Open at night: {{ resort.night }}</p>
  </div>
</template>

<script>
export default {
  name: "DetailView",
  props: ["resortId"],
  computed: {
    resort() {
      return this.$root.$data.resorts[this.resortId - 1];
    },
  },
};
</script>

<style scoped>
.detail {
  border-radius: 1em;
  color: white;
  padding: 1em 2em;
  margin: 3em 0;
  font-family: "Times New Roman", Times, serif;
}
</style>
