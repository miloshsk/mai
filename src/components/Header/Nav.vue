<template>
  <nav class='header-nav'>
    <ul class='header-nav__list'>
      <li v-for='link in links' :key='link.title'>
        <a
          href='#'
          class='header-nav__link'
          :class='{ "header-nav__link-active": link.isActive }'
          >{{ link.title }}</a
        >
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'PageNav',
  data() {
    return {
      links: [
        { title: 'Главная', isActive: true },
        { title: 'О нас', isActive: false },
        { title: 'Как получить инвестиции', isActive: false },
        { title: 'Инвесторам', isActive: false },
        { title: 'Статус проектов', isActive: false },
        { title: 'Контакты', isActive: false }
      ]
    };
  }
};
</script>

<style scoped lang='sass'>
.header-nav
  max-width: 1075px
  width: 100%
  font-size: 14px
  &__list
    display: flex
    li
      max-width: 180px
      width: 100%
  &__link
    display: block
    padding: 35px 50px 35px 0
    position: relative
    color: #222222
    text-transform: uppercase
    &:after
      content: ''
      display: block
      opacity: 0
      position: absolute
      left: 0
      right: 0
      top: 0
      height: 8px
      background-color:  #222222
      transition: 0.3s ease
    &:hover
      &:after
        opacity: 1
  &__link-active
    &:after
      opacity: 1
</style>
