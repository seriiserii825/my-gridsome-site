<template>
  <div class="layout">
    <header class="header">
      <strong>
        <g-link to="/">{{ $static.metadata.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" exact to="/">Home</g-link>
        <g-link class="nav__link" exact to="/about/">About</g-link>
        <g-link class="nav__link" to="/products/">Products</g-link>
        <g-link class="nav__link" to="/new-products/">New products</g-link>
        <g-link class="nav__link" to="/new/product/">New product</g-link>
        <g-link class="nav__link" to="/new/">Index new</g-link>
      </nav>
    </header>
    <slot/>
    <Footer></Footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>
<script>
import Footer from "../components/Footer";

export default {
  components: {
    Footer
  }
}
</script>

<style>
body {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.nav__link {
  margin-left: 20px;
}
.active {
  color: red;
}
</style>
