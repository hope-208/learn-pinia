<template>
  <div class="home">
    <!-- <h1 class="home__header">Home</h1> -->
    <div class="count">{{ storeCounter.count }}</div>
    <div class="btns">
      <button class="btn" @click="storeCounter.decreaseCount">-</button>
      <button class="btn" @click="storeCounter.increaseCount">+</button>
    </div>
    <hr>
    <div>
      This counter is: {{ storeCounter.oddOrEven }}.
    </div>
  </div>
</template>

<script setup>
import { useCounterStore } from '@/stores/counter'

const storeCounter = useCounterStore()

</script>

<style>
.count {
  font-size: 60px;
  margin: 20px;
}

.btns .btn {
  font-size: 40px;
  margin: 10px;
}
</style>
