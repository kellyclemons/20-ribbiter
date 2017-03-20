<template lang="html">
  <div class="">
    <div class="section">
      <div class="container">
        <div class="ribbits-heading">
          <h1>Recent Ribbits</h1>
        </div>

        <div class="ribbit">
          <div class="ribbit__heading">
            <h1>New Ribbit</h1>
          </div>
        <form @submit.prevent="submit" class="ribbit-form">
          <div class="ribbit-form__content"></div>
        </form>

        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Ribbits',
  data() {
    return {
    };
  },

  methods: {

  },
};
</script>
