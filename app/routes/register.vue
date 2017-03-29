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
              <input type="text" v-model="formValues.username" class="form-input" placeholder="Username" id="username">
            </div>

            <div class="form-input">
              <p class="form-input__prompt">Email</p>
              <input type="text" v-model="formValues.email" class="form-input" placeholder="Email" id="email">
            </div>

            <div class="form-input">
              <p class="form-input__prompt">Password</p>
              <input type="password" v-model="formValues.password" class="form-input" placeholder="Password" id="password">
            </div>

            <div class="form-buttons">
              <router-link class="form-buttons__login" :to="{ name: 'login' }">Login</router-link>
              <button class="form-buttons__register" type="submit">Sign Up</button>
            </div>

          </form>
          </div>

        <div class="error" v-if="users.loading === 'error'">
          <h1>Sorry, there was an error with this username/password</h1>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
import store from '../store';
import userResource from '../resources/user';
const {
  actionCreators: {
    create
  }
} = userResource;
export default {
  name: 'Register',
  data() {
    return {
      formValues: {
        username: '',
        email: '',
        password: '',
      },
      users: this.$select('users'),
    };
  },

  methods: {
    submit() {
      store.dispatch(create(this.formValues))
        .then(() => {
          this.$router.push({
            name: 'users'
          });
        }).catch(() => {});
    },
  },
};
</script>
