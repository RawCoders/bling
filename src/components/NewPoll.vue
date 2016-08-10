<template>
  <div class="new-poll">
    <div class="poll-list">
      <list-item-header text="Your polls"></list-item-header>
      <list-item text="Ionic or React?" participants="7" active="true"></list-item>
      <list-item text="PHP or NodeJS?" participants="18"></list-item>
    </div>
  </div>
</template>

<script>

import ListItem from './ListItem';
import ListItemHeader from './ListItemHeader';

export default {
  name: 'new-poll',
  data() {
    return {
    };
  },
  components: {
    ListItem,
    ListItemHeader,
  },
};
</script>


<style lang="scss" scoped>

@import '../styles/variables';


</style>
