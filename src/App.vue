<template>
  <div id="app" class="bg-gray-000 sm:h-screen">
    <div id="nav" class="block ml-10 pr-4">
      <nav class="flex justify-center items-center mt-4">
          <div class="flex flex-row mt-5">
            <router-link to="/" class="mt-3 text-gray-600 mx-3 font-semibold hover:text-gray-500">Joke</router-link>
            <router-link to="/jokes" class="mt-3 text-gray-600 mx-3 font-semibold hover:text-gray-500">First jokes</router-link>
          </div>
      </nav>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  mounted(){
    this.$store.dispatch('setCurrentJoke');
  }
}
</script>

<style lang='scss'></style>
