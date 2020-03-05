<template>
  <div class="container">
      <app-new-quote @quoteAdded="newQuote"></app-new-quote>
      <app-quote-grid :quotes="quotes"></app-quote-grid>
  </div>
</template>

<script>
  import QuoteGrid from "./components/QuoteGrid";
  import NewQuote from "./components/NewQuote";

  export default {
      name: 'App',
      components: {
          appQuoteGrid: QuoteGrid,
          appNewQuote: NewQuote
      },
      data() {
          return {
              quotes: [
                  'Just a Quote to see something'
              ],
              maxQuotes: 10,

          }
      },
      methods: {
          newQuote(quote) {
              this.quotes.unshift(quote);
          }
      }

  }
</script>

<style>
    .container {
        margin-top: 15px;
    }
</style>
