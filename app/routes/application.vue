<template lang="html">
  <div class="">
    <div class="top-nav">
      <div class="navbar">
        <router-link :to="{ name: 'index' }">Ribbeter</router-link>
        <ul class="nav-right">
          <router-link :to="{ name: 'ribbits'}" class="nav-right__item">Ribbets</router-link>
          <router-link :to="{ name: 'users' }" class="nav-right__item">Frogs</router-link>
          <router-link :to="{ name: 'login' }" class="nav-right__item">Login</router-link>
        </ul>
      </div>
    </div>

    <router-view></router-view>

  </div>
</template>

<script>
import Index from './index.vue';
export default {
  components: {
    Index,
  },

  name: 'Application',
  data() {
    return {
    };
  },

  methods: {

  },
};
</script>
