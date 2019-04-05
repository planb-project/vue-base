<template>
  <div class="fixed-center text-center">
    <img src="~assets/sad.svg" style="width: 30vw; max-width: 150px;">
    <p class="q-mt-sm text-faded">
      {{ $t('pages.errors.e404.message') }}
      <strong>(404)</strong>
    </p>

    <q-btn
      color="secondary"
      style="width:200px;"
      @click="$router.push('/')"
    >{{ $t('pages.errors.e404.back') }}</q-btn>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

@Component
export default class Error404 extends Vue {}
</script>
