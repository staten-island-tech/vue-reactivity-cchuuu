<template>
  <div>
    <div
      class="shoppingcart fixed top-0 right-0 w-72 h-full bg-gray-100 shadow-lg p-5 overflow-y-auto"
    >
      <h1 class="text-center text-xl font-bold">Shopping Cart</h1>
      <div class="mt-4 font-semibold">Total: ${{ totalPrice() }}</div>
      <li v-for="item in cartItems.cart" :key="item.id" :item="item" class="flex justify-between">
        <h3>x{{ item.quantity }} {{ item.name }}</h3>
        <h3>${{ price(item) }}</h3>
      </li>
      <button
        @click="clearCart(cart)"
        class="rounded-lg w-[5vw] h-[1.5vw] border-black border-2 text-black m-1"
      >
        Clear Cart
      </button>
    </div>
  </div>
</template>

<script setup>
import { cartItems } from '@/array/store'
defineProps({
  cartItems: Array,
})
function totalPrice() {
  let total = 0
  cartItems.cart.forEach((item) => {
    return (total += item.price * item.quantity)
  })

  return Math.round(total * 100) / 100
}

function price(item) {
  return Math.round(item.price * item.quantity * 100) / 100
}

function clearCart() {
  cartItems.cart.forEach((items) => (items.quantity = 1))
  cartItems.cart = []
}
</script>

<style scoped></style>
