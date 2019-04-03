<template>
  <header class='page-header container'>
    <appLogo></appLogo>
    <appHeaderNav></appHeaderNav>
    <appHeaderControls></appHeaderControls>
  </header>
</template>

<script>
	import Logo from './Logo.vue';
  import HeaderNav from './Nav';
  import HeaderControls from './Controls';
	export default {
		name: 'PageHeader',
    components: {
			appLogo: Logo,
			appHeaderNav: HeaderNav,
      appHeaderControls: HeaderControls
    }
	}
</script>

<style scoped lang='sass'>
  .page-header
    display: flex
    font-family: 'FavoritCondC',serif
    padding-left: 160px
    position: relative
</style>