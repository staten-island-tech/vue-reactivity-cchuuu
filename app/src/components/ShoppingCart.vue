<template>
  <div>
    <div
      class="shoppingcart fixed top-0 right-0 w-72 h-full bg-gray-100 shadow-lg p-5 overflow-y-auto"
    >
      <h1 class="text-center text-xl font-bold">Shopping Cart</h1>
      <ul>
        <li v-for="item in cartItems" :key="item.id" class="flex justify-between">
          <h3>{{ item.name }} ({{ item.quantity }})</h3>
          <h3>\${{ item.price * item.quantity }}</h3>
          <button @click="removeItem(item.id)" class="text-red-500">Remove</button>
        </li>
      </ul>
      <div class="mt-4 font-semibold">Total: \${{ totalPrice }}</div>
    </div>
  </div>
</template>

<script setup>
import { reactive } from 'vue'
const cartItems = reactive([])
defineProps({
  cartItems: Array,
})

function removeItem() {
  const item = props.cartItems.find(item => item.id === id)
  if (item){
    if (item.quantity)
  }
  }
}
</script>

<style scoped></style>
