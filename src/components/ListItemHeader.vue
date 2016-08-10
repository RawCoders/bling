<template>
  <div class="list-item-header">
    {{ text }}
  </div>
</template>


<script>

export default {
  name: 'list-item-header',
  data() {
    return {
    };
  },
  props: {

    text: {
      type: String,
      required: true,
    },

  },
};
</script>


<style lang="scss" scoped>

@import '../styles/variables';

.list-item-header {

  padding: 16px;
  padding-bottom: 18px;
  font-size: 0.8em;
  color: $muted-text;

}

</style>
