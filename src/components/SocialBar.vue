<template>
<section id="social-bar-wrapper">
  <div class="container">
    <button class="btn-footer">sign-up now</button>
    <nav>
      <h2>follow us</h2>
      <a :href="social.link" v-for="(social, index) in socialIcons" :key="index"><img :src="require('../assets/img/' + social.img)" :alt="social.alt"></a>
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
@import '../assets/scss/partials/_mixin.scss';

#social-bar-wrapper {
  background-color: $social-bar-bkg;
  padding: 2rem 0.5rem;

  .container {
    @include flex(row, space-between);

    nav {
      @include flex();

      h2 {
        color: $primary-color;
        text-transform: uppercase;
        margin-right: 1rem;
      }

      img {
        display: block;
        margin: 0.5rem;
      }
    }
  }
}

</style>
