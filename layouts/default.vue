<template>
  <div class="flex flex-col h-screen justify-between jarallax">
    <bg-particle-video />
    <Navbar />
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import Footer from '@/components/Footer'
import BgParticleVideo from '@/components/bg-particle'

export default {
  components: {
    Navbar,
    Footer,
    BgParticleVideo
  },
}
</script>
