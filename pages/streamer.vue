<template>
  <section class="text-gray-400 body-font">
    <div class="container px-5 py-24 mx-auto">
      <div class="flex flex-wrap -m-4">
        <StreamCard />
        <StreamCard />
        <StreamCard />
      </div>
    </div>
  </section>
</template>

<script>
import StreamCard from '@/components/StreamCard'

export default {
  components:{
    StreamCard,
  }
}
</script>
