<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-white text-grey-10" bordered>
      <q-toolbar>
        <q-btn
          to="/camera"
          flat
          round
          size="18px"
          icon="eva-camera-outline"
          dense
        />

        <q-separator spaced vertical inset />
        <q-toolbar-title class="text-center text-grand-hotel text-h4 text-bold"
          >QuasarGram</q-toolbar-title
        >

        <q-separator spaced vertical inset />
        <q-btn to="/" flat round size="18px" icon="eva-home-outline" dense />
      </q-toolbar>
    </q-header>

    <q-footer class="bg-white" small-screen-only bordered>
      <q-tabs
        class="text-grey-10"
        active-color="primary"
        indicator-color="transparent"
      >
        <!-- <q-route-tab to="/" icon="eva-home-outline" />
        <q-route-tab to="/camera" icon="eva-camera-outline" /> -->
      </q-tabs>
    </q-footer>

    <q-page-container class="bg-grey-1">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>

<!-- <style lang="sass" scoped>
  .q-footer
    .q-tab_icon
      font-size: 30px
</style> -->
