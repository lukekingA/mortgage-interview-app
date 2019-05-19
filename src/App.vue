<template>
  <div id="app" class="container-fluid">
    <div class="banner">
      <img src="@/assets/logo.png" width="25px" class="logo">
      <h3>Vue Mortgage Calculator</h3>
    </div>
    <div class="row">
      <div class="col-6 offset-3">

        <!-- Your calculator component(s) should go here -->

        <calculator v-on:mortgageValues="calculateMortgage"></calculator>
        <div class="text-left font-weight-bold">
          <p class="ml-0">
            Balance: ${{balance}}
          </p>
          <p class="ml-0">
            Payment: ${{payment}}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import calc from './services/mortgage.service.js'
  import Calculator from '@/components/Calculator.vue'
  export default {
    name: "app",
    data() {
      return {
        balance: 0,
        payment: 0
      }
    },
    methods: {
      calculateMortgage(values) {
        this.balance = values.balance
        this.payment = values.pmt
      }
    },
    components: {
      Calculator
    }
  };
</script>

<style>
  #app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    font-weight: 100;
    font-size: 14px;
  }

  body {
    margin: 0;
  }

  h3 {
    display: inline-block;
    text-align: center;
  }

  .banner {
    background-color: lightgray;
    text-align: center;
    margin-bottom: 25px;
  }

  .logo {
    display: inline-block;
    margin-bottom: -8px;
    margin-right: 5px;
  }

  p {
    width: 75%;
    margin: 0 auto;
    padding: 10px;
  }
</style>