<template>
  <base-container title="Vuex" v-if="isAuth">
  <display-counter></display-counter>
  <FavoriteValue></FavoriteValue>
  <button @click="addOne">Add 10</button>
  <ChangeCounter></ChangeCounter>
  </base-container>
  <base-container title="Auth">
  <user-auth></user-auth>
  </base-container>
</template>

<script>
import BaseContainer from './components/BaseContainer.vue';
import DisplayCounter from './components/DisplayCounter.vue';
import ChangeCounter from './components/ChangeCounter.vue'
import FavoriteValue from './components/FavoriteValue.vue'
import UserAuth from './components/UserAuth.vue';

export default {
  components: {
    BaseContainer,
    DisplayCounter,
    ChangeCounter,
    FavoriteValue,
    UserAuth
  },
  computed: {
        isAuth() {
           return this.$store.getters.userAuthenticated;
        }
    },

  methods: {
    addOne() {
      // this.$store.commit('increase', {value: 10 })
      this.$store.dispatch({
        type: 'increase',
        value: 10
      })
    }
  }
};
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>