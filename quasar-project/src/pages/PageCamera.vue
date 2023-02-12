<template>
  <q-page class="constrain-more q-pa-md">
    <div class="camera-frame q-pa-md">
      <img class="full-width" src="images/mishka.jpeg" />
    </div>

    <div class="text-center q-pa-md">
      <q-btn color="grey-10" icon="eva-camera" size="lg" round />

      <div class="row justify-center q-ma-md">
        <q-input v-model="text" class="col" label="Caption" dense />
      </div>

      <div class="row justify-center q-ma-md">
        <q-input v-model="text" class="col" label="Location" dense>
          <template v-slot:append>
            <q-btn round dense flat icon="eva-navigation-2-outline" />
          </template>
        </q-input>
      </div>


      <div class="row justify-center q-mt-lg">
        <q-btn unelevated rounded color="primary" label="Post Image" />
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageCamera",
});
</script>

<style scoped>
.camera-frame {
  border: 2px solid grey;
}
</style>
