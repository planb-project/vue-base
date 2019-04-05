<template>
  <q-layout view="lHh Lpr lFf">
    <my-header title="Grammar" @toggle="toggle"/>
    <my-drawer :open="opened"/>
    <my-container/>
  </q-layout>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

import myHeader from "@/components/layout/Header.vue";
import myDrawer from "@/components/layout/Drawer.vue";
import myContainer from "@/components/layout/Container.vue";

@Component({
  components: {
    myHeader,
    myDrawer,
    myContainer
  }
})
export default class MainLayout extends Vue {
  opened: boolean;

  constructor() {
    super();
    this.opened = this.$q.platform.is.desktop;
  }

  toggle() {
    this.opened = !this.opened;
  }
}
</script>
