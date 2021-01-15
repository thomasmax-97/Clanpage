<template>
  <section class="text-gray-400 body-font relative">
    <div class="absolute inset-0 bg-gray-900">
      <iframe
        title="map"
        style="filter: grayscale(1) contrast(1.2) opacity(0.16);"
        marginheight="0"
        marginwidth="0"
        scrolling="no"
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2572.6642840453014!2d8.351064715879849!3d49.8487652384157!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47bd85d36dd2da53%3A0x56f987f2d52e9f0f!2sGermany-playsgroup%20e.V.!5e0!3m2!1sde!2sde!4v1610207066108!5m2!1sde!2sde"
        width="100%"
        height="100%"
        frameborder="0"
      />
    </div>
    <div class="container px-5 py-24 mx-auto flex">
      <div class="lg:w-1/3 md:w-1/2 bg-gray-900 shadow-md rounded-lg p-8 flex flex-col md:ml-auto w-full mt-10 md:mt-0 relative z-10">
        <h2 class="text-white text-lg mb-1 font-medium title-font">
          Kontakt
        </h2>
        <p class="leading-relaxed mb-5">
          orem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam mauris arcu, aliquet in finibus sed
        </p>
        <div class="relative mb-4">
          <label
            for="email"
            class="leading-7 text-sm text-gray-400"
          >Email</label>
          <input
            id="email"
            type="email"
            name="email"
            class="w-full bg-gray-800 rounded border border-gray-700 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-900 text-base outline-none text-gray-100 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out"
          >
        </div>
        <div class="relative mb-4">
          <label
            for="message"
            class="leading-7 text-sm text-gray-400"
          >Nachricht</label>
          <textarea
            id="message"
            name="message"
            class="w-full bg-gray-800 rounded border border-gray-700 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-900 h-32 text-base outline-none text-gray-100 py-1 px-3 resize-none leading-6 transition-colors duration-200 ease-in-out"
          />
        </div>
        <button class="text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg">
          Abschicken
        </button>
        <p class="text-xs text-gray-400 text-opacity-90 mt-3">
          Vivamus nec eros justo. Suspendisse tortor torto
        </p>
      </div>
    </div>
  </section>
</template>
