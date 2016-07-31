<template>
    
    <ui-toolbar
    type="colored"
    title="Bling"
    text-color="white">
        <div slot="actions">
            <ui-icon-button
                type="clear" color="white" icon="search"
            ></ui-icon-button>

            <ui-icon-button
                type="clear" color="white" icon="more_vert" has-dropdown-menu
                :menu-options="menu" dropdown-position="bottom right"
            ></ui-icon-button>
        </div>
    </ui-toolbar>
    <ui-button>
    click
    </ui-button>
    
</template>


<script>

import { UiToolbar, UiButton, UiIconButton } from 'keen-ui';

export default {
  data() {
    return {
      msg: 'Hello World!',
    };
  },
  components: {
    UiToolbar,
    UiButton,
    UiIconButton,
  },
};
</script>


<style lang="scss" scoped>

@import '../styles/variables';

.ui-toolbar-colored {
  background-color: $brand-primary;
}

</style>
