<template>
  <section class="text-gray-400 body-font">
    <div class="container px-5 py-24 mx-auto">
      <div class="flex flex-wrap -m-4" v-for="item in data">
        <StreamCard :data="item"/>
      </div>
    </div>
  </section>
</template>

<script>
import StreamCard from '@/components/StreamCard'

export default {
  components: {
    StreamCard,
  },
  async asyncData({$axios}) {
    let {data} = await $axios.get('api/streamer')

    return data
  },
}
</script>
