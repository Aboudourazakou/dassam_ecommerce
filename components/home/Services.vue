<template>
  <v-container class="container d-flex mt-4 mx-auto">
    <v-card
      v-for="service in services"
      :key="service.title"
      class="card d-flex pl-2 ml-0 mr-5"
      height="60"
      width="280"
    >
      <v-avatar size="40" class="mr-3">
        <v-img :src="'/' + service.image"></v-img>
      </v-avatar>
      <v-list-item-title class="item-title">{{ service.title }}</v-list-item-title>
    </v-card>
  </v-container>
</template>

<script>
export default {
  props: {
    services: Array
  }
};
</script>

<style scoped>
/*c*/
.card {
  margin-left: auto;
  margin-right: auto;
  align-items: center;
  background: #ffffff;
}
.container {
  height: 72px;
  padding-right: 0px;
}

/*i*/
.item-title {
  font-weight: 500;
  font-size: 16px;
  line-height: normal;
  height: 21px;
  color: #282828;
}
</style>
