<script>
  import card1 from './components/card1.vue';
  import card2 from './components/card2.vue';

  export default {
    data() {
      return {
        currentComponent: "card1",
      };
    },
    methods: {
      toggle() {
        this.currentComponent = this.currentComponent === "card1" ? "card2" : "card1";
      },
    },
    components: {
      card1,
      card2,
    },
  };
</script>

<template>
    <center>
      <h1 style="text-align: center; color:green">
        GeeksforGeeks
      </h1>
      <strong>
        Vue.js Dynamic Components
      </strong>
      <br />
    </center>
    <center>
      <component :is="currentComponent" />
      <button @click="toggle">Toggle</button>
    </center>
</template>

<style>

</style>
