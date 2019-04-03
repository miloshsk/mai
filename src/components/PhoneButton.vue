<template>
  <button class='btn phone'>{{number}}</button>
</template>

<script>
	export default {
		name: 'PhoneButton',
    data() {
			return {
				number: '8 (800) 777-77-77'
      }
    }
	}
</script>

<style scoped lang='sass'>
  .phone
    max-width: 135px
    width: 100%
    position: fixed
    top: 230px
    left: 0
    background-color: #222222
    color: #fff
    border: 1px solid #222222
    font-family: 'FavoritCondC', serif
</style>