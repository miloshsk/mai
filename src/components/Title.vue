<template>
  <h2>
    {{title}}
  </h2>
</template>

<script>
	export default {
		name: 'Caption',
    props: {
			title: String
    }
	}
</script>

<style scoped lang='sass'>
  h2
    font-size: 45px
    text-transform: uppercase
    font-family: 'Cocogoose Compressed Trial', serif
    color: #0c81fd
    span
      display: block
      color: #222222
</style>