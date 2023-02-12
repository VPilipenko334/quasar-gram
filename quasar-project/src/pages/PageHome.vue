<template>
  <q-page class="constain q-pa-md">
    <div class="row q-col-gutter-lg">
      <div class="col-12 col-sm-8">
        <q-card
          v-for="post in posts"
          :key="post.id"
          class="my-card q-mb-md"
          flat
          bordered
        >
          <q-item>
            <q-item-section avatar>
              <q-avatar>
                <img
                  src="https://avatars.githubusercontent.com/u/63820576?v=4"
                />
              </q-avatar>
            </q-item-section>

            <q-item-section>
              <q-item-label class="text-bold">veronika_instagram</q-item-label>
              <q-item-label caption> {{ post.location }} </q-item-label>
            </q-item-section>
          </q-item>

          <q-separator />

          <q-img :src="post.imageUrl" />

          <q-card-section>
            <div>{{ post.caption }}</div>
            <div class="text-caption text-grey">{{ post.date }}</div>
          </q-card-section>
        </q-card>
      </div>
      <div class="col-4">
        <q-item class="fixed">
          <q-item-section avatar>
            <q-avatar>
              <img src="https://avatars.githubusercontent.com/u/63820576?v=4" />
            </q-avatar>
          </q-item-section>

          <q-item-section>
            <q-item-label class="text-bold">veronika_instagram</q-item-label>
            <q-item-label caption> Veronika Pilipenko </q-item-label>
          </q-item-section>
        </q-item>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "PageHome",
  data() {
    return {
      posts: [
        {
          id: 1,
          caption: "My little Mishka.",
          date: "May 5th 11:11 A.M",
          location: "New York, New York",
          imageUrl: "images/mishka.jpeg",
        },
        {
          id: 2,
          caption: "Mishkas tongue sticking out in the summertime.",
          date: "September 3rd, 2:45 P.M. ",
          location: "Lower East Side, New York",
          imageUrl: "images/puppy.JPG",
        },
        {
          id: 3,
          caption: "Best friends in the snow.",
          date: "December 2nd 4:54 P.M. ",
          location: "PA, Pennsylvania",
          imageUrl: "images/best_friends.jpeg",
        },
        {
          id: 4,
          caption: "Mishkass baby teeth coming in.",
          date: "June 27th, 9:43 A.M.",
          location: "East Village, New York",
          imageUrl: "images/baby_mish.jpeg",
        },
      ],
    };
  },
};
</script>
