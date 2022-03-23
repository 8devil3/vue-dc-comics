<template>
<main>
  <section id="jumbotron">
    <img src="../assets/img/dc-comics_banner.png" alt="DC Comics">
  </section>
  <section id="comics" class="container">
    <div class="lbl">current series</div>
    <CurrentSeries
      v-for="card in comics"
      :img="card.thumb"
      :title="card.series"
      :price="card.price"
      :key="card.series"
    />
    <button class="btn-primary">load more</button>
  </section>
  <section id="blue-icons">
    <BlueIcons />
  </section>
</main>
</template>

<script>
import BlueIcons from './BlueIcons.vue'
import CurrentSeries from './CurrentSeries.vue'
import comics from './dc-comics.json'

export default {
  name: 'MainSite',
  components: {
    BlueIcons,
    CurrentSeries
  },
  data () {
    return {
      comics
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/scss/partials/_variables.scss';
@import '../assets/scss/partials/_mixin.scss';

main {
  background-color: $main-bkg-color;
  color: $main-text-color;

  #jumbotron {
    img {
      object-fit: contain;
      width: 100%;
    }
  }

  #comics {
    @include flex(row, center, stretch, wrap, 1);
    padding: 2rem 0.5rem;
    gap: 1rem;
    position: relative;
  }

  #blue-icons {
    background-color: $primary-color;
    padding: 2.5rem 0.5rem;
    color: $main-text-color;
    font-size: 0.8rem;
    text-transform: uppercase;
  }
}

</style>
