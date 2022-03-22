<template>
<main>
  <section>
    <div class='container'>
      <h2>contenuto</h2>
    </div>
  </section>
<BlueIcons />
</main>
</template>

<script>
import BlueIcons from './BlueIcons.vue'

export default {
  name: 'MainSite',
  components: {
    BlueIcons
  }
}
</script>

<style scoped lang="scss">
@import '../assets/scss/partials/_variables.scss';

section {
  background-color: $main-bkg-color;
  padding: 2.5rem 0.5rem;
  color: $main-text-color;
}

</style>
