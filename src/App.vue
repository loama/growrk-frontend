<template>
  <div id="app">
    <Pricing />
    <img class="background left" src="./assets/background_left.svg">
    <img class="background right" src="./assets/background_top_right.svg">
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
@font-face
  font-family: 'HomepageBaukasten-Book'
  src: url('./assets/HomepageBaukasten-Book.otf')

@font-face
  font-family: 'HomepageBaukasten-Bold'
  src: url('./assets/HomepageBaukasten-Bold.otf')

html, body
  background: #F7F7FF
  font-family: 'HomepageBaukasten-Book'
  margin: 0
  padding: 0
  --black: #5C5C74
  --border: #ECECEC
  --gradient: linear-gradient( 135deg, #A1A5EF, #6C70DE )
  --white: #FFF

#app
  color: var(--black)

  .background
    position: absolute

    &.left
      bottom: 0
      left: 0

    &.right
      right: 0
      top: 0
</style>
