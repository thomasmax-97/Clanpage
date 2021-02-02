<template>
  <div>
    <section
      class="text-gray-700"
    >
      <div class="container px-5 py-24 mx-auto">
        <div class="text-center mb-20">
          <h1 class="sm:text-3xl text-2xl font-medium text-center title-font text-white mb-4">
            FAQ- HÄUFIG GESTELLTE FRAGEN
          </h1>
        </div>

        <div class="flex flex-wrap lg:w-4/5 sm:mx-auto sm:mb-2 -mx-2">
          <div
            v-for="item in data.faq"
            class="w-full lg:w-1/2 px-4 py-2"
          >
            <details class="mb-4">
              <summary class="font-semibold  bg-gray-200 rounded-md py-2 px-4">
                {{ item.question }}
              </summary>
              <span class=" text-white">
                {{ item.answer }}
              </span>
            </details>
          </div>
        </div>
      </div>
    </section>
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
