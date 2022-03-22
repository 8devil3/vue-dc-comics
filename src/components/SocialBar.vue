<template>
  <section class="social-bar">
    <div class="container">
      <button>sign-up now</button>
      <nav>
        <h2>follow us</h2>
        <a :href="social.link" v-for="(social, index) in socialIcons" :key="index"><img :src="'../assets/img/' + social.img" :alt="social.alt"></a>
      </nav>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SocialBar',
  data () {
    return {
      socialIcons: [
        {
          alt: 'Facebook',
          img: 'footer-facebook.png',
          link: '#'
        },
        {
          alt: 'Twitter',
          img: 'footer-twitter.png',
          link: '#'
        },
        {
          alt: 'YouTube',
          img: 'footer-youtube.png',
          link: '#'
        },
        {
          alt: 'Pinterest',
          img: 'footer-pinterest.png',
          link: '#'
        },
        {
          alt: 'Periscope',
          img: 'footer-periscope.png',
          link: '#'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/scss/partials/_variables.scss';

.social-bar {
  background-color: $social-bar-bkg;
  padding: 2rem 0.5rem;

    > div {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
}

nav {
  display: flex;
  align-items: center;

  h2 {
    color: $primary-color;
    text-transform: uppercase;
  }
}

img {
  display: block;
  margin: 1rem;
}

button {
  background-color: transparent;
  border: 2px $primary-color solid;
  color: $footer-title-color;
  font-size: 1rem;
  font-weight: 700;
  text-transform: uppercase;
  text-align: center;
  padding: 0.75rem;
  cursor: pointer;
}

</style>
