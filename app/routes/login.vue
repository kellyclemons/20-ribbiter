<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">
          <div class="login">
            <div class="login__heading">
              <h1>Login</h1>
            </div>

          <form @submit.prevent="submit" class="login-form">

            <div class="form-input">
              <p class="form-input__prompt">Email</p>
              <input type="text" class="form-input" placeholder="Email" id="email">
            </div>

            <div class="form-input">
              <p class="form-input__prompt">Password</p>
              <input type="text" class="form-input" placeholder="Password" id="password">
            </div>

            <div class="form-buttons">
              <router-link class="form-buttons__register" :to="{ name: 'register' }">Register</router-link>
              <div class="form-buttons__login">Login</div>
            </div>

          </form>
          </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data() {
    return {
    };
  },

  methods: {

  },
};
</script>
