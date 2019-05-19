<template>
  <div class="calculator">
    <form class="d-flex flex-column" @submit.prevent="calculator">
      <label class="d-flex justify-content-between"><span>Total Loan </span><input class="rounded pl-1 mr-3"
          type="number" v-model="amount" placeholder="exe 200000"></label>
      <label class="d-flex justify-content-between"><span>Interest </span><span><input class="rounded pl-1"
            type="number" v-model="interest" placeholder="exe 7.5"> %</span></label>
      <!-- <label>Term <input class="rounded pl-1" type="number" v-model="term" placeholder="years"></label> -->
      <label class="d-flex justify-content-between"><span>Term </span><select class="rounded mr-3" v-model="term">
          <option class="bg-dark text-light" value="15">15</option>
          <option class="bg-dark text-light" value="30">30</option>
        </select></label>
      <button type="submit">Calculate</button>
    </form>
  </div>
</template>


<script>
  import {
    calculate
  } from '../services/mortgage.service.js'
  export default {
    name: 'calculator',
    data() {
      return {
        amount: null,
        interest: null,
        term: null
      }
    },
    computed: {},
    methods: {
      calculator() {


        let result = calculate(this.amount, this.interest, this.term)
        this.$emit('mortgageValues', result)
        this.clearForm()
      },
      clearForm() {
        this.amount = null
        this.interest = null
        this.term = null
      }

    },
    components: {}
  }
</script>


<style scoped>

</style>