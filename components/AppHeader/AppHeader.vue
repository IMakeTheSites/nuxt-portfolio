<template>
  <div>
    <b-navbar toggleable="md" type="dark" variant="warning">
      <b-navbar-brand to="/">I Make the Sites</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item to="/work">Work</b-nav-item>
          <b-nav-item to="/about">About</b-nav-item>
          <b-nav-item to="/blog">Blog</b-nav-item>
          <b-nav-item to="/contact">Contact</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'AppHeader',
}
</script>

<style></style>
