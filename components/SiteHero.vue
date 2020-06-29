/* eslint-disable vue/html-indent */
/* eslint-disable no-mixed-spaces-and-tabs */
/* eslint-disable */
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
        <h1 class="title animated fadeInUp">{{ title }}</h1>

        <h2 class="subtitle animated fadeInUp slower">{{ subtitle }}</h2>
        <!-- <br /> -->
        <div class="icon-container">
          <font-awesome-icon icon="low-vision" />
          <font-awesome-icon icon="deaf" />
          <font-awesome-icon icon="brain" />
          <font-awesome-icon icon="wheelchair" />
        </div>

        <!-- 
		// Subscribe button
		<div v-if="$slots.default" class="under-subtitle animated fadeInDown slower">
          <slot />
        </div> 
        -->
      </div>
    </div>

    <div class="reasons-container">
      <h2>What is Web Accessibility?</h2>
      <div class="title container reasons-container">
        <div class="columns">
          <div class="column">
            <h3
              class="title is-3"
            >It is the simple act of making sites and apps available to everyone, including those with disabilities.</h3>
          </div>
        </div>
      </div>

      <h2>Benefits Of Web Accessibility</h2>
      <div class="container">
        <!-- <p>We have created a fictional band website. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</p> -->

        <div class="columns is-centered" style="padding: 2rem">
          <div class="column">
            <div class="card">
              <span class="icon">
                <font-awesome-icon icon="users" />
              </span>
              <div class="card-content">
                <h3 class="has-text-centered">Increase Audience/Customer Base</h3>
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
              <span class="icon">
                <font-awesome-icon icon="dollar-sign" />
              </span>
              <div class="card-content">
                <h3 class="has-text-centered">Significant Financial Benefits</h3>
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
              <span class="icon">
                <font-awesome-icon icon="balance-scale" />
              </span>
              <div class="card-content">
                <h3 class="has-text-centered">Legally and Morally Right</h3>
                <div class="content">
                  <ul>
                    <li>Legal Requirement</li>
                    <li>Web Access is Basic Human Rights</li>
                    <li>Costly if Sued</li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
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
    width: 90%;
    margin: 0.75em auto;
    /* @media (min-width: 768px) {
        font-size: 3.2rem;
    } */
}
.subtitle,
.under-subtitle {
    padding: 0;
    margin: 0;
}
.subtitle {
    font-size: 1.5em;
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
.site-layout-width-contained {
    > div[id*='home'] {
        h1.title {
            // eslint-disable-next-line no-mixed-spaces-and-tabs
            display: none !important;
        }
        #hero-logo {
            display: block !important;
            margin: 0 auto 2.5em;
        }
    }
    > div:not([id*='home-']) {
        h1.title {
            // eslint-disable-next-line no-mixed-spaces-and-tabs
            display: block !important;
            /* margin: 0; */
        }
        #hero-logo {
            display: none !important;
        }
    }
}
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
            padding-top: 5rem;
            padding-bottom: 5rem;
            .container {
                .icon-container {
                    margin-top: 1em;
                    svg {
                        color: #396999;
                        height: 2.5em;
                        width: 2.5em;
                        margin: 0 2em;
                        vertical-align: bottom;
                    }
                }
            }
        }
    }
    &:not(.home-page) {
        .hero-body {
            padding: 2em 0;
            /* .subtitle {
                display: none;
			} */
            > .container {
                svg,
                h2.subtitle {
                    display: none;
                }
            }
        }
        .title.container {
            display: none;
        }
    }
}

.reasons-container {
    h2 {
        background-color: #0a3055;
        font-size: 2em;
        color: #fff;
        padding: 0.25em 0;
    }
    .container {
        p {
            padding: 1em;
        }
        .card {
            .icon {
                height: 1.5em;
                font-size: 4em;
                color: #396999;
                svg {
                    height: 50%;
                }
            }
            .card-content {
                padding: 0 0 1.5rem 0;
                h3 {
                    background-color: #0a3055;
                    color: #fff;
                    padding: 0.5em 0;
                }
                .content {
                    ul {
                        li {
                            text-align: left;
                        }
                    }
                }
            }
        }
    }
}

img#hero-logo {
    width: 55%;
}
</style>
