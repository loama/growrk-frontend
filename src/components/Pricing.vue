<template>
  <div class="pricing">
    <div class="cards">
      <div class="card white"></div>

      <div class="card purple"></div>

      <div class="card white"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style lang="sass" scoped>
.pricing
  margin: 0 auto
  text-align: center

  .cards
    margin: 0 auto
    width: 300px

    .card
      background: #FFF
      box-shadow: 0 2px 9px rgba(0, 0, 0, 0.13)
      border-radius: 8px
      height: 387px
      margin: 18px 0
      position: relative
      vertical-align: top
      width: 300px

      &.purple
        background: linear-gradient( 135deg, #A1A5EF, #6C70DE )
        height: 423px
        margin: 0
        z-index: 1

@media (min-width: 1024px)
  .pricing
    .cards
      width: unset

      .card
        display: inline-block

        &:first-child
          margin-right: -8px

        &:last-child
          margin-left: -8px

</style>
