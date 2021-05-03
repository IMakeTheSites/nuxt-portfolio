<template>
  <div class="container">
    <div>
      <h1 class="title">I Make the Sites</h1>
    </div>
    <span class="icons"
      ><font-awesome-icon :icon="['fab', 'fa-twitter-square']"
    /></span>
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
