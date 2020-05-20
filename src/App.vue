<template>
  <div id="app">
    <Pricing />
  </div>
</template>

<script>
import Pricing from './components/Pricing.vue'

export default {
  components: {
    Pricing: Pricing
  }
}
</script>

<style lang="sass">
html, body
  background: #F7F7FF
  margin: 0
  padding: 0
  --black: #5C5C74
  --border: #ECECEC
  --gradient: linear-gradient( 135deg, #A1A5EF, #6C70DE )
  --white: #FFF

#app
  color: var(--black)
</style>
