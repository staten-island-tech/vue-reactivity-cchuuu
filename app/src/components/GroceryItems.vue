<template>
  <div>
    <div class="container flex flex-wrap items-center justify-around mt-5">
      <DisplayFunction v-for="item in GroceryItems" :key="item.name" :item="item" />
    </div>
  </div>
</template>

<script setup>
import DisplayFunction from './DisplayFunction.vue'

const GroceryItems = [
  {
    name: 'Apple',
    price: 1.59,
    type: 'Fruit',
    image: 'images/apple.jfif',
    quantity: 1,
  },
  {
    name: 'Banana',
    price: 1.29,
    type: 'Fruit',
    image: 'images/banana.jfif',
    quantity: 1,
  },
  {
    name: 'Kiwi',
    price: 2.39,
    type: 'Fruit',
    image: 'images/kiwi.jfif',
    quantity: 1,
  },
  {
    name: 'Orange',
    price: 1.99,
    type: 'Fruit',
    image: 'images/orange.webp',
    quantity: 1,
  },
  {
    name: 'Broccoli',
    price: 2.19,
    type: 'Vegetable',
    image: 'images/broccoli.jpg',
    quantity: 1,
  },
  {
    name: 'Beef',
    price: 4.59,
    type: 'Meat',
    image: 'images/beef.jfif',
    quantity: 1,
  },
  {
    name: 'Chicken Breast',
    price: 3.89,
    type: 'Meat',
    image: 'images/chickenbreast.jfif',
    quantity: 1,
  },
  {
    name: 'Milk',
    price: 1.69,
    type: 'Dairy',
    image: 'images/milk.jfif',
    quantity: 1,
  },
  {
    name: 'Oat',
    price: 1.59,
    type: 'Grain',
    image: 'images/oat.jfif',
    quantity: 1,
  },
  {
    name: 'Yogurt',
    price: 2.49,
    type: 'Dairy',
    image: 'images/yogurt.jfif',
    quantity: 1,
  },
  {
    name: 'Cheese',
    price: 3.19,
    type: 'Dairy',
    image: 'images/cheese.jpg',
    quantity: 1,
  },
  {
    name: 'Avocado',
    price: 2.89,
    type: 'Fruit',
    image: 'images/avocado.jfif',
    quantity: 1,
  },
  {
    name: 'Lime',
    price: 1.39,
    type: 'Fruit',
    image: 'images/lime.jfif',
    quantity: 1,
  },
  {
    name: 'Peas',
    price: 1.99,
    type: 'Vegetable',
    image: 'images/peas.jfif',
    quantity: 1,
  },
  {
    name: 'Strawberry',
    price: 3.69,
    type: 'Fruit',
    image: 'images/strawberry.jfif',
    quantity: 1,
  },
  {
    name: 'Duck',
    price: 4.79,
    type: 'Meat',
    image: 'images/duck.jpg',
    quantity: 1,
  },
  {
    name: 'Lamb',
    price: 4.29,
    type: 'Meat',
    image: 'images/lamb.jfif',
    quantity: 1,
  },
  {
    name: 'Pork',
    price: 3.59,
    type: 'Meat',
    image: 'images/pork.jfif',
    quantity: 1,
  },
  {
    name: 'Mutton',
    price: 3.99,
    type: 'Meat',
    image: 'images/mutton.jfif',
    quantity: 1,
  },
  {
    name: 'Spam',
    price: 2.79,
    type: 'Meat',
    image: 'images/spam.jfif',
    quantity: 1,
  },
]
</script>

<style scoped></style>
