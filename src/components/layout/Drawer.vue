<template>
  <q-layout-drawer
    side="left"
    :value="isOpen"
    :content-class="$q.theme === 'mat' ? 'bg-grey-3' : null"
  >
    <q-scroll-area class="fit">
      <q-list-header>Left Panel</q-list-header>
      <q-item>
        <q-item-side icon="account circle"/>
        <q-item-main label="Item 1" sublabel="Learn more about it"/>
        <q-item-side right icon="thumb_up"/>
      </q-item>
      <q-item>
        <q-item-side icon="view_array"/>
        <q-item-main label="Item 2" sublabel="Learn more about it"/>
      </q-item>
    </q-scroll-area>
  </q-layout-drawer>
</template>

<script lang="ts">
import { Vue, Component, Prop } from "vue-property-decorator";
@Component({
  name: "my-drawer"
})
export default class Drawner extends Vue {
  @Prop(Boolean)
  open!: boolean;

  get isOpen() {
    return this.open;
  }
}
</script>

<style scoped>
</style>
