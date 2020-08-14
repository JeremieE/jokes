<template>
<div class="flex items-center justify-center" style="height: 95vh">
  <div class="home bg-indigo-000 mx-auto rounded-md sm:p-20 lg:w-10/12 md:w-12/12">
        <h1 class="text-center text-5xl tracking-tight leading-10 font-extrabold text-gray-900 mb-5 sm:text-5xl sm:leading-none md:text-6xl">Your 3 first <span class="text-indigo-600">Jokes</span></h1>
    <div class="mt-10 mb-16 text-center py-4 lg:px-4">
      <div
        class="p-4 bg-indigo-600 items-center text-indigo-100 leading-none mb-5 rounded flex ml-2 mr-2 lg:inline-flex"
        role="alert"
      >
        <span
          class="flex rounded text-gray-700 bg-indigo-100 uppercase px-2 py-1 text-xs font-bold mr-3"
        >LAST</span>
        <span class="font-semibold mr-2 text-left flex-auto">{{lastjoke}}</span>
      </div>
    </div>
    <div class="flex items-center justify-center sm:flex-col">
        <div class="align-items-center text-indigo-000 leading-none mb-5 lg:inline-flex h-40 mx-2">
            <div v-for="(joke,idx) in jokes.slice(0,3)" :key="idx" class="shadow-outline rounded h-48 flex flex-col items-center justify-center bg-indigo-000 max-w-sm mb-4 sm:p-5 sm:mr-5 sm:mb-5">
                <h1 class="text-center text-4xl tracking-tight leading-10 font-extrabold text-gray-900 mb-5 sm:text-5xl sm:leading-none md:text-5xl">
                    #{{idx+1}} 
                </h1>
                <span class="flex align-item-center text-indigo-600 text-xl text-center px-4">{{joke}}</span>
            </div>
        </div>
    </div>
    </div>
  </div>
</template>

<script>
import { mapGetters } from "vuex";
export default {
  computed: {
    ...mapGetters({ jokes: "getAllJokes", lastjoke: "getCurrentJoke" })
    //jokes(){
    //return this.$store.getters.getAllJokes;
    //}
  }
};
</script>

<style scoped>
h4 {
  color: blueviolet;
  font-weight: bolder;
  font-size: 2.5rem;
}
</style>