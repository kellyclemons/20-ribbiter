<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">
        <div class="main">
          <div class="welcome">
            <p class="welcome__heading">
              Welcome To Ribbiter!
            </div>
            <div class="start-card">
              <p class="welcome__subheading">Let's Get Started!</p>
              <div class="welcome__bottom">
                <div class="welcome__button">
                  <router-link class="login-button" :to="{ name: 'login' }">Login</router-link>
                </div>
                <div class="welcome__button">
                  <router-link class="register-button" :to="{ name: 'register' }">Sign Up</router-link>
                </div>
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
