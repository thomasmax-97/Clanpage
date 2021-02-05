<template>
  <div class="flex flex-wrap -mx-32 overflow-hidden md:-mx-32">
    <div
      class="max-w-sm mx-auto bg-white dark:bg-gray-800 shadow-lg rounded-lg overflow-hidden mt-10 bg-gray-700  bg-opacity-50"
      v-for="item in data.players">
      <img class="w-full h-56 object-cover object-center"
           :src="item.image"
           alt="avatar">
      <div class="flex items-center px-1 py-3 bg-gray-900">
        <h1 class="text-white font-semibold text-lg">{{item.role}}</h1>
      </div>
      <h1 class="text-xl font-semibold">{{item.players}}</h1>
      <p class="py-2 text-white">{{item.desc}}</p>
    </div>
  </div>


</template>

<script>
export default {
  props: {
    data: {
      players: {
        type: Object,
        required: true,
      }
    },
  },
}
</script>
