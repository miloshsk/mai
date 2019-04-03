<template>
  <ul class='header-controls'>
    <li><a href='#' class='btn btn-request'>Заявка на инвестиции</a></li>
    <li><a href='#' class='btn btn-login'>Вход</a></li>
  </ul>
</template>

<script>
	export default {
		name: 'HeaderControls'
	}
</script>

<style scoped lang='sass'>
  .header-controls
    flex-grow: 1
    margin-top: 15px
  .btn
    &-request
      background-color: #0c81fd
      color: #fff
      max-width: 160px
      width: 100%
      margin-bottom: 5px
    &-login
      background-color: #ebebeb
      color: #222222
      max-width: 70px
      width: 100%
</style>