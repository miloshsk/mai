<template>
  <h1>
    <span v-for='title in titles' :key='title'>
      {{ title }}
    </span>
  </h1>
</template>

<script>
	export default {
		name: 'MainScreenCaption',
		data() {
			return {
				titles: ['Маи', 'Международная', 'ассоциация', 'инвесторов']
			};
		}
	}
</script>

<style scoped lang='sass'>
  h1
    margin: 100px 0 200px
    font-family: 'Cocogoose Compressed Trial', serif
    text-transform: uppercase
    color: #0c81fd
    font-size: 40px
    line-height: 50px
    span
      display: block
      &:first-child
        font-size: 175px
        line-height: 125px
        margin-bottom: 35px
      &:nth-child(2),
      &:nth-child(3)
        color: #222222
</style>