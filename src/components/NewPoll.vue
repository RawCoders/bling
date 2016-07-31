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

    <div style="padding: 8px 0;">
        <list-item text="List Item 1" icon-left="turned_in"></list-item>
        <list-item text="List Item 2" icon-left="search"></list-item>
        <list-item text="List Item 2" icon-right="search"></list-item>
    </div>
</template>


<script>

import { UiToolbar, UiButton, UiIconButton } from 'keen-ui';
import ListItem from './common/ListItem';

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
    ListItem,
  },
};
</script>


<style lang="scss" scoped>

@import '../styles/variables';

.ui-toolbar-colored {
  background-color: $brand-primary;
}

</style>
