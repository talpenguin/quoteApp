<template>
  <div>
    <div class="col-sm-12 text-center">
      <h2>Quote App</h2>
      <div class="progress">
        <div
          class="progress-bar"
          :style="{ width: quotes.length * 10 + '%' }"
          :aria-valuenow="quotes.length"
          :aria-valuemax="maxQuotes"
        >
          {{ quotes.length }} / {{ maxQuotes }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProgressBar",
  props: {
    quotes: { type: Array },
    maxQuotes: { type: Number }
  }
};
</script>
