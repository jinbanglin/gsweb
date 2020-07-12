<template>
  <div>
    <div class="bg-white">
      <div class="container">
        <navbar />
      </div>
    </div>
    <nuxt />
  </div>
</template>

<script>
import Vue from 'vue'
import Navbar from '~/components/Navbar'

export default Vue.extend({
  components: {
    Navbar
  }
})
</script>
