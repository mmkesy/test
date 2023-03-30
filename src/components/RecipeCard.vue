<script setup>

defineProps({
  imageurl: String,
  imgalt: String,
  titleurl: String,
  title: String,
  description: String,
  time: String,
  servings: String,
  level: String
})

</script>

<template>
  <div class="m-5 shadow-md w-80 rounded overflow-hidden    ">
      <img :src="imageurl" :alt="imgalt">
      <div class="p-2">
        <div class="font-bold text-lg text-gray-700 leading-snug">
          <a :href="titleurl" class="hover:underline">{{ title }}</a>
        </div>
        <p class="text-xs leading-tight tracking-wide my-2">{{ description }}</p>
        <div class="flex pt-2 border-t border-gray-300 text-sm text-gray-700 divide-x-2">
          <div class="flex-1 text-center">
            <i class="far fa-clock"></i>
            <p>{{ time }}</p>
          </div>
          <div class="flex-1 text-center">
            <i class="fas fa-utensils"></i>
            <p>{{ servings }}</p>
          </div>
          <div class="flex-1 text-center">
            <i class="fas fa-signal"></i>
            <p>{{ level }}</p>
          </div>
        </div>
      </div>
    </div>

</template>

