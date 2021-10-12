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



      <!--title-->
       <v-container class="title d-flex" style="height:60px;width:1160px;justify-content:left;align-items:center;background:white">
         <h5 style="color:black">Les  plus demandes</h5>
       </v-container>
      <!--end title-->
       <v-container class="products-container white d-flex justify-space-around pr-0 pl-3 pb-4 pr-3 mt-0 pt-0" style="height:280px;width:1160px">

         <v-div class="product-wrapper " v-for="i in 6">

             <v-div style="width:100%;height:120px;background:red">
                <v-img src="/101.jpg"></v-img>
             </v-div>

         </v-div>
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
      if ($scrollLeft - 700 < 500) {
        $(".scroll-right ").animate({ scrollLeft: "-=700" }, 800);
        console.log($scrollLeft);
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
  margin: auto;
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
  border-bottom-left-radius: 0px !important;
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
.products-container {
  background: #ffffff;
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 5px;
}
.products-container .product-wrapper {
  width: 16%;
}

.product-wrapper {
  border-radius: 4px;
  background: #fff;

  padding: 14px 80px 18px 36px;
  cursor: pointer;
}

.product-wrapper:hover {
  transform: scale(1.05);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12), 0 4px 8px rgba(0, 0, 0, 0.06);
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

/*t*/
.title {
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
}
/*w*/
.wrapped-item-card {
  display: none;
}
</style>
