<template>
  
  <div class="list-item" :class="isActive" v-el:listitem>
    <span>{{ text }}</span>
    <i class="material-icons participants">supervisor_account</i>
    <span class="participant-count">{{ participants }}</span>
    <i class="material-icons indicator">fiber_manual_record</i>
    <ui-ripple-ink :trigger="$els.listitem"></ui-ripple-ink>
  </div>
  
</template>

<script>

import { UiIconButton, UiRippleInk } from 'keen-ui';

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

    participants: {
      type: String,
      required: true,
    },

    active: {
      type: String,
    },
  },
  computed: {
    isActive() {
      if (this.active) {
        return ['active'];
      }
      return [];
    },
  },
  components: {
    UiIconButton,
    UiRippleInk,
  },
};
</script>


<style lang="scss" scoped>

@import '../styles/variables';

.list-item {

  position: relative;
  padding: 16px;

  i {
    position: absolute;
    line-height: 0.8;
    color: #bbb;

    &.indicator {
      right: 16px;
    } 

    &.participants {
      right: 78px;
    } 
  }

  &.active .indicator{
    color: $indicator-green;
  }
  
  span.participant-count {
    position: absolute;
    right: 56px;
    color: $muted-text;
  }
}

</style>
