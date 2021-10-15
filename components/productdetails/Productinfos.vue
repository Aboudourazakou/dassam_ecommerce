<template>
  <div class="product-infos pr-5" style="width:60%;background:white;">
    <div class="chip d-flex" style="align-items:center;justify-content:space-between;height:40px">
      <p
        style="background-color: #b60000;max-width:124px;font-size: 14px;
                font-weight: 500;height: 20px;line-height: 16.8px;margin: 8px 0px 0px;padding: 0px 4px;"
      >Boutique officielle</p>

      <div style="height:20px;width:20px;position:relative;">
        <v-btn icon color="deep-orange" style="position:absolute;z-index:10;top:-8px;left:-8px"></v-btn>
        <v-img src="/icons/love.svg"></v-img>
      </div>
    </div>
    <div class="product-title">
      <p
        class="title"
        style="color: #282828; font-size: 20px;font-weight: 400;height: 92px;line-height: normal;margin: 0px;padding: 8px 0px 4px;width:463px"
      >L'Oréal Paris L'Oréal Paris Elsève Dream Long - Crème sauveuse de pointes cheveux longs huile de ricin - 200 ml</p>
    </div>
    <div class="marque d-flex" style="flex-wrap:nowrap;align-items:center">
      <p style="color:#282828">Marque:</p>
      <p>
        <a href="#" class="ml-1 name-marque link">Durex</a>
        <span class="mr-1 ml-1" style="color:#282828;font-weight:400">|</span>

        <a href="#" class="similary-marque link">Produits similaires a Durex</a>
      </p>
    </div>
    <div class="rating d-flex" style="align-items:center;">
      <v-rating
        v-model="rating"
        background-color="white"
        color="yellow accent-4"
        dense
        half-increments
        size="18"
      ></v-rating>
      <a class="link" style="height:10px!important" href="#">(2000 avis)</a>
    </div>
    <div class="livraison mt-3" style="height:16px;width:135px">
      <v-img src="/livraison.png"></v-img>
    </div>
    <div class="hr">
      <hr class="interline mt-4" style="height:1px" />
    </div>
    <div class="prices d-block">
      <p
        class="real-price"
        style="font-size: 24px;font-weight: 700;height: 20px;color: #282828; "
      >32.00 Dhs</p>
      <div class="discount d-flex">
        <p
          class="default-price text-decoration-line-through"
          style="color: #75757a; font-size: 16px;font-weight: 400;height:10px"
        >88.00 Dhs</p>
        <v-card
          flat
          width="60"
          height="24"
          color="#FFCCBC"
          class="d-flex ml-4"
          style="color:#f68b1e;justify-content:center"
        >
          <p>-90%</p>
        </v-card>
      </div>
    </div>
    <div
      class="shippement-place mt-3"
      style="font-size: 12px;font-weight: 400;height: 32px;color: #282828; "
    >
      <p>+ livraison à partir de 10.00 Dhs vers CASABLANCA - Anfa</p>
    </div>
    <div class="buy-button mb-4" style="position:relative;height:45px;">
      <div style="height:20px;width:20px;position:absolute;z-index:10;top:25%;left:20px">
        <v-img src="/icons/shop-cart.svg"></v-img>
      </div>
      <v-btn
        elevation="5"
        shaped
        large
        color="success"
        style="  background: #e4811c !important;color: #ffffff;width:100%"
      >J'Achète</v-btn>
    </div>
    <div class="hr">
      <hr class="interline mt-4" style="height:1px" />
    </div>
    <h5
      class="promo"
      style="font-size: 14px;font-weight: 500;height: 35px;color: #282828; "
    >PROMOTIONS</h5>

    <ul class="promo-list pl-0">
      <li>
        <a href="#" class="d-flex pr-0 ml-0" style="justify-content:center">
          <div class="icon-promo pl-0 ml-0 mr-2" style="height:20px;width:20px">
            <v-img src="/icons/crown.svg"></v-img>
          </div>
          <p
            class="promo-text"
            style="font-size: 14px;font-weight: 400;height: 45px;color: #264996; "
          >Livraison gratuite à Casablanca, Rabat, Marrakech ou Tanger avec Jumia Prime, abonnez-vous maintenant</p>
        </a>
      </li>
      <li>
        <a href="#" class="d-flex pr-0 ml-0" style="justify-content:center">
          <div class="icon-promo pl-0 ml-0 mr-2" style="height:20px;width:20px">
            <v-img src="/icons/crown.svg"></v-img>
          </div>
          <p
            class="promo-text"
            style="font-size: 14px;font-weight: 400;height: 45px;color: #264996; "
          >Livraison gratuite à Casablanca, Rabat, Marrakech ou Tanger avec Jumia Prime, abonnez-vous maintenant</p>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      rating: 4.3
    };
  }
};
</script>


<style scoped>
a {
  text-decoration: none;
}
.chip,
.product-title {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
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
}
</style>
