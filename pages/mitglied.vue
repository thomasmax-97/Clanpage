<template>
  <div>
    <Applyhead :data="{heading, content}" />
    <Apply />
    <Faq :data="{faq}" />
  </div>
</template>
<script>
import Apply from '@/components/Apply'
import Applyhead from '@/components/Applyhead'
import Faq  from '@/components/Faq'

export default {
  components:{
    Apply,
    Applyhead,
    Faq,
  },
  async asyncData({$axios}){
    let {data} = await $axios.get('api/member')

    let {
      content,
      heading,
      faq : faq
    } = data

    return {
      content,
      heading,
      faq
    }
  },
}
</script>
