<template>
  <div>
    <section class="container">
      <div>
        <logo/>
        <h1 class="title">
          {{ title }}
        </h1>
        <h2 class="subtitle">
          My magnificent Nuxt.js project by {{ name }}
        </h2>
        <div>
          <sample-component :title="indexText">
            ここがデフォルトのslot
            <div slot="named">
              こっちはnamedのslot
            </div>
          </sample-component>
        </div>
        <div>
          <button-component />
        </div>
        <div>
          <reverse-name-component />
        </div>
        <div>
          <class-style-bind-component />
        </div>
        <div class="links">
          <a
            href="https://nuxtjs.org/"
            target="_blank"
            class="button--green">Documentation</a>
          <a
            href="https://github.com/nuxt/nuxt.js"
            target="_blank"
            class="button--grey">GitHub</a>
        </div>
        <div>
          <nuxt-link to="/about">ABOUT</nuxt-link>
        </div>
        <div>
          <nuxt-link to="/hoge">HOGE</nuxt-link>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import SampleComponent from '~/components/SampleComponent.vue'
import ButtonComponent from '~/components/ButtonComponent.vue'
import ReverseNameComponent from '~/components/ReverseNameComponent.vue'
import ClassStyleBindComponent from '~/components/ClassStyleBindComponent.vue'

export default {
  components: {
    Logo,
    SampleComponent,
    ButtonComponent,
    ReverseNameComponent,
    ClassStyleBindComponent
  },
  props: {
    title: {
      type: String,
      default: 'yeah!'
    }
  },
  data() {
    return {
      name: 'ggggg',
      indexText: 'kiyagare!!!'
    }
  },
  mounted() {
    console.log('mounted')
  }
}
</script>

<style>
.container {
  /* min-height: 100vh; */
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.çenter {
  text-align: center;
  margin-bottom: 100px;
}
</style>
