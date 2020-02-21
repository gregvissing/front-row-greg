<template>
  <section :class="`hero is-medium hero-theme-${computedTheme}`">
    <!-- <img
      class="hero-bg-img"
      :src="responsiveImage.src"
      :lazy="false"
      :srcset="responsiveImage.srcSet"
    />-->
    <img class="hero-bg-img" />
    <div class="hero-body">
      <div class="container">
        <img
          id="hero-logo"
          alt="Front Row Greg logo"
          src="https://github.com/gregvissing/images-for-website/blob/master/front-row-greg-logo.png?raw=true"
        />
        <!-- <h1 class="title animated fadeInUp">{{ title }}</!-->

        <h2 class="subtitle animated fadeInUp slower">
          {{ subtitle }}
        </h2>
        <br />
        <div v-if="$slots.default" class="under-subtitle animated fadeInDown slower">
          <slot />
        </div>
      </div>
    </div>
    <div class="reasons-container">
      <h2>
        Reasons For Web Accessibility
      </h2>
      <div class="container">  
        <p>
          We have created a fictional band website. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.
        </p>

        <div class="columns is-centered" style="padding: 2rem">
          <div class="column">
            <div class="card">
              <div class="card-image">
                <figure class="image is-2by1">
                  <img src="https://images.pexels.com/photos/167635/pexels-photo-167635.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940" alt="Placeholder image">
                </figure>
              </div>
              <div class="card-content">
                <div class="media">
                  <div class="media-content">
                    <h3 class="has-text-centered">
                      Increase Audience/Customer Base
                    </h3>
                  </div>
                </div>
                <div class="content">
                  <ul>
                    <li>Neurological/Behavioral/Mental disorders</li>
                    <li>Simple navigation and link titles</li>
                    <li>Text-to-speech software</li>
                  </ul>
                </div>
              </div>
            </div>
		</div>
		<div class="column">
            <div class="card">
              <div class="card-image">
                <figure class="image is-2by1">
                  <img src="https://images.pexels.com/photos/167635/pexels-photo-167635.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940" alt="Placeholder image">
                </figure>
              </div>
              <div class="card-content">
                <div class="media">
                  <div class="media-content">
                    <h3 class="has-text-centered">
                      Significant Financial Benefits
                    </h3>
                  </div>
                </div>
                <div class="content">
                  <ul>
                    <li>Neurological/Behavioral/Mental disorders</li>
                    <li>Simple navigation and link titles</li>
                    <li>Text-to-speech software</li>
                  </ul>
                </div>
              </div>
            </div>
		</div>
		<div class="column">
            <div class="card">
              <div class="card-image">
                <figure class="image is-2by1">
                  <img src="https://images.pexels.com/photos/167635/pexels-photo-167635.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940" alt="Placeholder image">
                </figure>
              </div>
              <div class="card-content">
                <div class="media">
                  <div class="media-content">
                    <h3 class="has-text-centered">
                      Legally and Morally Right
                    </h3>
                  </div>
                </div>
                <div class="content">
                  <ul>
                    <li>Neurological/Behavioral/Mental disorders</li>
                    <li>Simple navigation and link titles</li>
                    <li>Text-to-speech software</li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="columns">
      <div class="column">
        <h3>Increase Audience/Customer Base</h3>
        <ul>
          <li>Neurological/Behavioral/Mental disorders</li>
          <li>Simple navigation and link titles</li>
          <li>Text-to-speech software</li>
        </ul>
      </div>
      <div class="column">
        <h3>Significan Financial Benefits</h3>
        <ul>
          <li>Range from arthritis and carpal tunnel</li>
          <li>Paralysis/Missing Limbs</li>
          <li>Head pointer/Mouth stick</li>
        </ul>
      </div>
      <div class="column">
        <h3>Legally and Morally Right</h3>
        <ul>
          <li>Low Vision</li>
          <li>Color blindness/Blindness</li>
          <li>Rely on tools to navigate web</li>
        </ul>
      </div>
    </div>
    </div>
  </section>
</template>
<script>
export default {
    name: 'SiteHero',
    props: {
        title: { type: String, default: '' },
        subtitle: { type: String, default: '' },
        image: { type: String, default: '' },
        color: { type: String, default: '#469af0' },
        theme: { type: String, default: '' }
    },
    computed: {
        // responsiveImage() {
        //     if (this.image.indexOf('/uploads') === 0) {
        //         return require(`~/assets${this.image}`)
        //     }
        //     return { src: this.image, srcSet: '' }
        // },
        computedTheme() {
            if (this.theme === '' && this.$siteConfig.hero.theme) {
                return this.$siteConfig.hero.theme
            }
            return this.theme || 'mist'
        }
    }
}
</script>

<style lang="scss" scoped>
.hero {
    margin-top: 52px;
    background-size: cover !important;
    background-position: center;
    text-align: center;
    overflow: hidden;
    position: relative;
}

.title {
    font-weight: 300;
    @media (min-width: 768px) {
        font-size: 3.2rem;
    }
}
.subtitle,
.under-subtitle {
    padding: 0;
    margin: 0;
}
.subtitle {
    font-size: 1rem;
    margin-bottom: 0 !important;
}
.under-subtitle {
    display: inline-block;
    font-size: 0.8rem;
    border-top: 2px solid $primary;
    padding-top: 5px;
}
.opti-image {
    opacity: 0;
}
.opti-image-loaded {
    opacity: 0.12;
    animation: blurIn 4.5s ease;
}
</style>
<style lang="scss">
.hero {
    .hero-bg-img {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        object-fit: cover;
        width: 100%;
        height: 100%;
    }
    .opti-image {
        opacity: 0;
    }
    .opti-image-loaded {
        opacity: 1;
    }
}
.hero-theme-mist {
    .hero-bg-img {
        filter: grayscale(1);
    }
    .opti-image-loaded {
        opacity: 0.12;
        animation: blurInGrayscale 4.5s ease;
    }
}
.hero-theme-dark,
.hero-theme-light {
    /* &.hero:after {
        content: '';
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background: rgba(0, 0, 0, 0.65);
        position: absolute;
    } */
    .hero-body {
        position: relative;
        z-index: 2;
    }
}
.hero-theme-dark {
    .title,
    .subtitle,
    .under-subtitle,
    .under-subtitle strong {
        color: #0a3055;
        /* color: white; */
    }
}
.hero-theme-light.hero {
    &:after {
        background: rgba(255, 255, 255, 0.6);
    }
    .title,
    .subtitle,
    .under-subtitle,
    .under-subtitle strong {
        text-shadow: 1px 1px 2px white;
    }
}

#post-page {
    .hero-body {
        padding-bottom: 3rem;
        padding-top: 3rem;
    }
}

.page-wrapper {
	&.home-page {
		.hero-body {
			padding-top: 7rem;
			padding-bottom: 5rem;
		}
	}
	&:not(.home-page) {
		.hero-body {
			padding: 3em 0 2em;
			.subtitle {
				display: none;
			}
		}
	}
}

.reasons-container {
	h2 {
		background-color: #0a3055;
		font-size: 2em;
		color: #fff;
	}
	.container {
		p {
			padding: 1em;
		}
	}
}

img#hero-logo {
    width: 55%;
}
</style>
