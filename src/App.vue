<template>
  <div class="container">
      <app-quote-grid :quotes="quotes"></app-quote-grid>
  </div>
</template>

<script>
  import QuoteGrid from "./components/QuoteGrid";
  export default {
    name: 'App',
    components: {
      appQuoteGrid: QuoteGrid
    },
    data() {
      return {
        quotes: [
          'Just a Quote to see something'
        ],
        maxQuotes: 10,

      }
    }

  }
</script>

<style>

</style>
