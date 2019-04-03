<template>
  <p class='subtitle'>
    <span class='subtitle__number'>{{subtitle.ind}}</span>
    <span class='subtitle__text'>{{ subtitle.caption }}</span>
  </p>
</template>

<script>
export default {
  name: 'SubTitle',
  props: {
    subtitle: Object
  }
};
</script>

<style scoped lang='sass'>
.subtitle
  font-size: 14px
  text-transform: uppercase
  font-family: 'FavoritCondC', serif
  color: #222222
  position: relative
  transition: 0.3s ease
  &__number
    padding-right: 40px
    color: #0c81fd
    &:after
      content: ''
      display: block
      position: absolute
      left: 20px
      top: 50%
      transform: translateY(-50%)
      width: 25px
      height: 2px
      background-color: #222222
</style>
