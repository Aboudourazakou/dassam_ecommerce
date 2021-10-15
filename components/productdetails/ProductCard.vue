<template>
  <div class="product-card pt-4" style="width:40%;">
    <div class="active-image" style="height:305px;width:305px">
      <v-img :src="activeImage"></v-img>
    </div>
    <div
      class="avalaible-images-wrapper d-flex"
      style="position:relative;width:305px;justify-content:center;"
    >
      <div
        v-on:click="scrollright()"
        class="arrow-right"
        style="position:absolute;right:5px;top:30%;height:10px;width:10px"
      >
        <v-img src="/icons/arrow-right-black.svg"></v-img>
      </div>
      <div
        v-on:click="scrolleft()"
        class="arrow-left"
        style="position:absolute;left:4px;top:30%;height:8px;width:8px;z-index:10"
      >
        <v-img src="/icons/arrow-left-black.svg"></v-img>
      </div>
      <div class="avalaible-images d-flex">
        <div
          v-on:click="select(i)"
          v-for="i in 7"
          :key="i"
          :id="'image'+i"
          class="image"
          :class="{border:active==i}"
        >
          <v-img :src="'/nivea'+i+'.jpg'"></v-img>
        </div>
        <div
          v-on:click="select(i)"
          v-for="i in 7"
          :key="i"
          :id="'image'+i"
          class="image"
          :class="{border:active==i}"
        >
          <v-img :src="'/nivea'+i+'.jpg'"></v-img>
        </div>
      </div>
    </div>
    <div class="hr">
      <hr class="interline mt-4" style="height:1px" />
    </div>
    <h5
      class="promo"
      style="font-size: 14px;font-weight: 500;height: 35px;color: #282828; "
    >PARTAGEZ CE PRODUIT</h5>
    <div class="social d-flex">
      <div class="social-link facebook mr-3" style="height:30px;width:30px">
        <v-img src="/social/facebook.svg"></v-img>
      </div>
      <div class="social-link twitter" style="height:30px;width:30px">
        <v-img src="/social/twitter.svg"></v-img>
      </div>
    </div>
    <div class="mt-5 report">
      <a class="link" href="#">Signaler des informations incorrectes liées au produit</a>
    </div>
  </div>
</template>

  <script>
import $ from "jquery";
export default {
  data() {
    return {
      active: 0,
      activeImage: "nivea1.jpg"
    };
  },
  methods: {
    select(i) {
      this.active = i;
      this.activeImage = "/nivea" + i + ".jpg";
    },
    scrollright() {
      $(".avalaible-images ").animate({ scrollLeft: "+=35" }, 800);
    },
    scrolleft() {
      $(".avalaible-images ").animate({ scrollLeft: "-=35" }, 800);
    }
  }
};
</script>

<style scoped>
a {
  text-decoration: none;
}

.image {
  width: 12%;
  margin-right: 1%;
  margin-left: 1%;
}
.avalaible-images {
  justify-content: center;
  align-items: center;
  overflow-x: scroll;
  flex-wrap: nowrap;
  height: 45px;
  width: 270px;
  -ms-overflow-style: none !important;
  scrollbar-width: none; /* Firefox */
  -ms-overflow-style: none;
  scrollbar-width: none; /* Firefox */
}
.avalaible-images::-webkit-scrollbar {
  display: none;
}
.border {
  border: 1px solid #f68b1e;
}
.social-link {
  cursor: pointer;
}
.link {
  color: #264996;
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
  font-size: 12px;
  font-weight: 400;
  height: 19px;
  line-height: normal;
  margin: 0px;
  padding: 0px;
}

/* Hide scrollbar for IE, Edge add Firefox */
</style>
