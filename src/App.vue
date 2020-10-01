<template>
  <div id="app" class="root">
    <div class="root__container">
      <div class="card" style="width: 18rem">
        <img
          class="card-img-top"
          src="https://cs5.pikabu.ru/post_img/big/2015/04/23/8/1429794583_343353562.png"
          alt="Card image cap"
        />
        <div class="card-body">
          <p class="card-text" :style="{ fontSize: fontSize + 'px' }">
            {{ titleUpper }}
          </p>
        </div>
      </div>
      <form>
        <div class="form-group">
          <label for="formGroupExampleInput">title</label>
          <input
            type="text"
            class="form-control"
            id="formGroupExampleInput"
            v-model="title"
          />
        </div>
        <div class="form-group">
          <label for="formGroupExampleInput2">font size</label>
          <input
            type="text"
            class="form-control"
            id="formGroupExampleInput2"
            v-model="fontSize"
          />
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      title: "MENU",
      fontSize: 16,
    };
  },
  computed: {
    titleUpper: function () {
      return this.title.toUpperCase();
    },
  },
};
</script>

<style lang="scss">
.root__container {
  display: flex;
  justify-content: space-between;
  width: 520px;
  margin: 0 auto;
  margin-top: 20%;
}
.card-body {
  display: flex;
  justify-content: center;
  text-transform: uppercase;
  font-weight: 600;
}
</style>
