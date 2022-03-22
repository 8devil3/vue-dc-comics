<template>
  <section class="blue-icons">
    <div class='container'>
      <div class="icon" v-for="(icon, index) in icons" :key="index" >
        <img :src="'../assets/img/' + icon.img" :alt="icon.text">
        <p>{{ icon.text }}</p>
      </div>
    </div>
  </section>
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

.blue-icons {
  background-color: $primary-color;
  padding: 2.5rem 0.5rem;
  color: $main-text-color;
  font-size: 0.8rem;
  text-transform: uppercase;

    > div {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .icon {
      display: flex;
      align-items: center;
        img {
          margin: 0.5rem;
          height: 4rem;
        }
    }
}

</style>
