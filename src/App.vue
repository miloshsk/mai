<template>
  <div id='app'>
    <appToggleMenu></appToggleMenu>
    <appHeader></appHeader>
    <appPhoneButton></appPhoneButton>
    <appMainScreen></appMainScreen>
    <appProjectSection
      :title='titles[0]'
      :subtitle='subtitles[0]'
    ></appProjectSection>
  </div>
</template>

<script>
import PageHeader from './components/Header/Header.vue';
import ToggleMenu from './components/ToggleMenu.vue';
import PhoneButton from './components/PhoneButton.vue';
import MainScreen from './components/MainScreen/MainScreen';
import ProjectSection from './components/Projects/ProjectSection';

export default {
  name: 'app',
  components: {
    appHeader: PageHeader,
    appToggleMenu: ToggleMenu,
    appPhoneButton: PhoneButton,
    appMainScreen: MainScreen,
    appProjectSection: ProjectSection
  },
  data() {
    return {
      titles: [
        'Рассматриваем проекты',
        'Основные показатели',
        'Наши преимущества'
      ],
      subtitles: [
        {ind: '01', caption: 'Проекты'},
        {ind: '02', caption: 'Показатели'},
        {ind: '03', caption: 'Преимущества'}
      ]
    };
  }
};
</script>

<style lang='sass'>
@import './stylesheet'
@import './buttons'
*
  box-sizing: border-box
ul
  padding: 0
  margin: 0
  list-style-type: none
a
  text-decoration: none
p
  margin: 0
.container
  max-width: 1400px
  width: 100%
  margin: 0 auto
.sub-container
  max-width: 1075px
  width: 100%
  margin: 0 auto
</style>
