<template>
  <div id="app">
    <new-poll></new-poll>
  </div>
</template>

<script>
import Vue from 'vue';
import NewPoll from './components/NewPoll';

Vue.component('new-poll', NewPoll);

export default {
  components: {
    NewPoll,
  },
};
</script>

<style lang="scss">

@import '~keen-ui/dist/keen-ui.css';

* {
	box-sizing: border-box;
	padding: 0;
	margin: 0;
}

html {
  height: 100%;
}
</style>
