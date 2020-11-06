<template>
 <v-carousel
:show-arrows="false"

    cycle
    height="500"
    hide-delimiter-background
    show-arrows-on-hover
  >
    <v-carousel-item
      v-for="(item, i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
      src:"photoDiabete/diabete.jpg"
        },
        {
      src:"photoDiabete/diabete1.jpg"
        },
        {
      src:"photoDiabete/diabete2.jpg"
        }
      ]
    };
  }
};
</script>
<style ></style>
