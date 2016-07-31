<template>
  
  <div :class="styleClasses">
    <i class="material-icons">{{ iconLeft || iconRight }}</i>
    {{ text }}
    <ui-ripple-ink :trigger="$el"></ui-ripple-ink>
  </div>
  
</template>


<script>

import UiRippleInk from 'keen-ui';

export default {
  name: 'list-item',
  data() {
    return {
      txt: 'Some Text',
    };
  },
  props: {

    text: {
      type: String,
      required: true,
    },

    iconLeft: {
      type: String,
      default: null,
    },

    iconRight: {
      type: String,
      default: null,
    },

  },
  computed: {

    styleClasses() {
      const classes = ['list-item'];

      if (this.iconLeft) {
        classes.push('icon-left');
      }

      if (this.iconRight) {
        classes.push('icon-right');
      }

      return classes;
    },

  },
  components: {
    UiRippleInk,
  },
};
</script>


<style lang="scss" scoped>

@import '../../styles/variables';

.list-item {

  font-family: $font-stack;
  position: relative;
  padding: 16px;

  &.icon-left {
    padding-left: 72px;
    
    i.material-icons {
      left: 4px;
    }
  }

  &.icon-right {
    padding-right: 56px;

    i.material-icons {
      right: 4px;
    }
  }

  i.material-icons {
    position: absolute;
    top: 0;
    height: 24px;
    width: 24px;
    margin: 12px;
  }

}

</style>
