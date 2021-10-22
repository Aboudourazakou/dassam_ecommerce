<template>
  <div class="product-card pt-4 pl-5" style="width:40%;">
    <!--Active image -->
    <div class="active-image">
      <v-img :src="activeImage"></v-img>
    </div>
    <!--end active image -->

    <!--avalaible images -->
    <div class="avalaible-images-wrapper d-flex">
      <div v-on:click="scrollright()" class="arrow-right">
        <v-img src="/icons/arrow-right-black.svg"></v-img>
      </div>
      <div v-on:click="scrolleft()" class="arrow-left">
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
    <!--end avalaible image -->
    <!--hr -->
    <div class="hr mr-3">
      <hr class="interline mt-4" style="height:1px" />
    </div>
    <!--end hr -->
    <h5 class="promo">PARTAGEZ CE PRODUIT</h5>
    <!--Social links -->
    <div class="social d-flex">
      <div class="social-link facebook mr-3">
        <v-img src="/social/facebook.svg"></v-img>
      </div>
      <div class="social-link twitter">
        <v-img src="/social/twitter.svg"></v-img>
      </div>
    </div>
    <!--end social links -->

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

.active-image {
  height: 280px;
  width: 280px;
}
.arrow-left {
  position: absolute;
  left: 4px;
  top: 30%;
  height: 8px;
  width: 8px;
  z-index: 10;
}
.arrow-right {
  position: absolute;
  right: 19px;
  top: 30%;
  height: 10px;
  width: 10px;
}

.image {
  width: 16%;
  margin-right: 1%;
  margin-left: 1%;
}
.avalaible-images {
  justify-content: center;
  align-items: center;
  overflow-x: scroll;
  flex-wrap: nowrap;
  height: 45px;
  width: 200px;
  -ms-overflow-style: none !important;
  scrollbar-width: none; /* Firefox */
  -ms-overflow-style: none;
  scrollbar-width: none; /* Firefox */
}
.avalaible-images-wrapper {
  position: relative;
  width: 280px;
  justify-content: center;
}
.avalaible-images::-webkit-scrollbar {
  display: none;
}
.border {
  border: 1px solid #f68b1e;
}

.interline {
  border: 1px solid #c7c7cd;
  border-bottom: none;
}

.social-link {
  cursor: pointer;
  height: 30px;
  width: 30px;
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

.product-card {
  position: relative;
}
.promo {
  font-size: 14px;
  font-weight: 500;
  height: 35px;
  color: #282828;
}

.report {
  position: absolute;
  bottom: 15px;
}

/* Hide scrollbar for IE, Edge add Firefox */
</style>
