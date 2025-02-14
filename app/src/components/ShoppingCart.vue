<template>
  <div>
    <div
      class="shoppingcart fixed top-0 right-0 w-72 h-full bg-gray-100 shadow-lg p-5 overflow-y-auto"
    >
      <h1 class="text-center text-xl font-bold">Shopping Cart</h1>
      <div class="mt-4 font-semibold">Total: ${{ totalPrice() }}</div>
      <ul>
        <li v-for="item in cartItems.cart" :key="item.id" :item="item" class="flex justify-between">
          <h3>{{ item.name }} Quantity: {{ item.quantity }}</h3>
          <h3>${{ price(item) }}</h3>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { cartItems } from '@/array/store'
defineProps({
  cartItems: Array,
})
function totalPrice() {
  const total = cartItems.cart.reduce((total, item) => {
    return total + item.price * item.quantity
  }, 0)

  return Math.round(total * 100) / 100
}

function price(item) {
  return Math.round(item.price * item.quantity * 100) / 100
}
</script>

<style scoped></style>
