/* eslint-disable */
<template>
  <div id="resources-page" class="page-wrapper resources-page content-page">
    <site-hero
      title="Resources"
      subtitle="Bookmarks for Days"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>A11Y - Standards</h3>
          <p>
            <ul>
              <li><a href="https://www.w3.org/WAI/standards-guidelines/">W3C Accessibility Standards Overview</a></li>
              <li><a href="https://www.w3.org/TR/WCAG20/">Web Content Accessibility Guidelines (WCAG) 2.0</a></li>
            </ul>
          </p>
          <h3>A11Y - How-To</h3>
          <p>
            <ul>
              <li><a href="https://www.creativebloq.com/advice/14-easy-ways-to-make-your-website-more-accessible">14 easy ways to make your website more accessible</a></li> 
              <li><a href="https://labs.clio.com/a11y-at-clio-how-we-build-accessible-ui-web-components-b31d8e1fef23">A11y at Clio: How We Build Accessible UI Web Components</a></li>
            </ul>
          </p>
          <h3>A11Y - Strategy</h3>
          <p>
            <ul>
              <li><a href="https://www.oho.com/blog/ada-website-compliance-preparing-your-college-or-university-website">ADA Website Compliance: Preparing Your College or University Website</a></li>
              <li><a href="https://opensenselabs.com/blog/articles/checklist-comply-ada-accessibility-higher-education">Checklist to Comply with ADA Accessibility in Higher Education</a></li>
              <li><a href="https://www.adaactionguide.org/action-steps">ADA Title II Action Guide for State and Local Governments</a></li>
              <li><a href="https://medium.com/myplanet-musings/making-the-web-more-accessible-using-machine-learning-8a32eaafdb3a">Making the Web More Accessible Using Machine Learning</a></li>
            </ul>
          </p>
          <h3>A11Y - Policy Example</h3>
          <p>
            <ul>
              <li><a href="https://usability.yale.edu/web-accessibility/accessibility-yale">Accessibility at Yale</a></li>
            </ul>
          </p>
          <h3>A11Y - Tools</h3>
          <p>
            <ul>
              <li><a href="https://marcozehe.de/2018/04/11/introducing-the-accessibility-inspector-in-the-firefox-developer-tools/">Accessibility Inspector (Firefox)</a></li>
            </ul>
          </p>
          <h3>A11Y - Forms</h3>
          <p>
            <ul>
              <li><a href="https://marcozehe.de/2018/04/11/introducing-the-accessibility-inspector-in-the-firefox-developer-tools/">Accessibility Inspector (Firefox)</a></li>
            </ul>
          </p>
          <!-- <quote-card /> -->
          <h3>A11Y - Testing</h3>
          <p>
            <ul>
              <li><a href="https://marcozehe.de/2018/04/11/introducing-the-accessibility-inspector-in-the-firefox-developer-tools/">Accessibility Inspector (Firefox)</a></li>
            </ul>
          </p>
          <h3>A11Y - Legal</h3>
          <p>
            <ul>
              <li><a href="https://www.d.umn.edu/~lcarlson/atteam/lawsuits.html">Higher Ed Accessibility Lawsuits, Complaints, and Settlements</a></li>
              <li><a href="https://www.insidehighered.com/news/2018/11/06/universities-still-struggle-make-websites-accessible-all">Feds Prod Universities to Address Website Accessibility Complaints</a></li>
            </ul>
          </p>
          <h3>A11Y - Influencers</h3>
          <p>
            <ul>
              <li><a href="https://www.kpodnar.com/">Kristina Podnar</a></li>
            </ul>
          </p>
        </div>

        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Cool Stuff We Do
              </p>
              <p class="subtitle">
                Sooo Cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Other Cool Things
              </p>
              <p class="subtitle">
                Just as cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                All the cool
              </p>
              <p class="subtitle">
                that is all
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
        </div>
      </template>

      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
// import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `Resources | ${this.$siteConfig.siteName}`
    }
  },
//   components: { QuoteCard }
}
</script>
