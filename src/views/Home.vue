<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <BaseFooter
      brand="Company Name"
      copyright-year="2020"
      :nav-links="[
        { label: 'Home' },
        { label: 'About' },
        { label: 'Product' },
        { label: 'Contact' }
      ]"
    />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import BaseFooter from '@/components/BaseFooter.vue'

export default {
  name: 'Home',
  components: {
    BaseFooter,
    HelloWorld
  }
}
</script>
