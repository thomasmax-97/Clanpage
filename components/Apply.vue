<template>
  <form id="contact-me" class="w-full mx-auto max-w-3xl bg-gray-900 shadow p-8 text-gray-700"
        v-on:submit.prevent="submit">
    <h2 class="w-full text-center  text-white my-2 text-3xl font-bold leading-tight my-5">Bewerben</h2>
    <!-- name field -->
    <div class="flex flex-wrap mb-6">
      <div class="relative w-full appearance-none label-floating">
        <input
          v-model="contact.name"
          class="tracking-wide py-2 px-4 mb-3 leading-relaxed appearance-none block w-full bg-gray-700 border border-gray-700 rounded focus:outline-none text-white focus:border-gray-500"
          type="text" placeholder="Name " required>
        <label for="name"
               class="absolute tracking-wide py-2 px-4 mb-4 opacity-0 leading-tight block top-0 left-0 cursor-text">
          Name
        </label>
      </div>
    </div>
    <!-- email field -->
    <div class="flex flex-wrap mb-6">
      <div class="relative w-full appearance-none label-floating">
        <input
          v-model="contact.email"
          class="tracking-wide py-2 px-4 mb-3 leading-relaxed appearance-none block w-full bg-gray-700 border border-gray-700 text-white rounded  focus:border-gray-500"
          id="email" type="text" placeholder="Email" name="name" required>
        <label for="email"
               class="absolute tracking-wide py-2 text-gray-400 px-4 mb-4 opacity-0 leading-tight block top-0 left-0 cursor-text">
          Email
        </label>
      </div>
    </div>
    <!-- Message field -->
    <div class="flex flex-wrap mb-6">
      <div class="relative w-full appearance-none label-floating">
            <textarea
              v-model="contact.message"
              class="autoexpand tracking-wide py-2 px-4 mb-3 leading-relaxed appearance-none block w-full bg-gray-700 border border-gray-700 rounded focus:outline-none text-white focus:border-gray-500"
              id="message" type="text" placeholder="Bewerbung"></textarea>
        <label for="message"
               class="absolute tracking-wide py-2 px-4 mb-4 opacity-0 leading-tight block top-0 left-0 cursor-text">Message...
        </label>
      </div>
    </div>
    <div class="">
      <button
        class="w-full shadow text-white bg-indigo-500 hover:bg-indigo-600 focus:shadow-outline focus:outline-none text-white font-bold py-2 px-4 rounded"
        type="submit"
        @click="submit">
        Send
      </button>
    </div>
  </form>

</template>

<script>
export default {
  data() {
    return {
      contact: {
        name: '',
        email: '',
        message: '',
      }
    }
  },
  methods: {
    async submit() {
      await this.$axios.post('/api/member', {
        name: this.contact.name,
        email: this.contact.email,
        message: this.contact.message
      })
        .then(function (response) {
          console.log(response);
        })
        .catch(function (error) {
          console.log(error);
        });
    },
  },
}
</script>
