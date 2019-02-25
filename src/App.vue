<template>
  <div id="app">
    <Timetable/>
  </div>
</template>

<script>
import Timetable from './components/Timetable.vue';


export default {
  name: 'app',
  components: {
    Timetable,
  },
};
</script>

<style>
body, html {
  color: #2EB738;
  margin: 0px;
  padding: 0px;
}
</style>
