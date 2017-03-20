<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">
        <div class="main">
          <div class="welcome">
            <div class="welcome__heading">
              <h1>Welcome to Ribbiter</h1>
            </div>
            <div class="welcome__bottom">
              <div class="welcome__button">
                <router-link class="register-button" :to="{ name: 'register' }">Register</router-link>
              </div>
              <div class="welcome__button">
                <router-link class="login-button" :to="{ name: 'login' }">Login</router-link>
              </div>
            </div>

          </div>
        </div>
      </div>
    </div>


  </div>
</template>

<script>
export default {
  name: 'Index',
  data() {
    return {
    };
  },

  methods: {

  },
};
</script>
