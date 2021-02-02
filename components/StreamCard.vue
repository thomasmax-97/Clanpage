<template>
  <div class="p-4 md:w-1/3">
    <div class="h-full border-2 border-gray-800 bg-gray-900 rounded-lg overflow-hidden">
      <img
        class="lg:h-48 md:h-36 w-full object-cover object-center"
        :src="data.image"
        alt="blog"
      >
      <div class="p-6">
        <h1 class="title-font text-lg font-medium text-white mb-3">
          <a href="https://www.twitch.tv/" target="_blank">
            {{data.players}}
          </a>
        </h1>x
        <p class="leading-relaxed mb-3">
          {{data.desc}}
        </p>
        <div class="flex items-center flex-wrap ">
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  props: {
    data: {
      type: Object,
      required: true,
    }
  },
}
</script>
