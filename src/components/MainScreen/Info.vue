<template>
  <div class='request'>
    <p class='request__text'>Инвестиции в перспективные проекты.</p>
    <p class='request__text'>МАИ - крупнейшая инвестиционная организация восточной Европы.</p>
    <a href='#' class='btn request__btn'>Подать заявку</a>
    <p class='request__subtext'>Расскажите о вашем проекте
 и подайте заявку на инвестирование
    </p>
  </div>
</template>

<script>
	export default {
		name: 'Info'
	}
</script>

<style scoped lang='sass'>
  p
    font-family: 'Roboto Condensed' ,serif
  .request
    max-width: 540px
    width: 100%
    margin-top: 100px
    margin-right: 160px
    &__text
      font-size: 30px
      &:nth-child(2)
        margin-top: 20px
        margin-bottom: 60px
    &__btn
      max-width: 125px
      width: 100%
      padding: 20px
      color: #fff
      background-color: #0c81fd
      margin-bottom: 20px
    &__subtext
      font-size: 14px
      white-space: pre
</style>