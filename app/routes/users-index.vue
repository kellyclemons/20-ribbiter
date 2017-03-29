<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">
        <div class="users-heading">
          <h1>Users</h1>
        </div>

        <div class="users-grid">

          <div class="users-grid__item">
            <div class="user">
              <img src="#" alt="" class="user-image">
              <div class="user-info">
                <p class="user-info__name">{{ user.username }}</p>
                <a href="" class="user-info__email">{{ user.email }}</a>
              </div>
            </div>
          </div>

        </div>

      </div>
    </div>
  </div>
</template>

<script>
import store from '../store';
import userResource from '../resources/user';
export default {
  name: 'Users',
  data() {
    return {
      users: this.$select('users'),
    };
  },

  methods: {
  },

  created() {
    const {
      actionCreators: {
        findAll,
      },
    } = userResource;
    store.dispatch(findAll());
  },
};
</script>
