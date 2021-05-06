<template>
  <div class="container">
    <b-jumbotron
      header="I Make the Sites"
      lead="My brand new Nuxt.js portfolio and blog"
    ></b-jumbotron>
    <b-button href="https://twitter.com/imakethesites"
      ><font-awesome-icon
        :icon="{ prefix: 'fab', iconName: 'twitter' }"
        style="color: #fff; font-size: 50px"
    /></b-button>
    <b-button href="https://www.linkedin.com/in/gowiththewlo/"
      ><font-awesome-icon
        :icon="{ prefix: 'fab', iconName: 'linkedin' }"
        style="color: #fff; font-size: 50px"
    /></b-button>
    <b-button href="https://www.facebook.com/imakethesites"
      ><font-awesome-icon
        :icon="{ prefix: 'fab', iconName: 'facebook' }"
        style="color: #fff; font-size: 50px"
    /></b-button>
    <b-button href="https://github.com/IMakeTheSites"
      ><font-awesome-icon
        :icon="{ prefix: 'fab', iconName: 'github' }"
        style="color: #fff; font-size: 50px"
    /></b-button>
    <!-- <span class="icons"
      ><font-awesome-icon :icon="['fab', 'fa-twitter-square']"
    /></span> -->
  </div>
</template>

<script lang="ts">
export default {
  head() {
    return {
      title: 'I Make the Sites',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Best place for a new site or mobile app',
        },
      ],
    }
  },
}
</script>
<style>
.icons {
  margin-top: 1rem;
  padding: 0.4rem;
}
.icons a:hover {
  color: #eece1a;
  transition: all 0.5s ease-out;
}
</style>
