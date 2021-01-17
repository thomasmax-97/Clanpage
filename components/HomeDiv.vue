<template>
  <div
    class="gpg-home-container fixed"
  >
    <div class="flex flex-wrap w-full mb-20 flex-col items-center text-center">
      <h1 class="text-white md:w-32 lg:w-48 sm:text-lg text-center md:font-serif gpg-font-bold gpg-header">
        GERMANY PLAYSGROUP
      </h1>
      <div class="flex m-auto flex-row flex-wrap	justify-center items-center">
        <NuxtLink to="/verein">
          <button
            class="uppercase px-12 py-4 rounded gpg-bg-primary text-blue-50 max-w-max shadow-sm hover:shadow-lg justify-center"
          >
            <span>Erfahre Mehr!</span>
          </button>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<style>
/* TODO MAKE RESPONSIVE */
.gpg-home-container{
  top: 45%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.gpg-header{
  font-size: 6.375rem;
  font-weight: bold;
  width:max-content;

}
@media screen and (max-width: 50em) {
.gpg-header{
  font-size: 4.375rem;
  font-weight: bold;
  width:min-content;
}
}
@media screen and (max-width: 30em) {
.gpg-header{
  font-size: 3.100rem;
  font-weight: bold;
  width:min-content;
}
}
</style>
