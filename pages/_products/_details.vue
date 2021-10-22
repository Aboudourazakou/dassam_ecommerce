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
          <div class="left-card d-flex justify-center" style="width:70%;border-radius:5px">
            <ProductdetailsDescription />
          </div>
          <!--end product details -->

          <!--Right card --->
          <div class="right-card ml-4" style="width:30%;border-radius:5px;position:sticky;top:80px">
            <div class="ancre-wrapper" style="background:#ffffff;border-radius:5px">
              <div
                v-for="element in ancres"
                :key="element"
                class="ancre d-flex pl-3 pr-3"
                style="height:48px;align-items:center;cursor:pointer"
              >
                <div class="ancre-icon mr-5" style="height:16px;width:16px">
                  <v-img :src="'/icons/'+element.icon"></v-img>
                </div>
                <div style="font-size: 14px;font-weight: 500;">
                  <a href style="color: #282828; ">{{element.title}}</a>
                </div>
              </div>
            </div>
          </div>
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
      ],
      ancres: [
        {
          title: "Details",
          icon: "details.svg"
        },
        {
          title: "Fiche technique",
          icon: "technique.svg"
        },
        {
          title: "Avis des utilisateurs",
          icon: "comment.svg"
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

.ancre:nth-child(2) {
  border-top: 1px solid #ededed;
  border-bottom: 1px solid #ededed;
  background-color: #ededed;
}
* {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
  color: #282828;
}

.v-application {
  background-color: #f5f5f5;
}
</style>
