<template>
    금액 : <input type="text" v-model.number="amount"/>
    <br>
    <br>
    <button @click="deposit">입금</button>
    <button @click="withdraw">출금</button>
    <br>
    <h4>계좌 잔액 : {{ balance }}</h4>
</template>
<script>
export default {
  data() {
    return {
       balance : 500000,
       amount : 0
    }
  },
  methods : {
    deposit(){
        this.balance += this.amount
    },
    withdraw(){
        if(this.balance - this.amount >= 0){
            this.balance -= this.amount
        }
    }
  }
}
</script>
<style>

</style>