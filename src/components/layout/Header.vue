<template>
  <q-layout-header :reveal="true">
    <q-toolbar>
      <q-btn flat round dense icon="menu" @click="toggle" aria-label="Toggle menu on left side"/>
      <q-toolbar-title @click="goHome">
        <q-btn flat round dense icon="home" @click="goHome"/>
        {{ title }}
      </q-toolbar-title>

      <q-btn-dropdown
        ref="selectLanguages"
        v-if="hasMultipleLanguages"
        icon="language"
        :label="currentLanguage.code"
        flat
        dense
      >
        <q-list link>
          <q-item
            v-close-overlay
            v-for="(language, index) in availableLanguages"
            :key="index"
            @click.native="setLanguage(language.code)"
          >
            <q-item-main :label="language.name"/>
            <q-item-side
              v-if="language.code === currentLanguage.code"
              right
              icon="done"
              color="primary"
            />
          </q-item>
        </q-list>
      </q-btn-dropdown>
    </q-toolbar>
  </q-layout-header>
</template>


<script lang="ts">
import { Vue, Component, Mixins, Emit, Prop } from "vue-property-decorator";
import { Mixin as i18nMixin } from "@/plugins/i18n";

@Component
export default class Header extends Mixins(i18nMixin) {
  @Prop() title!: String;

  @Emit("toggle")
  toggle() {}
  goHome() {
    this.$router.push("/");
  }
}
</script>

<style scoped>
</style>
