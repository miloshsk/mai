<template>
  <ul class='toggle-list'>
    <li v-for='link in links' :key='link.title'>
      <a
        href='#'
        class='toggle-list__link'
        :class='{ "toggle-list__link-active": link.isActive }'
        >{{ link.title }}</a
      >
    </li>
  </ul>
</template>

<script>
export default {
  name: 'ToggleList',
  data() {
    return {
      links: [
        { title: 'Проекты', isActive: true },
        { title: 'Показатели', isActive: false },
        { title: 'Преимущества', isActive: false },
        { title: 'Новости', isActive: false }
      ]
    };
  }
};
</script>

<style scoped lang='sass'>
.toggle-list
  position: fixed
  z-index: 10
  top: 575px
  left: 10px
  font-size: 14px
  text-transform: uppercase
  font-family: 'FavoritCondC', serif
  &__link
    color: #b3b3b3
    position: relative
    transition: 0.3s ease
    &:before
      content: ''
      display: block
      position: absolute
      left: -10px
      top: 50%
      transform: translateY(-50%)
      width: 5px
      height: 2px
      background-color: #b3b3b3
    &:hover
      color: #222222
      &:before
        background-color: #222222
    &-active
      color: #222222
      &:before
        background-color: #222222
</style>
