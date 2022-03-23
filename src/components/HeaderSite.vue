<template>
<header>
  <div class='container header'>
    <img src="../assets/img/dc-logo.png" alt="DC logo">
    <nav>
      <a v-for="(link, index) in menuLinks" :key="index" :href="link.href" @click="activeLink=index" :class="activeLink==index ? 'active' : ''"><span>{{ link.text }}</span></a>
    </nav>
  </div>
</header>
</template>

<script>
export default {
  name: 'HeaderSite',
  data () {
    return {
      activeLink: 0,
      menuLinks: [
        {
          href: '#',
          text: 'characters'
        },
        {
          href: '#',
          text: 'comics'
        },
        {
          href: '#',
          text: 'movies'
        },
        {
          href: '#',
          text: 'games'
        },
        {
          href: '#',
          text: 'collectibles'
        },
        {
          href: '#',
          text: 'videos'
        },
        {
          href: '#',
          text: 'fans'
        },
        {
          href: '#',
          text: 'news'
        },
        {
          href: '#',
          text: 'shop'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/scss/partials/_variables.scss';

header {
  padding: 0 0.5rem;
}

.header {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: stretch;
}

nav {
  display: flex;
  flex-direction: row;
}

a {
  text-transform: uppercase;
  color: $header-link-color;
  font-family: 'Encode Sans Condensed', sans-serif;
  font-weight: 700;
  font-size: 0.8rem;
  margin: 0 0 0 2rem;
  display: block;
  height: 100%;
  display: flex;
  align-items: center;
  border-bottom: 0.3rem transparent solid;

    &:hover {
      border-bottom: 0.3rem $primary-color solid;
      color: $primary-color;
    }
}

.active {
      border-bottom: 0.3rem $primary-color solid;
      color: $primary-color;
    }

img {
  height: 5rem;
  width: 5rem;
  display: block;
  margin: 1rem 0;
}

</style>
