<template>
<div class="flex items-center justify-center" style="height: 95vh">
  <div class="home bg-indigo-000 mx-auto rounded-lg sm:w-10/12 lg:p-20">
      <main class="mx-auto max-w-screen-xl px-4 sm:px-0 lg:px-8 xl:mt-0">
        <div class="sm:text-center lg:text-left">
          <h2 class="text-center text-5xl tracking-tight leading-10 font-extrabold text-gray-900 mb-10 sm:text-5xl sm:leading-none md:text-6xl">
            Can I haz
            <span 
              class="text-indigo-600 hover:text-indigo-500 cursor-pointer"
              style=".noselect {-webkit-touch-callout: none;-webkit-user-select: none;-khtml-user-select: none;-moz-user-select: none;-ms-user-select: none;user-select: none;}" 
              @click="addJoke">
              Dad Jokes
            </span>
          </h2>
          <h2 class="h-24 text-center text-4xl tracking-tight leading-10 font-extrabold text-gray-900 mb-10 sm:text-5xl sm:leading-none md:text-4xl">
            <span class="text-indigo-600">{{joke}}</span>
          </h2>
        </div>
      </main>
  </div>
</div>
</template>

<script>
import { mapActions, mapGetters } from "vuex";
export default {
  name: 'Home',
  data: () => ({
    //joke: ''
  }),
  methods: {
    ...mapActions({addJoke: "setCurrentJoke", addLike: "setCurrentLike",}),
    //addJoke(){
      //this.$store.dispatch("setCurrentJoke");
      //this.setCurrentJoke();
    //}
  },
  computed: {
    ...mapGetters({joke: "getCurrentJoke"}),
    //joke(){
      //return this.$store.getters.getCurrentJoke;
      //return this.getCurrentJoke;
    //}
  }
  //mounted(){
    //this.joke = this.$store.getters.getCurrentJoke;
  //}
}
</script>
