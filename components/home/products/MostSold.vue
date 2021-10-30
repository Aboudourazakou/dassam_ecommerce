<
<template>

      <!--Les plus demandees-->
     <v-container class="d-flex mb-0 pb-0 mx-auto">
        <v-container class="container   pt-0 nomobile pl-0  mt-3 mb-0"  style="width:auto;position:relative">


         <!--Scrool arrow right-->
            <div  @mouseover="displayArrows()" class="arrow-right" id="right-arrow" style="position:absolute;right:3px;bottom:50%;z-index:10;">
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
            <div  @mouseover="displayArrows()"  class="arrow-left" id="left-arrow" style="position:absolute;left:3px;bottom:50%;z-index:10;">
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


      <!--title-->
       <v-container class="title d-flex" style="height:50px;width:1160px;justify-content:left;align-items:center;background:white">
         <h5 style="color:black">Les  plus demandés</h5>
       </v-container>
      <!--end title-->
       <v-container class="products-container  scroll-right white d-flex align-items-space-around pr-0 pl-3 pb-4 pr-0 mt-0 pt-0" style="height:270px;width:1160px;position:relative">

         <div class="product-wrapper mr-0 ml-0 pr-0 pl-0 pt-0 mb-0 pb-0" style="display:flex;flex-wrap:wrap;position:relative" v-for="product in products"  @mouseover="displayArrows()" @mouseleave="disableArrows()" @click="viewProduct(product.name)" >


            <v-card

                rounded

                flat
                width="40"
                height="24"
                color="white"
                style="position:absolute;right:20px;top:20px;z-index:1;color:#f68b1e;background-color: #feefde; "
                >-20%</v-card
              >
              <div style="border-radius:5px; width:100%;height:187px;important">
               <v-img

               :src="'/' + product.image" loading="lazy"></v-img>
             </div>
             <div class="pr-3 pl-3 " style="height:70px;width:100%;">
               <p style="width:inherit;color:black"
                class="itemname d-inline-block text-truncate pb-0 mb-0">
                Cafeine thailandais au gaz ou bien je vais</p>
                   <h5 class="price d-inline-block text-truncate" >160.00 Dhs</h5>
                   <h4 class=" canceled-price text-truncate text-decoration-line-through ">88.00 Dhs</h4>
             </div>



         </div>


       </v-container>
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
    viewProduct(name) {
      
   this.$router.push(name.trim().replace(/ /g, "-").toLowerCase())
    },
    disableArrows() {
      document.getElementById("right-arrow").style.display = "none";
      document.getElementById("left-arrow").style.display = "none";
    },
    displayArrows() {
      var $width = $(".scroll-right ").outerWidth();
      var $scrollWidth = $(".scroll-right ")[0].scrollWidth;
      var $scrollLeft = $(".scroll-right ").scrollLeft();

      //Check if scrolling is finished
      if ($width + $scrollLeft < $scrollWidth) {
        document.getElementById("right-arrow").style.display = "block";
      } else {
        document.getElementById("right-arrow").style.display = "none";
      }

      console.log($scrollLeft);
      //Check if scrolling is finished
      if ($scrollLeft <= 0) {
        document.getElementById("left-arrow").style.display = "none";
      } else {
        document.getElementById("left-arrow").style.display = "block";
      }
    },
    scrolright() {
      $(".scroll-right ").animate({ scrollLeft: "+=700" }, 800);
      //Display left arrow
      document.getElementById("left-arrow").style.display = "block";

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
      //Display right arrow
      document.getElementById("right-arrow").style.display = "block";

      var $scrollLeft = $(".scroll-right ").scrollLeft();
      //Check if scrolling is finished
      if ($scrollLeft - 700 < 500) {
        $(".scroll-right ").animate({ scrollLeft: "-=700" }, 800);

        document.getElementById("left-arrow").style.display = "none";
      }
    }
  }
};
</script>

<style scoped>
/*a*/
.arrow-right {
  display: none;
}
.arrow-left {
  display: none;
}

.container {
  padding-right: 0px;
  justify-content: center;
}

/* Hide scrollbar for IE, Edge add Firefox */
.card-overflow {
  -ms-overflow-style: none;
  scrollbar-width: none; /* Firefox */
}
/*d*/
.disable-scrollLeft {
  display: none;
}
.disable-Right {
  display: none;
}

/*e*/
.enable-scrollLeft {
  display: block;
}
.enable-scrollRight {
  display: block;
}

/*i*/
.itemname {
  color: #282828;
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
  font-size: 14px;
  font-weight: 400;
  height: 16px;
  line-height: 14px;
}
/*h*/
.header1 > h2 {
  font-weight: 500;
  font-size: 16px;
  line-height: normal;
  height: 21px;
  color: #282828;
  border-bottom-left-radius: 0px !important;
}

/*p*/

.price {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
  color: #282828;
  font-size: 16px;
  font-weight: 500;
  line-height: 16px;
  width: inherit;
}

.canceled-price {
  color: #75757a;
  font-weight: 300;
  font-size: 12px;
  width: inherit;
}
.products-container {
  background: #ffffff;
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 5px;
  overflow-x: scroll;
  -ms-overflow-style: none;
  scrollbar-width: none; /* Firefox */
}
.products-container .product-wrapper {
  width: 16.5%;
}

.product-wrapper {
  border-radius: 4px;
  background: #fff;
  flex-wrap: nowrap;

  padding: 14px 80px 18px 36px;
  cursor: pointer;
}

.product-wrapper:hover {
  transform: scale(1.05);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12), 0 4px 8px rgba(0, 0, 0, 0.06);
}
.products-container::-webkit-scrollbar {
  display: none;
}
.products-first {
  border-radius: 0px 0px 5px 5px;
  overflow-x: scroll;
  -ms-overflow-style: none;
  scrollbar-width: none; /* Firefox */
}

/*t*/
.title {
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
}
.title h5 {
  color: #282828;
  font-size: 20px;
  font-weight: 500;
  height: 27px;
}
/*w*/
.wrapped-item-card {
  display: none;
}
</style>
