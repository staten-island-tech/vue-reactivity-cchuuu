<template>
  <div>
    <div class="container fixed flex flex-wrap items-center justify-around w-full h-full mt-5">
      <DisplayFunction v-for="item in GroceryItems" :key="item.name" :item="item" />
    </div>
  </div>
</template>

<script setup>
import DisplayFunction from './DisplayFunction.vue'

const GroceryItems = [
  {
    name: 'Apple',
    price: '$1.50',
    type: 'Fruit',
    image: 'images/apple.jfif',
    quantity: 1,
  },
  {
    name: 'Banana',
    price: '$1.20',
    type: 'Fruit',
    image: 'images/banana.jfif',
    quantity: 1,
  },
  {
    name: 'Kiwi',
    price: '$2.30',
    type: 'Fruit',
    image: 'images/kiwi.jfif',
    quantity: 1,
  },
  {
    name: 'Orange',
    price: '$1.90',
    type: 'Fruit',
    image: 'images/orange.webp',
    quantity: 1,
  },
  {
    name: 'Broccoli',
    price: '$2.10',
    type: 'Vegetable',
    image: 'images/broccoli.jpg',
    quantity: 1,
  },
  {
    name: 'Beef',
    price: '$4.50',
    type: 'Meat',
    image: 'images/beef.jfif',
    quantity: 1,
  },
  {
    name: 'Chicken Breast',
    price: '$3.80',
    type: 'Meat',
    image: 'images/chickenbreast.jfif',
    quantity: 1,
  },
  {
    name: 'Milk',
    price: '$1.60',
    type: 'Dairy',
    image: 'images/milk.jfif',
    quantity: 1,
  },
  {
    name: 'Oat',
    price: '$1.50',
    type: 'Grain',
    image: 'images/oat.jfif',
    quantity: 1,
  },
  {
    name: 'Yogurt',
    price: '$2.40',
    type: 'Dairy',
    image: 'images/yogurt.jfif',
    quantity: 1,
  },
  {
    name: 'Cheese',
    price: '$3.10',
    type: 'Dairy',
    image: 'images/cheese.jpg',
    quantity: 1,
  },
  {
    name: 'Avocado',
    price: '$2.80',
    type: 'Fruit',
    image: 'images/avocado.jfif',
    quantity: 1,
  },
  {
    name: 'Lime',
    price: '$1.30',
    type: 'Fruit',
    image: 'images/lime.jfif',
    quantity: 1,
  },
  {
    name: 'Peas',
    price: '$1.90',
    type: 'Vegetable',
    image: 'images/peas.jfif',
    quantity: 1,
  },
  {
    name: 'Strawberry',
    price: '$3.60',
    type: 'Fruit',
    image: 'images/strawberry.jfif',
    quantity: 1,
  },
  {
    name: 'Duck',
    price: '$4.70',
    type: 'Meat',
    image: 'images/duck.jpg',
    quantity: 1,
  },
  {
    name: 'Lamb',
    price: '$4.20',
    type: 'Meat',
    image: 'images/lamb.jfif',
    quantity: 1,
  },
  {
    name: 'Pork',
    price: '$3.50',
    type: 'Meat',
    image: 'images/pork.jfif',
    quantity: 1,
  },
  {
    name: 'Mutton',
    price: '$3.90',
    type: 'Meat',
    image: 'images/mutton.jfif',
    quantity: 1,
  },
  {
    name: 'Spam',
    price: '$2.70',
    type: 'Meat',
    image: 'images/spam.jfif',
    quantity: 1,
  },
]
</script>

<style scoped></style>
