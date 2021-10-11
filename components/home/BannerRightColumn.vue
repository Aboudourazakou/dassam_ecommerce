<template>
   <div class="d-block ml-3">
          <v-card width="218" style="border-radius:5px" class="mb-4" color="white">
            <div
              class="list-wrapper d-flex pt-4 pl-2"
              style="padding-bottom:8px"
              v-for="info in infos"
              :key="info.title"
            >
              <v-avatar size="30" class="mr-3">
                <v-img :src="'/' + info.image"></v-img>
              </v-avatar>
              <div class="list-content d-block" style="color:black">
                <h4 class="pb-0 m-0 infotitle">{{ info.title }}</h4>
                <h5 class="pt-0 mt-0 infosubtitle">{{ info.info }}</h5>
              </div>
            </div>
          </v-card>
          <v-img style="border-radius:5px" src="/4.jpg" width="auto" height="auto"></v-img>
        </div>
</template>

<script>
export default {
  props:{
    infos:Array,
  }

}
</script>

<style scoped>
  /*i*/
  .infosubtitle {
  font-size: 12px;
  font-weight: 400 !important;
}
.infotitle {
  font-size: 14px;
  font-weight: 500 !important;
}
</style>
