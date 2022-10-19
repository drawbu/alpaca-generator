<script>
  export let alpaca;
</script>

<div class="alpaca-img">
  <img
    src="src/assets/alpaca/backgrounds/{alpaca.backgrounds}.png"
    alt="Background of the alpaca ({alpaca.backgrounds})"
  />
  <img
    src="src/assets/alpaca/ears/{alpaca.ears}.png"
    alt="Ears of the alpaca ({alpaca.ears})"
  />
  <img
    src="src/assets/alpaca/neck/{alpaca.neck}.png"
    alt="Neck of the alpaca ({alpaca.neck})"
  />
  <img src="src/assets/alpaca/nose.png" alt="Nose of the alpaca" />
  <img
    src="src/assets/alpaca/hair/{alpaca.hair}.png"
    alt="Hair of the alpaca ({alpaca.hair})"
  />
  <img
    src="src/assets/alpaca/eyes/{alpaca.eyes}.png"
    alt="Eyes of the alpaca ({alpaca.eyes})"
  />
  <img
    src="src/assets/alpaca/leg/{alpaca.leg}.png"
    alt="Leg of the alpaca ({alpaca.leg})"
  />
  <img
    src="src/assets/alpaca/mouth/{alpaca.mouth}.png"
    alt="Mouth of the alpaca ({alpaca.mouth})"
  />
  <img
    src="src/assets/alpaca/accessories/{alpaca.accessories}.png"
    alt="Accessories of the alpaca ({alpaca.accessories})"
  />
</div>

<style lang="scss">
  .alpaca-img {
    width: 400px;
    height: 400px;
    position: relative;
    border-radius: 32px;
    border: 10px solid transparent;

    &:hover {
      border-color: #ffffff;

      @media (prefers-color-scheme: light) {
        border-color: #213547;
      }
    }

    img {
      width: 400px;
      position: absolute;
      left: 0;
      border-radius: 20px;
    }
  }
</style>
