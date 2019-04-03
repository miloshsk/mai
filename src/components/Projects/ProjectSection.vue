<template>
  <div class='sub-container'>
    <appSubtitle :subtitle='this.subtitle'></appSubtitle>
    <appTitle :title='this.title'></appTitle>
  </div>
</template>

<script>
import SubTitle from '../SubTitle';
import Title from '../Title';
export default {
  name: 'ProjectSection',
  components: {
    appSubtitle: SubTitle,
    appTitle: Title
  },
  props: {
    title: String,
    subtitle: Object
  }
};
</script>

<style scoped></style>
