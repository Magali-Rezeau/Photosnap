<template>
  
  <section class="features">
    <div class="features-card" v-for="feature in features" :key="feature.name">
      <img src="./../../assets/img/features/responsive.svg"/>
     
      <h2>{{ feature.name }}</h2>
      <p>{{ feature.description }}</p>
     
    </div>
  </section>
   <!-- <app-link></app-link> -->

</template>

<script>
// import AppLink from './../AppLink.vue';

export default {
  
  components: {
    // AppLink,
  },
  data() {
    return {
      features: [
        {
          logoSvg: "./../../assets/img/features/responsive.svg",
          name: "100% responsive",
          description: "No matter which the device you’re on, our site is fully responsive and stories look beautiful on any screen.",
        },
        {
          logoSvg: "./../../assets/img/features/no-limit.svg",
          name: "No photo upload limit",
          description: "Our tool has no limits on uploads or bandwidth. Freely upload in bulk and share all of your stories in one go.",
        },
        {
          logoSvg: "./../../assets/img/features/embed.svg",
          name: "Available to embed",
          description: "Embed Tweets, Facebook posts, Instagram media, Vimeo or YouTube videos, Google Maps, and more.",
        },
        {
          logoSvg: "./../../assets/img/features/custom-domain.svg",
          name: "Custom domain",
          description: "With Photosnap subscriptions you can host your stories on your own domain. You can also remove our branding!",
        },
        {
          logoSvg: "./../../assets/img/features/boost-exposure.svg",
          name: "Boost your exposure",
          description: "Users that viewed your story or gallery can easily get notifed of new and featured stories with our built in mailing list.",
        },
        {
          logoSvg: "./../../assets/img/features/drag-drop.svg",
          name: "Drag & Drop image",
          description: "Easily drag and drop your image and get beautiful shots everytime. No over the top tooling to add friction to creating stories.",
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@mixin sm {
  @media (min-width: 600px) {
    @content;
  }
}
@mixin md {
  @media (min-width: 1100px) {
    @content;
  }
}
.features {
  padding: 4rem 2.5rem 5.70rem 2.5rem;
  display: grid;
  grid-template-rows: repeat(6, 14.75rem);
  grid-gap: 3.5rem;
  @include sm {
    grid-template-rows: repeat(3, 14.75rem);
    grid-template-columns: repeat(2, 1fr);
     padding: 7rem 2.5rem;
     grid-row-gap: 4.5rem;
     grid-column-gap: 1rem;
  }
  @include md {
    grid-template-rows: repeat(2, 14.75rem);
    grid-template-columns: repeat(3, 1fr);
     padding: 10rem;
     grid-row-gap: 6.5rem;
     grid-column-gap: 1.875rem;
  }
  &-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    & img {
      width: 4.5rem;
      height: 4.5rem;
    }
   
      
       & h2 {
      text-transform: capitalize;
      margin: 3rem 0 1rem 0;

    }
    & p {
      
      text-align: center;
      font-size: 15px;
line-height: 25px;
      opacity: .6;
    }
    
   
  }
}
</style>
