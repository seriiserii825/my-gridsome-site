<template>
  <Layout>
    <h1>About us</h1>
    <p>{{ $static.metadata.siteDescription }}</p>
  </Layout>
</template>

<static-query>
{ metadata { siteDescription } }
</static-query>

<script>
export default {
  metaInfo: {
    title: 'About us'
  }
}
</script>
