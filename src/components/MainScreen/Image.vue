<template>
  <div class="img">
    <div v-for="(column, id) in columnsCnt" :key="id" class="column">
      <span class="column__bg-before"></span>
      <span class="column__bg-after"></span>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainScreenImg",
  props: {
    showInfo: Boolean
  },
  data() {
    return {
      columnsCnt: 5
    };
  },
  methods: {
    imgAnimate() {
      const columnsBefore = document.querySelectorAll(".column__bg-before");
      const columnsAfter = document.querySelectorAll(".column__bg-after");
      columnsBefore.forEach(item => {
        item.classList.add("img-show");
      });
      setTimeout(() => {
        columnsAfter.forEach(item => {
          item.classList.add("img-hide");
        });
      }, 1000);
      setTimeout(() => {
        this.$emit("infoToggle", !this.showInfo);
      }, 2000);
    }
  },
  mounted() {
    setTimeout(this.imgAnimate, 500);
  }
};
</script>

<style scoped lang="sass">
.img
  width: 65%
  height: 505px
  background-size: 100%
  background: url('../../assets/img/bg.jpg') no-repeat 75% 60%
  display: flex
  position: absolute
  top: 0
  right: 0
.column
  width: 20%
  height: 100%
  position: relative
  z-index: 10
  &__bg-before
    position: absolute
    top: 0
    bottom: 0
    left: 0
    right: 0
    background-color: #fff
    transition: 0.7s ease
  &__bg-after
    position: absolute
    top: 0
    bottom: 0
    left: 0
    right: 100%
    background-color: #fff
    transition: 0.7s ease
  .img-show
    left: 100%
  .img-hide
    right: 0
</style>
