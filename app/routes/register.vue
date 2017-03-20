<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">
          <div class="account">
            <div class="account__heading">
              <h1>Create an Account</h1>
            </div>

          <form @submit.prevent="submit" class="register-form">

            <div class="form-input">
              <p class="form-input__prompt">Username</p>
              <input type="text" class="form-input" placeholder="Username" id="username">
            </div>

            <div class="form-input">
              <p class="form-input__prompt">Email</p>
              <input type="text" class="form-input" placeholder="Email" id="email">
            </div>

            <div class="form-input">
              <p class="form-input__prompt">Password</p>
              <input type="text" class="form-input" placeholder="Password" id="password">
            </div>

            <div class="form-buttons">
              <router-link class="form-buttons__login" :to="{ name: 'login' }">Login</router-link>
              <div class="form-buttons__register">Sign Up</div>
            </div>

          </form>

          </div>
      </div>
    </div>


  </div>
</template>

<script>
export default {
  name: 'Register',
  data() {
    return {
    };
  },

  methods: {

  },
};
</script>
