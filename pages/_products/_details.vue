<template>
  <v-app>
    <SecondHeader />
    <v-main>
      <v-container class="main-wrapper d-flex justify-center mt-5">
        <div class="wrapper d-flex" style="width:1160px">
          <div
            class="left-card d-flex justify-center"
            style="width:70%;background:#ffffff;border-radius:5px"
          >
            <ProductdetailsProductCard />
            <ProductdetailsProductinfos :product="product" :promotions="promotions" />
          </div>
          <div class="right-card ml-4 pt-2" style="width:30%;background:#ffffff;border-radius:5px">
            <ProductdetailsRightCard />
          </div>
        </div>
      </v-container>
    </v-main>
  </v-app>
</template>
<script>
export default {
  data() {
    return {
      product: {
        name:
          "L'Oréal Paris L'Oréal Paris Elsève Dream Long - Crème sauveuse de pointes cheveux longs huile de ricin - 200 ml",
        rating: 4.3,
        marque: "Durex",
        price: "32.00",
        discountedprice: "88.00",
        discount: "20",
        notations: "2000"
      },
      promotions: [
        {
          icon: "/icons/crown.svg",
          title:
            "Livraison gratuite à Casablanca, Rabat, Marrakech ou Tanger avec Jumia Prime, abonnez-vous maintenant"
        },
        {
          icon: "/icons/crown.svg",
          title:
            "Livraison gratuite à Casablanca, Rabat, Marrakech ou Tanger avec Jumia Prime, abonnez-vous maintenant"
        }
      ]
    };
  }
};
</script>

<style scoped>
/*a*/
a {
  text-decoration: none;
}
* {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
}
/*c*/

.v-application {
  background-color: #f5f5f5;
}
</style>
