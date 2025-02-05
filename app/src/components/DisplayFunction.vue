<template>
  <div
    class="card w-1/6 h-[15vw] bg-gray-400 rounded-3xl flex flex-col items-center justify-evenly m-6 border-2 border-black"
  >
    <h2 class="text-center font-bold text-2xl">{{ item.name }}</h2>
    <img
      :src="item.image"
      :alt="item.type"
      class="object-cover w-[90%] h-[55%] rounded-lg shadow-md border-black border-2"
    />
    <h3 class="text-center text-xl">{{ item.price }}</h3>
  </div>
</template>

<script setup>
defineProps({
  item: Object,
})
</script>

<style scoped></style>
