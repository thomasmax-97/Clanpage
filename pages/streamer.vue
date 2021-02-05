<template>
  <div class="streamer">
    <div v-for=" item in data">
      <StreamCard :data="item"/>
    </div>
  </div>
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
