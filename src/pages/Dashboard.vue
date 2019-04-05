<template>
  <q-page class="flex flex-center">
    <div class="column flex-center">
      <h1>{{ $t('pages.dashboard.title') }}</h1>
    </div>
  </q-page>
</template>

<style>
</style>

<script lang="ts">
import { Vue, Component, Mixins } from "vue-property-decorator";

@Component({
  meta() {
    return {
      title: "Dashboard"
    };
  }
})
export default class PageDashboard extends Vue {}
</script>
