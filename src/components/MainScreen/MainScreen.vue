<template>
  <div class='main-screen container'>
    <appCaption></appCaption>
    <appImage
      v-if='!showInfo'
      :showInfo='showInfo'
      @infoToggle='infoToggle'
    ></appImage>
    <appInfo v-else></appInfo>
  </div>
</template>

<script>
import Caption from './Caption';
import Image from './Image';
import Info from './Info';
export default {
  name: 'MainScreen',
  components: {
    appCaption: Caption,
    appImage: Image,
    appInfo: Info
  },
  data() {
    return {
      showInfo: false
    };
  },
  methods: {
    infoToggle(newShowInfo) {
      this.showInfo = newShowInfo;
    }
  }
};
</script>

<style scoped lang='sass'>
  .main-screen
    display: flex
    justify-content: space-between
    position: relative
    padding-left: 150px
</style>
