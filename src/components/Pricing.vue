<template>
  <div class="pricing">
    <h2>Our Pricing</h2>

    <div class="periodicity">
      <span>Anually</span>

      <div class="switch"
           v-bind:class="[periodicity]"
           v-on:click="togglePeriodicity()">
        <div class="indicator"></div>
      </div>

      <span>Monthly</span>
    </div>

    <div class="cards">
      <div class="card white">
        <div class="title">Basic</div>

        <div class="price">
          <div class="sign">$</div>
          <span class="amount">{{prices[periodicity].Basic}}</span>
        </div>

        <div class="attributes">
          <div class="attribute">500 GB Storage</div>
          <div class="attribute">2 Users Allowed</div>
          <div class="attribute">Send up to 3 GB</div>
        </div>

        <div class="button">Learn More</div>
      </div>

      <div class="card purple">
        <div class="title">Professional</div>

        <div class="price">
          <div class="sign">$</div>
          <span class="amount">{{prices[periodicity].Professional}}</span>
        </div>

        <div class="attributes">
          <div class="attribute">1 TB Storage</div>
          <div class="attribute">5 Users Allowed</div>
          <div class="attribute">Send up to 10 GB</div>
        </div>

        <div class="button">Learn More</div>
      </div>

      <div class="card white">
        <div class="title">Master</div>

        <div class="price">
          <div class="sign">$</div>
          <span class="amount">{{prices[periodicity].Master}}</span>
        </div>

        <div class="attributes">
          <div class="attribute">2 TB Storage</div>
          <div class="attribute">10 Users Allowed</div>
          <div class="attribute">Send up to 20 GB</div>
        </div>

        <div class="button">Learn More</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      periodicity: 'Monthly',
      prices: {
        Anually: {
          Basic: 16.79,
          Professional: 20.99,
          Master: 33.59
        },
        Monthly: {
          Basic: 19.99,
          Professional: 24.99,
          Master: 39.99
        }
      }
    }
  },
  methods: {
    togglePeriodicity () {
      if (this.periodicity === 'Monthly') {
        this.periodicity = 'Anually'
      } else {
        this.periodicity = 'Monthly'
      }
    }
  },
  name: 'Pricing'
}
</script>

<style lang="sass" scoped>
.pricing
  margin: 0 auto
  text-align: center

  h2
    font-size: 27px
    letter-spacing: 0.06
    margin: 35px 0 10px

  .periodicity
    > *
      display: inline-block
      margin-bottom: 54px
      vertical-align: top

    span
      line-height: 27px

    .switch
      background: var(--gradient)
      border-radius: 14px
      cursor: pointer
      height: 27px
      margin: 0 21px
      position: relative
      transition: all 0.3s
      width: 48px

      .indicator
        background: var(--white)
        border-radius: 50%
        height: 21px
        left: 24px
        position: absolute
        top: 3px
        transform: translate3d(0, 0, 0)
        transition: all 0.3s
        width: 21px

      &.Anually
        background: var(--white)

        .indicator
          background: var(--gradient)
          transform: translate3d(-24px, 0, 0)

  .cards
    margin: 0 auto
    width: 300px

    .card
      background: var(--white)
      box-shadow: 0 2px 9px rgba(0, 0, 0, 0.13)
      border-radius: 8px
      height: 387px
      margin: 18px 0
      position: relative
      vertical-align: top
      width: 300px

      &.purple
        background: var(--gradient)
        box-shadow: 0 2px 9px rgba(161, 165, 239, 0.13)
        color: var(--white)
        height: 423px
        margin: 0
        z-index: 1

        .title
          margin-top: 52px

        .button
          background: var(--white)
          color: #8185E5

      .title
        font-size: 15px
        letter-spacing: 0.04
        margin: 33px 0 24px

      .price
        line-height: 60px
        margin-bottom: 24px

        div
          display: inline-block

        .sign
          font-size: 36px
          line-height: 40px
          margin-top: 10px
          vertical-align: top

        .amount
          font-size: 60px

      .attributes
        .attribute
          border-top: 1px solid var(--border)
          height: 40px
          line-height: 40px
          margin-left: 24px
          width: calc(100% - 48px)

          &:last-child
            border-bottom: 1px solid var(--border)

      .button
        background: var(--gradient)
        border-radius: 4px
        color: var(--white)
        cursor: pointer
        height: 33px
        line-height: 33px
        margin: 38px 24px 0 24px
        width: calc(100% - 48px)

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
