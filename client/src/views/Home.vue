<template>
<div>
  <Hero
  pageTitle="Foundations"
  />
  <article>
    <h2>Introduction to Project</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Leo integer malesuada nunc vel. Pellentesque adipiscing commodo elit at imperdiet. Vulputate dignissim suspendisse in est ante in nibh.</p>

    <!-- TODO load content dynamically with a loop -->
    <div class="logos">
      <img width="100px" v-for="(logo, index) in logos" :key="index" :src="logo.url" :alt="logo.alt" />
    </div>
  </article>
  <section>

  </section>
  <!-- So what statement -->
  <article>
    <h2>Why is this important?</h2>
    <p>Because there are so many choices and it is satisfying for both the developer and user when the right choice is made</p>
    <section>
      <div>
        <h3>Python Server</h3>
        <p>Section requires editing. this should be a quick intro blurb</p>
        <ul>
          <li>Data Science</li>
          <li>AI and Machine Learning</li>
          <li>Synchronous</li>
          <li>Elegant Syntax</li>
        </ul>
      </div>
      <div>
        <h3>JavaScript Server</h3>
        <ul>
          <li>Asynchronous</li>
          <li>IOT</li>
          <li>Real Time Applications</li>
          <li>Scalable</li>
        </ul>
      </div>
      </section>
  </article>
  <section class="image-ribbon">

  </section>
  <article>
    <div>
      <img src="#" alt="">
      </div>
    <div>
    <h2>Another Options</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <button>Link to resources</button>
    </div>
  </article>
</div>
</template>

<script>
import Hero from '../components/Hero.vue'

export default {
  components: {
    Hero
  },
  props: {
    logo: Object
  },
  data () {
    return {
      pageInfo: {
        name: 'Home'
      },
      logos: [
        {
          url: require('../assets/logos/vue.png'),
          altText: 'vue logo'
        },
        {
          url: require('../assets/logos/python-logo.png'),
          alt: 'flask logo'
        },
        {
          url: require('../assets/logos/node.png'),
          alt: 'node logo'
        },
        {
          url: require('../assets/logos/ExpressJS-logo.png'),
          alt: 'node logo'
        }
      ]
    }
  }
}

</script>

<style scoped>
article {
  padding: 2rem;
}

.image-ribbon {
  background-image: url('../assets/images/pexels-christina-morillo.jpg');
  background-position: center;
  background-size: cover;

  height: 40vh;
}
.logos > * {
  margin: 1rem;
}
</style>
