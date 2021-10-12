<
<template>

      <!--Les plus demandees-->
     <v-container class="d-flex" style="justify-content:center;">
        <v-container class="container  pt-0 nomobile pl-0  mt-5"  style="width:auto;position:relative">

       <!--Scrool arrow right-->
            <div class="arrow-right" id="right-arrow" style="position:absolute;right:3px;bottom:50%;z-index:10;">
               <v-fab-transition>
      <v-btn
      v-on:click="scrolright()"
       style="background:#75757a"
        fab
        small
        dark


        class="v-btn--example  "
      >
    <v-avatar size="12">
              <v-img src="/icons/arrow-right.svg"></v-img>
              </v-avatar>
      </v-btn>
    </v-fab-transition>
        </div>
       <!--End Scroll arrow right -->

         <!--Scrool arrow left-->
            <div class="arrow-left" id="left-arrow" style="position:absolute;left:3px;bottom:50%;z-index:10;">
               <v-fab-transition>
      <v-btn
      v-on:click="scrolleft()"
       style="background:#75757a"
        fab
        small
        dark


        class="v-btn--example  "
      >
    <v-avatar size="12">
              <v-img src="/icons/arrow-left.svg"></v-img>
              </v-avatar>
      </v-btn>
    </v-fab-transition>
        </div>
       <!--End Scroll arrow left -->
        <v-card flat class="header1 d-flex pl-2 pb-0  white pt-3" height="48" width="1160" >
          <h2>
            Les plus demandés
          </h2>
        </v-card>

        <v-card
          flat
          class=" products-first scroll-right pt-0 d-flex pl-3 text-center"
          height="auto"
          color="white"
          width="1160"

        >
          <v-card
            flat
            class="wrapped-item-card d-block "
            height="263"
            width="193"
            v-for="product in products"
            color="white"
          >
            <v-card
              style="position:relative"
              tile
              flat
              class="image-card "
              height="187"
              width="187"
              color="white"
            >
              <v-card
                rounded

                flat
                width="40"
                height="24"
                color="white"
                style="position:absolute;right:2px;top:2px;z-index:1;color:#f68b1e"
                >-20%</v-card
              >
              <v-img :src="'/' + product.image"></v-img>
            </v-card>

            <p

              style="width:inherit;color:black"
              class="itemname d-inline-block text-truncate pb-0 mb-0"
            >
              {{ product.name }}
            </p>
            <div class="price d-block pt-0 mt-0" style="color:black ">
              <h3>{{ product.priceN }}</h3>
              <h5 class="text-decoration-line-through ">{{ product.priceR }}</h5>
            </div>
          </v-card>
        </v-card>
      </v-container>
      </v-container>
      <!--End les plus demandes-->
</template>

<script>
import $ from "jquery";

export default {
  props: {
    products: Array
  },
  data() {
    return {
      scrolValue: 500,
      leftScrolling: false,
      rightScrolling: false
    };
  },

  methods: {
    scrolright() {
      console.log("Salut");
      $(".scroll-right ").animate({ scrollLeft: "+=700" }, 800);

      var $width = $(".scroll-right ").outerWidth();
      var $scrollWidth = $(".scroll-right ")[0].scrollWidth;
      var $scrollLeft = $(".scroll-right ").scrollLeft();

      //Check if scrolling is finished
      if ($width + $scrollLeft + 700 > $scrollWidth) {
        $(".scroll-right ").animate({ scrollLeft: "+=700" }, 800);

        document.getElementById("right-arrow").style.display = "none";
      }
    },
    scrolleft() {
      $(".scroll-right ").animate({ scrollLeft: "-=700" }, 800);
      var $scrollLeft = $(".scroll-right ").scrollLeft();

      //Check if scrolling is finished
      if ( $scrollLeft -700 <500) {
        $(".scroll-right ").animate({ scrollLeft: "-=700" }, 800);

        document.getElementById("left-arrow").style.display = "none";
      }
    }
  }
};
</script>

<style scoped>
.container {
  margin: auto;
  padding-right: 0px;
  justify-content: center;
}

/* Hide scrollbar for IE, Edge add Firefox */
.card-overflow {
  -ms-overflow-style: none;
  scrollbar-width: none; /* Firefox */
}

/*i*/
.itemname {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
  font-size: 12px;
  color: #282828;
}
/*h*/
.header1 > h2 {
  font-weight: 500;
  font-size: 16px;
  line-height: normal;
  height: 21px;
  color: #282828;
}

/*p*/
.price h3 {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
  color: #282828;
  font-weight: 500;
  font-size: 16px;
}
.price h5 {
  color: #75757a;
  height: 15px;
  font-weight: 400;
}
.products-first::-webkit-scrollbar {
  display: none;
}
.products-first {
  border-radius: 0px 0px 5px 5px;
  overflow-x: scroll;
  -ms-overflow-style: none;
  scrollbar-width: none; /* Firefox */
}
</style>
