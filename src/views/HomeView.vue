<template>
  <div class="home">
    <!-- <h1 class="home__header">Home</h1> -->
    <div class="count">{{ count }}</div>
    <div class="btns">
      <button class="btn" @click="decreaseCount">-</button>
      <button class="btn" @click="increaseCount">+</button>
    </div>
    <hr>
    <div>
      This counter is: {{ oddOrEven }}.
    </div>
  </div>
</template>

<script setup>
import { computed, ref } from 'vue';


const count = ref(0)

const increaseCount = () => {
  count.value++
}
const decreaseCount = () => {
  count.value--
}

const oddOrEven = computed(() => {
  if (count.value % 2 === 0) return 'even'
  return 'odd'
})
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
