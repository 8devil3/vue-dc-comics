<template>
  <div class='container'>
    <div class="icon" v-for="(icon, index) in icons" :key="index" >
      <img :src="require('../assets/img/' + icon.img)" :alt="icon.text">
      <p>{{ icon.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BlueIcons',
  data () {
    return {
      icons: [
        {
          img: 'buy-comics-digital-comics.png',
          text: 'digital comics'
        },
        {
          img: 'buy-comics-merchandise.png',
          text: 'dc merchandise'
        },
        {
          img: 'buy-comics-subscriptions.png',
          text: 'subscription'
        },
        {
          img: 'buy-comics-shop-locator.png',
          text: 'comic shop locator'
        },
        {
          img: 'buy-dc-power-visa.svg',
          text: 'dc power visa'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/scss/partials/_variables.scss';
@import '../assets/scss/partials/_mixin.scss';

.container {
  @include flex(row, space-between, center, wrap);
}

.icon {
  @include flex();

  img {
    margin: 0.5rem;
    width: 3rem;
    height: 3rem;
    object-fit: contain;
  }
}

</style>
