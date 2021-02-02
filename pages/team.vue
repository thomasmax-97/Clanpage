<template>
  <section class="text-gray-400 body-font">
    <div class="container px-5 py-24 mx-auto">
      <div class="flex flex-col text-center w-full mb-20">
        <h1 class="text-2xl font-medium title-font mb-4 text-white tracking-widest">
          Unser Team
        </h1>
        <p class="lg:w-2/3 mx-auto leading-relaxed text-base">
          {{ content }}
        </p>
      </div>
      <div class="flex flex-wrap -m-4">
        <team-card :data="{players}" />
      </div>
    </div>
  </section>
</template>

<script>
import TeamCard from '@/components/TeamCard'

export default {
  components:{
    TeamCard
  },
  async asyncData({$axios}){
    let {data} = await $axios.get('api/team')

    let {
      content,
      team_players: players
    } = data.data

    return {
      content,
      players
    }
  },
}
</script>
