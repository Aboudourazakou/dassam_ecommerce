<template>
  <div class="product-infos pr-5">
    <!--Chip and heart icon -->
    <div class="chip d-flex">
      <p class="chip-content">Boutique officielle</p>

      <div class="heart">
        <v-btn class="btn" icon color="deep-orange"></v-btn>
        <v-img src="/icons/love.svg"></v-img>
      </div>
    </div>
    <!--End chip and heart icon -->

    <!--product title -->
    <div class="product-title">
      <p class="title">{{product.name}}</p>
    </div>
    <!--end product title -->

    <!--marques --->
    <div class="marque d-flex">
      <p style="color:#282828">Marque:</p>
      <p>
        <a href="#" class="ml-1 name-marque link">{{product.marque}}</a>
        <span class="mr-1 ml-1" style="color:#282828;font-weight:400">|</span>

        <a href="#" class="similary-marque link">Produits similaires a Durex</a>
      </p>
    </div>
    <!--end marques -->

    <!--rating -->
    <div class="rating d-flex" style="align-items:center;">
      <v-rating
        v-model="product.rating"
        background-color="white"
        color="yellow accent-4"
        dense
        half-increments
        size="18"
      ></v-rating>
      <a class="link notations" href="#">({{product.notations}})</a>
    </div>
    <!--end rating -->

    <!-- info image -->
    <div class="livraison mt-3" style="height:16px;width:135px">
      <v-img src="/livraison.png"></v-img>
    </div>
    <!--end info image -->

    <!-- hr line -->
    <div class="hr">
      <hr class="interline mt-4" style="height:1px" />
    </div>
    <!--end  hr  line -->
    <!--prices div -->
    <div class="prices d-block">
      <p class="real-price">{{product.price}}</p>
      <div class="discount d-flex">
        <p class="default-price text-decoration-line-through">{{product.discountedprice}}</p>
        <v-card
          flat
          width="60"
          height="24"
          color="#FFCCBC"
          class="d-flex ml-4"
          style="color:#f68b1e;justify-content:center"
        >
          <p>-{{product.discount}} %</p>
        </v-card>
      </div>
    </div>
    <!--end prices div -->

    <!--begin shipment place -->
    <div class="shipment-place mt-3">
      <p>
        + livraison à partir de
        <span style="font-weight:500">10.00 Dhs</span> vers CASABLANCA - Anfa
      </p>
    </div>
    <!--end shipment place -->

    <!--buy button -->
    <div class="buy-button mb-4">
      <!--icon -->
      <div class="buy-icon">
        <v-img src="/icons/shop-cart.svg"></v-img>
      </div>
      <!--icon -->
      <v-btn
        class=""
        elevation="5"
        shaped
        large
        color="success"
        style="  background: #e4811c !important;color: #ffffff;width:100%"
      >J'Achète</v-btn>
    </div>
    <!--end buy button -->

    <div class="hr">
      <hr class="interline mt-4" style="height:1px" />
    </div>
    <h5 class="promo">PROMOTIONS</h5>

    <!--Promotions list -->
    <ul class="promo-list pl-0">
      <li v-for="promotion in promotions" :key="promotion.icon">
        <a href="#" class="d-flex pr-0 ml-0" style="justify-content:center">
          <div class="icon-promo pl-0 ml-0 mr-2">
            <v-img :src="promotion.icon"></v-img>
          </div>
          <p class="promo-text">{{promotion.title}}</p>
        </a>
      </li>
    </ul>
    <!--End promotion list -->
  </div>
</template>

<script>
export default {
  props: {
    promotions: Array,
    product: Array
  },
  data() {}
};
</script>


<style scoped>
a {
  text-decoration: none;
}

.buy-button {
  position: relative;
  height: 45px;
}

.buy-icon {
  height: 20px;
  width: 20px;
  position: absolute;
  z-index: 10;
  top: 25%;
  left: 20px;
}

.default-price {
  color: #75757a;
  font-size: 16px;
  font-weight: 400;
  height: 10px;
}

.chip {
  align-items: center;
  justify-content: space-between;
  height: 40px;
}

.chip-content {
  background-color: #b60000;
  max-width: 124px;
  font-size: 14px;
  font-weight: 500;
  height: 20px;
  line-height: 16.8px;
  margin: 8px 0px 0px;
  padding: 0px 4px;
}

.heart {
  height: 20px;
  width: 20px;
  position: relative;
}

.heart > .btn {
  position: absolute;
  z-index: 10;
  top: -8px;
  left: -8px;
}
.icon-promo {
  height: 20px;
  width: 20px;
}

.link {
  color: #264996;
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
  font-size: 14px;
  font-weight: 400;
  height: 19px;
  line-height: normal;
  margin: 0px;
  padding: 0px;
}
li {
  list-style: none;
}
.marque > p {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
  font-size: 14px;
  font-weight: 400;
  height: 27px;
  line-height: normal;
  margin: 0px;
  padding: 4px 0px;
  flex-wrap: nowrap;
  align-items: center;
}

.notations {
  height: 10px !important;
}

.product-infos {
  width: 60%;
  background: white;
}
.product-title {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
}

.promo {
  font-size: 14px;
  font-weight: 500;
  height: 35px;
  color: #282828;
}

.promo-text {
  font-size: 14px;
  font-weight: 400;
  height: 45px;
  color: #264996;
}

.real-price {
  font-size: 24px;
  font-weight: 700;
  height: 20px;
  color: #282828;
}
.shipment-place {
  font-size: 12px;
  font-weight: 400;
  height: 32px;
  color: #282828;
}
.title {
  color: #282828;
  font-size: 20px;
  font-weight: 400;
  height: 92px;
  line-height: normal;
  margin: 0px;
  padding: 8px 0px 4px;
  width: 463px;
}
</style>
