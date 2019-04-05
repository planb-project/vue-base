<template>
  <q-page-container>
    <transition
      enter-active-class="animated fadeIn"
      leave-active-class="animated fadeOut"
      mode="out-in"
    >
      <router-view/>
    </transition>
  </q-page-container>
</template>

<script>
export default {
  name: 'my-container'
}
</script>

<style>
  .q-layout-page-container{
    margin: 1em;
  }
</style>
