<template>
  <article>
    <img :src="img" :alt="title">
    <p class="comic-title">{{ title }}</p>
    <p class="comic-price">{{ price }}</p>
  </article>
</template>

<script>
export default {
  name: 'CurrentSeries',
  props: {
    title: String,
    img: String,
    price: Number
  }
}
</script>

<style lang="scss" scoped>

article {
  width: calc(100% / 6 - 1rem);

  img {
    width: 100%;
  }

  .comic-title {
    text-transform: uppercase;
    font-size: 0.9rem;
    margin-top: 0.5rem;
  }

  .comic-price {
    color: #999;
    font-size: 0.75rem;
    margin-top: 0.25rem;
  }
}

</style>
