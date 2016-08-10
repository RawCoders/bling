<template>
  <div id="app">

    <ui-toolbar type="colored" title="Bling" text-color="white">
      <div slot="actions">
        <ui-icon-button type="clear" color="white" icon="search"></ui-icon-button>
        <ui-icon-button type="clear" color="white" icon="more_vert" has-dropdown-menu
          :menu-options="menu" dropdown-position="bottom right"></ui-icon-button>
      </div>
    </ui-toolbar>

    <div id="app-body">
      <new-poll></new-poll>
    </div>

  </div>
</template>

<script>
import { UiToolbar, UiIconButton } from 'keen-ui';
import NewPoll from './components/NewPoll';

export default {
  components: {
    NewPoll,
    UiToolbar,
    UiIconButton,
  },
};
</script>

<style lang="scss">

@import '~keen-ui/dist/keen-ui.css';
@import './styles/variables';

* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

html {
  font-family: $font-stack;
  font-size: 16px;
  height: 100%;
}

.ui-toolbar-colored {
  background-color: $brand-primary;
}
</style>
