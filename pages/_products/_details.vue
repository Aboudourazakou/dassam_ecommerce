<template>
  <v-app>
    <SecondHeader />
    <v-main>
      <v-container class="main-wrapper d-flex justify-center mt-5">
        <div class="wrapper d-flex" style="width:1160px">
          <!--Product card wrapper and infos -->
          <div
            class="left-card d-flex justify-center"
            style="width:70%;background:#ffffff;border-radius:5px"
          >
            <ProductdetailsProductCard />
            <ProductdetailsProductinfos :product="product" :promotions="promotions" />
          </div>
          <!--end product card wrapper and infos -->

          <!--Right card --->
          <div class="right-card ml-4" style="width:30%;border-radius:5px">
            <ProductdetailsRightCard :cities="cities" :shipments="shipments" :policies="policies" />
            <ProductdetailsSupplierCard />
          </div>
          <!--End right card -->
        </div>
      </v-container>

      <v-container class="main-wrapper d-flex justify-center mt-5">
        <!--second wrapper -->
        <div class="second-wrapper d-flex" style="width:1160px">
          <!--Product details -->
          <div
            class="left-card d-flex justify-center"
            style="width:70%;background:#ffffff;border-radius:5px"
          ></div>

          <ProductdetailsDescription/>
          <!--end product details -->

          <!--Right card --->
          <div class="right-card ml-4" style="width:30%;border-radius:5px"></div>
          <!--End right card -->
        </div>
        <!--end second wrapper -->
      </v-container>
      <HomeFooter />
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
      ],
      cities: [
        {
          id: "1",
          name: "Grand Casablanca"
        },
        {
          id: "2",
          name: "Tetouan-Tanger-Al Hoceima-Taza"
        },
        {
          id: "3",
          name: "Rabat"
        }
      ],

      shipments: [
        {
          id: 1,
          title: "Livraison domicile",
          price: 20,
          icon: "/icons/car.svg",
          infos:
            "Vous pourrez faire le retour d'ici dix jours ,a compter de vendredi" +
            "20 Octobre 2022.Nous vous dirons la suite  plus tard"
        },
        {
          id: 2,
          price: 10,
          icon: "/icons/delivery.svg",
          title: "Point relais",
          infos:
            "Vous pourrez faire le retour d'ici dix jours ,a compter de vendredi" +
            "20 Octobre 2022.Nous vous dirons la suite  plus tard"
        }
      ],
      policies: [
        {
          id: 1,
          icon: "/icons/return-purchase.svg",
          title: "Politique de retour",
          infos:
            "Vous ne pourrez ramener l'article que dans un etat  le  plus complet possible.En verite,les bonnes choses se gatent au plus vite"
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
