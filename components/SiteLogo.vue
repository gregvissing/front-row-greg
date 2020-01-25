<template>
  <div class="logo-wrapper">
    <div class="logo-inner">
      <!-- <h1>navbar-brand</h1> -->
      <img 
        alt="Front Row Greg logo"
        src="https://github.com/gregvissing/images-for-website/blob/master/front-row-greg-logo.png?raw=true"
      >
    </div>
</template>
<script>
export default {
    name: 'SiteLogo',
    data() {
        return {
            frames: 5,
            currentFrame: 1,
            blinking: false //true
        }
    },
    mounted() {
        // setInterval(() => {
        //     const rand = Math.ceil(Math.random() * 10)
        //     this.blinking = rand % 2
        // }, 1000)
    }
}
</script>
<style lang="scss">
@keyframes logoBlink {
    100% {
        transform: translateY(-360px);
    }
}
.logo-wrapper {
    position: relative;
    height: 50px;
    overflow: hidden;
    width: 300px;
    .logo-inner {
        position: absolute;
        height: 500px;
        img {
            display: block;
            height: 40px;
            margin: 5px;
            max-height: initial;
        }
        &.blink {
            animation: logoBlink 0.2s steps(8, end) alternate;
        }
        h1 {
            font-size: 2em !important;
            color: #0a3055;
        }
    }
}
</style>
