<script>
  export let alpaca;

  import nose from '../assets/alpaca/nose.png';
  import blue50 from '../assets/alpaca/backgrounds/blue50.png';
  import blue60 from '../assets/alpaca/backgrounds/blue60.png';
  import blue70 from '../assets/alpaca/backgrounds/blue70.png';
  import darkblue30 from '../assets/alpaca/backgrounds/darkblue30.png';
  import darkblue50 from '../assets/alpaca/backgrounds/darkblue50.png';
  import darkblue70 from '../assets/alpaca/backgrounds/darkblue70.png';
  import green50 from '../assets/alpaca/backgrounds/green50.png';
  import green60 from '../assets/alpaca/backgrounds/green60.png';
  import green70 from '../assets/alpaca/backgrounds/green70.png';
  import grey40 from '../assets/alpaca/backgrounds/grey40.png';
  import grey70 from '../assets/alpaca/backgrounds/grey70.png';
  import grey80 from '../assets/alpaca/backgrounds/grey80.png';
  import red50 from '../assets/alpaca/backgrounds/red50.png';
  import red60 from '../assets/alpaca/backgrounds/red60.png';
  import red70 from '../assets/alpaca/backgrounds/red70.png';
  import yellow50 from '../assets/alpaca/backgrounds/yellow50.png';
  import yellow60 from '../assets/alpaca/backgrounds/yellow60.png';
  import yellow70 from '../assets/alpaca/backgrounds/yellow70.png';

  import defaultNeck from '../assets/alpaca/neck/default.png';
  import bendBackward from '../assets/alpaca/neck/bend-backward.png';
  import bendForward from '../assets/alpaca/neck/bend-forward.png';
  import thick from '../assets/alpaca/neck/thick.png';

  import defaultEars from '../assets/alpaca/ears/default.png';
  import tiltBackwardEars from '../assets/alpaca/ears/tilt-backward.png';
  import tiltForwardEars from '../assets/alpaca/ears/tilt-forward.png';

  import defaultHair from '../assets/alpaca/hair/default.png';
  import bang from '../assets/alpaca/hair/bang.png';
  import curls from '../assets/alpaca/hair/curls.png';
  import elegant from '../assets/alpaca/hair/elegant.png';
  import fancy from '../assets/alpaca/hair/fancy.png';
  import quiff from '../assets/alpaca/hair/quiff.png';
  import short from '../assets/alpaca/hair/short.png';

  import defaultEyes from '../assets/alpaca/eyes/default.png';
  import angry from '../assets/alpaca/eyes/angry.png';
  import naughty from '../assets/alpaca/eyes/naughty.png';
  import panda from '../assets/alpaca/eyes/panda.png';
  import smart from '../assets/alpaca/eyes/smart.png';
  import star from '../assets/alpaca/eyes/star.png';

  import defaultLeg from '../assets/alpaca/leg/default.png';
  import bubbleTea from '../assets/alpaca/leg/bubble-tea.png';
  import cookie from '../assets/alpaca/leg/cookie.png';
  import gameConsole from '../assets/alpaca/leg/game-console.png';
  import tiltBackwardLeg from '../assets/alpaca/leg/tilt-backward.png';
  import tiltForwardLeg from '../assets/alpaca/leg/tilt-forward.png';

  import defaultMouth from '../assets/alpaca/mouth/default.png';
  import astonished from '../assets/alpaca/mouth/astonished.png';
  import eating from '../assets/alpaca/mouth/eating.png';
  import laugh from '../assets/alpaca/mouth/laugh.png';
  import tongue from '../assets/alpaca/mouth/tongue.png';

  import flower from '../assets/alpaca/accessories/flower.png';
  import earings from '../assets/alpaca/accessories/earings.png';
  import glasses from '../assets/alpaca/accessories/glasses.png';
  import headphone from '../assets/alpaca/accessories/headphone.png';

  let styles = {
    backgrounds: {
      blue50,
      blue60,
      blue70,
      darkblue30,
      darkblue50,
      darkblue70,
      green50,
      green60,
      green70,
      grey40,
      grey70,
      grey80,
      red50,
      red60,
      red70,
      yellow50,
      yellow60,
      yellow70,
    },
    neck: {
      default: defaultNeck,
      'bend-backward': bendBackward,
      'bend-forward': bendForward,
      thick,
    },
    ears: {
      default: defaultEars,
      'tilt-backward': tiltBackwardEars,
      'tilt-forward': tiltForwardEars,
    },
    hair: { default: defaultHair, bang, curls, elegant, fancy, quiff, short },
    eyes: { default: defaultEyes, angry, naughty, panda, smart, star },
    leg: {
      default: defaultLeg,
      'bubble-tea': bubbleTea,
      cookie,
      'game-console': gameConsole,
      'tilt-backward': tiltBackwardLeg,
      'tilt-forward': tiltForwardLeg,
    },
    mouth: { default: defaultMouth, astonished, eating, laugh, tongue },
    accessories: { flower, earings, glasses, headphone },
  };
</script>

<div class="alpaca-img">
  <img
    src={styles.backgrounds[alpaca.backgrounds]}
    alt="Background of the alpaca ({alpaca.backgrounds})"
  />
  <img
    src={styles.ears[alpaca.ears]}
    alt="Ears of the alpaca ({alpaca.ears})"
  />
  <img
    src={styles.neck[alpaca.neck]}
    alt="Neck of the alpaca ({alpaca.neck})"
  />
  <img src={nose} alt="Nose of the alpaca" />
  <img
    src={styles.hair[alpaca.hair]}
    alt="Hair of the alpaca ({alpaca.hair})"
  />
  <img
    src={styles.eyes[alpaca.eyes]}
    alt="Eyes of the alpaca ({alpaca.eyes})"
  />
  <img src={styles.leg[alpaca.leg]} alt="Leg of the alpaca ({alpaca.leg})" />
  <img
    src={styles.mouth[alpaca.mouth]}
    alt="Mouth of the alpaca ({alpaca.mouth})"
  />
  <img
    src={styles.accessories[alpaca.accessories]}
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
