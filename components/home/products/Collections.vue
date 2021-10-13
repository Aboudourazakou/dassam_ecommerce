<template>
  <!--Collections  no mobile-->

  <v-container class="d-flex" style="justify-content:center">
    <v-container class="container d-block pt-0 ml pr-0 pl-0" style="width:auto;">
      <v-card
        flat
        class="header3 d-flex pl-2 pb-0"
        height="48"
        color="white"
        style="width:1160px;border-bottom-left-radius:0px;border-bottom-right-radius:0px"
      >
        <h2
          style="font-weight:500;font-size:16px;line-height:normal;height:21px;color:#282828"
        >Collections</h2>
      </v-card>

      <v-card
        color="white"
        flat
        style="border-radius:0px 0px 5px 5px;flex-wrap: wrap;width:1160px"
        class="products-collections pt-0 d-flex pl-1"
        height="307"
      >
        <v-card
          color="white"
          v-for="collection in collections"
          :key="collection.image"
          flat
          style="margin-left:auto;margin-right:auto"
          class="wrapped-item-card d-block text-center pr-0 pl-0 ml-0 mr-0"
          height="144"
          width="16.5%"
        >
          <v-card
            color="white"
            style="position:relative"
            tile
            flat
            class="image-card ml-0 pl-0"
            height="109"
            width="100%"
          >
            <v-img :src="'/' + collection.image"></v-img>
          </v-card>
          <p style="width:180px" class="mt-3">{{ collection.title }}</p>
        </v-card>
      </v-card>
    </v-container>
  </v-container>
  <!--End collections-->
</template>

<script>
export default {
  props: {
    collections: Array
  }
};
</script>
