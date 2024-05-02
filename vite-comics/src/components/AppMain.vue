<script>
export default {
  data() {
    return {};
  },
};
</script>

<template>
  <main>
    <div class="container">
      <h1>-->Content Here<--</h1>
    </div>
  </main>
</template>

<style scoped lang="scss">
@use "./style/partials/variables" as *;
@use "./style/partials/mixins" as *;

main {
  background-color: $main-color;
  padding: 60px 0;

  h1 {
    font-size: 35px;
  }
}
</style>
