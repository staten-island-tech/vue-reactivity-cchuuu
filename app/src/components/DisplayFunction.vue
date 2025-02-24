<template>
  <div
    class="card w-1/6 h-[17vw] bg-gray-400 rounded-3xl flex flex-col items-center justify-evenly m-6 border-2 border-black"
  >
    <h2 class="text-center font-bold text-2xl">{{ item.name }}</h2>
    <img
      :src="item.image"
      :alt="item.type"
      class="object-cover w-[90%] h-[55%] rounded-lg shadow-md border-black border-2"
    />
    <h3 class="text-center text-xl">${{ item.price }}</h3>
    <button
      @click="addItem(item)"
      class="bg-blue-100 rounded-lg w-[6vw] h-[2vw] border-black border-2 text-black"
    >
      Add to Cart!
    </button>
  </div>
</template>

<script setup>
import { cartItems } from '@/array/store'
defineProps({
  item: Object,
})

function addItem(item) {
  const itemInCart = cartItems.cart.find((itemInCart) => itemInCart.name === item.name)
  if (itemInCart) {
    itemInCart.quantity++
  } else {
    cartItems.cart.push(item)
  }
}
</script>

<style scoped></style>
