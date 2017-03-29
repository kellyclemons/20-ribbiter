<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">
        <p class="ribbits-heading">Recent Ribbits</p>
        <div class="grid">
          <div class="grid__item sidebar">
          <div class="new-card">
            <p class="new-card__heading">New Ribbit</p>
            <form @submit.prevent="submit">
              <div class="new-card__contents">
                <p class="new-card__contents-heading">What's Going On?</p>
                <textarea v-model="formValues.body" rows="4"></textarea>
              </div>
              <div class="buttons">
                <button class="buttons-clear" @click="clear">Clear</button>
                <button class="buttons-save" @submit.prevent="submit">Save</button>
              </div>
            </form>
          </div>
        </div>

          <div class="grid__item happening">
            <p class="new-card__heading">See What's Happening!</p>
            <div class="happening-contents">
              <button @click="load" class="load-ribbits__button">Load New Ribbits</button>
            </div>
            <div v-for="post in posts.items" class="card-row">
              <a href="#" class="card-row__link">{{ post.user.username }}</a>
              <p>{{ post.body }}</p>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>



</template>

<script>
import store from '../store.js';
import postResource from '../resources/post';
export default {
  name: 'Ribbits',
  data() {
    return {
      formValues: {
        body: '',
      },
      posts: this.$select('posts'),
    };
  },

  created() {
    this.load();
  },

  methods: {
    load() {
      const { actionCreators: { findAll } } = postResource;
      store.dispatch(findAll());
    },

    clear() {
      this.formValues = { body: '' };
    },

    submit() {
      const { actionCreators: { create } } = postResource;
      store.dispatch(create(this.formValues)).then(() => {
        this.clear();
      });
    }
  },
};
</script>
