<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">
        <p class="ribbits-heading">Recent Ribbits</p>
        <div class="grid">
          <div class="grid__item sidebar">
          <form class="new-card">
            <p class="new-card__heading">New Ribbit</p>
            <div class="new-card__contents">
              <p class="new-card__contents-heading">What's Going On?</p>
              <textarea rows="4"></textarea>
            </div>
            <div class="buttons">
              <div class="buttons-clear">Clear</div>
              <div class="buttons-save">Save</div>
            </div>
          </form>
        </div>

          <div class="grid__item happening">
            <p class="new-card__heading">See What's Happening!</p>
            <div class="happening-contents">
              <a href="/app" class="load-ribbits__button">Load New Ribbits</a>
            </div>
            <div class="card-row">
              <a href="/users/kellyclemons" class="card-row__link">$kellyclemons</a>
              <p>This is a "tweet"</p>
            </div>
          </div>
        </div>
        <!-- <form @submit.prevent="submit" class="ribbit-form">
          <div class="ribbit-form__content"></div>
        </form> -->
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Ribbits',
  data() {
    return {};
  },

  methods: {

  },
};
</script>
