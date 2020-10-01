<template>
  <div id="app" class="root">
    <Card :startValues="initialValues" />
  </div>
</template>

<script>
import Card from "./components/card";
export default {
  name: "App",
  components: {
    Card,
  },

  data() {
    return {
      initialValues: {
        title: "MENU",
        fontSize: 16,
        srcImage:
          "https://cs5.pikabu.ru/post_img/big/2015/04/23/8/1429794583_343353562.png",
      },
    };
  },
};
</script>

<style lang="scss">
</style>
