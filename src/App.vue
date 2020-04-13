<template>
  <div class="container">
    <progress-bar :quotes="quotes" :maxQuotes="maxQuotes" />
    <new-quote @addQuote="addNewQuote" />
    <quote-grid :quotes="quotes" />
    <div class="row">
        <div class="col-sm-4 col-sm-offset-4 text-center">
            <div class="alert alert-info"> INFO: Click on a quote to delete it </div>
        </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
import ProgressBar from "./components/ProgressBar.vue";

export default {
  components: { QuoteGrid, NewQuote, ProgressBar },
  data() {
    return {
      maxQuotes: 12,
      quotes: []
    };
  },
  methods: {
    addNewQuote(quote) {
      this.quotes.length < this.maxQuotes ? this.quotes.unshift(quote) : null;
    }
  }
};
</script>
