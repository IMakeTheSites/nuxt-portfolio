<template>
  <div>
    <h1>About I Make the Sites</h1>
    <h3>BIO</h3>
    <b-card no-body class="overflow-hidden" style="max-width: 900px">
      <b-row no-gutters>
        <b-col md="6">
          <b-card-img
            src="~/assets/profile.jpg"
            alt="Mark"
            class="rounded-0"
          ></b-card-img
        ></b-col>
        <b-col md="6">
          <b-card-body title="History of Mark">
            <b-card-text>
              I am very passionate about each of my projects and my objective is
              to create compelling software products that users will love! I am
              eager to develop attractive, functional, and mobile-friendly
              websites, web apps and mobile apps using current and cutting edge
              technology and code for you and your organization. After finishing
              my International MBA at the University of Memphis in 2011, I moved
              to China to teach English and look for international trade
              opportunities. Shortly after that, I began teaching myself web
              development. I started with HTML and CSS, then moved on to PHP,
              MySQL, JavaScript, and JavaScript frameworks like React.
              <br />
              These past few years as a mostly freelance developer specializing
              in frontend development have taught me much, and I am eager to use
              what I have learned to help you and your company by streamlining
              your online operations and improving your development through
              implementation of best practices and asset optimization.
            </b-card-text>
          </b-card-body>
        </b-col>
      </b-row>
    </b-card>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'About IMTS',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Mark makes the sites',
        },
      ],
    }
  },
}
</script>

<style></style>
