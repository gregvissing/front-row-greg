/* eslint-disable */
<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero title="About Me" subtitle="Example About Page" image="/uploads/about-hero.jpg"></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h2>Hello, welcome to my website about Web Accessibility!</h2>

          <h3>About the Nickname "Front Row Greg"</h3>
          <p>
            It all started in 2019 while attending
            <a
              href="https://smashingconf.com/toronto-2019/"
            >SmashingConf</a> up in Toronto, Canada. Click the link to learn more about this great conference! I was excited about the lineup of speakers, but I was particularly interested in the talk regarding
            <a
              href="https://vimeo.com/348952186"
            >Digital Policy</a> by Kristina Podnar. I went to the
            <a href="https://smashingconf.com/toronto-2019/jam-session">Jam Session</a> meet-up the night before the first day of talks.
          </p>

          <h3>Background</h3>

          <p>My name is Greg Vissing and I'm from Cincinnati, OH. I'm currently a Web Developer & UI Designer at the University of Cincinnati Foundation. I specialize in custom Web Development. My focus when developing a project is to make it as user friendly as possible no matter what device it is being viewed on. My attention to detail when creating training documents will allow clients to update their website with ease.</p>

          <h3>Skills</h3>
          <ol>
            <li>HTML5/HTML</li>
            <li>CSS3/CSS</li>
            <li>JavaScript</li>
            <li>jQuery</li>
            <li>VueJS</li>
            <li>WordPress</li>
            <li>Animations using Greensock</li>
            <li>PHP</li>
            <li>Bootstrap</li>
            <li>Foundation</li>
            <li>LESS/SASS</li>
          </ol>
          <h3>Work</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci
            eligendi impedit inventore ipsa laboriosam libero magnam modi odio,
            sunt temporibus. Distinctio doloremque eum magni nostrum quasi
            ratione rem repudiandae sit!
          </p>
          <h3>Job History</h3>
          <p>
            <strong>Employer:</strong> University of Cincinnati Foundation
          </p>
          <p>
            <strong>Title:</strong> Web Developer & UI Designer
          </p>
          <p>As a member of the digital communications team, I provide custom solutions to client needs across the Foundation. The Web Developer and UI Designer should speak both the business and technical languages fluently, and be passionate about hands-on technical configuration, creative problem solving and mentoring. While the primary focus of the position will be public-facing content on foundation.uc.edu and alumni.uc.edu, the Web Developer and UI Designer will need to develop a strong working understanding of how the fundraising database (Blackbaud CRM) integrates with the website in order to develop custom online parts.</p>
        </div>

        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <!-- <p class="title">Cool Stuff We Do</p>
              <p class="subtitle">Sooo Cool</p>-->
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <!-- <p class="title">Other Cool Things</p>
              <p class="subtitle">Just as cool</p>-->
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <!-- <p class="title">All the cool</p>
              <p class="subtitle">that is all</p>-->
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
        </div>
      </template>

      <template v-slot:sidebar>
        <h3 class="subtitle is-4">Latest Posts</h3>
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
            title: `About | ${this.$siteConfig.siteName}`
        }
    }
    // components: { QuoteCard }
}
</script>
