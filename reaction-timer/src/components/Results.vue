<template>
  <p>Reaction time: - {{ sc }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['sc'],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.sc < 250) {
      this.rank = 'Ninja Fingers';
    } else if (this.sc < 400) {
      this.rank = 'Rapid Reflexes';
    } else {
      this.rank = 'sanil pace...';
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>
