<template>
  <footer>
    <hr>
    <p>Copyright {{ getYear }} from footer</p>
  </footer>
</template>

<script>
export default {
  computed: {
    getYear () {
      function addZero (num) {
        if (String(num).length < 2) {
          return '0' + num;
        } else {
          return num;
        }
      }

      const date = addZero(new Date().getDate());
      const month = addZero(new Date().getMonth());
      const year = addZero(new Date().getFullYear());
      return `${date}/${month}/${year}`;
    }
  }
}
</script>

<style scoped>

</style>
