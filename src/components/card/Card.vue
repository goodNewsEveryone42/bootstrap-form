<template>
  <div class="root-container">
    <div class="card" style="width: 18rem">
      <img class="card-img-top" :src="srcImage" alt="Card image cap" />
      <div class="card-body">
        <p class="card-text" :style="{ fontSize: fontSize + 'px' }">
          {{ title }}
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
</template>

<script>
export default {
  props: ["startValues"],

  data() {
    return {
      title: this.startValues.title,
      fontSize: this.startValues.fontSize,
      srcImage: this.startValues.srcImage,
    };
  },
};
</script>

<style lang="scss" scoped>
.root-container {
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