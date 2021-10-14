<template>
  <v-app>
    <HomeMainHeader />
    <v-main>
      <!--Banner container -->
      <v-container class="banner d-flex mx-auto mt-3">
        <!--Menu on big devices not include mobile containing categories-->
        <HomeCategories :items="items" />

        <!--Caroussel-->
        <HomeCaroussel />

        <!--Right column-->
        <HomeBannerRightColumn :infos="infos" />
      </v-container>
      <!--End banner container-->


      <!--Container for differents services -->
      <HomeServices :services="services" />

      <!--Most sold products-->
      <HomeProductsMostSold :products="products1" />

      <!--Second product list -->
      <HomeProductsProductList
        :products="products2"
        title="Dernieres tendances sur Jumia"
        color="#FF550C"
        titleColor="#ffffff"
      />

      <HomeProductsCollections :collections="collections"/>
      <HomeFooter/>

    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      affiche: 1,

      collections: [
        { image: "tel.png", title: "Smartphone" },
        { image: "television.png", title: "Television" },
        { image: "montrefemme.png", title: "Montre femme" },
        { image: "montre.png", title: "Montre homme" },
        { image: "robe.png", title: "Robe femme" },
        { image: "sacamain.png", title: "Sac a main" },
        { image: "smartwatch.png", title: "Smart watch" },
        { image: "vhomme.png", title: "Veste Homme" },
        { image: "tablette.png", title: "Tablette" },
        { image: "informatique.png", title: "Informatique" },
        { image: "coque.png", title: "Coque" },
        { image: "chaussures.png", title: "Chaussure homme" }
      ],
      services: [
        {
          title: "Nos Marques ",
          image: "marques.png"
        },
        {
          title: "Dunia Global",
          image: "plane.png"
        },
        {
          title: "Dumia Food",
          image: "food.png"
        },
        {
          title: "Dunia Prime",
          image: "crown.png"
        }
      ],
      infos: [
        {
          title: "Centre d'assistance",
          info: "Guide du service client",
          image: "interrogation.png"
        },
        {
          title: "Retour facile",
          info: "Remboursement rapide",
          image: "retourfacile.png"
        },
        {
          title: "Creer votre Dunia",
          info: "Ouvrez votre shop ici",
          image: "createshop.png"
        }
      ],
      items: [
        {
          icon: "beauty.svg",
          title: "Beauté && Santé",
          to: "/Medecin"
        },
        {
          icon: "clothes.svg ",
          title: "Vêtements et Chaussures",
          to: "/pharmacies"
        },
        {
          icon: "computer.svg",
          title: "Accessoires et Mode",
          to: "/restaurants"
        },

        {
          icon: "house.svg",
          title: "Maison & Cuisine",
          to: "/boutiques"
        },

        {
          icon: "phone.svg",
          title: "Téléphone & Tablette",
          to: "/traducteurs"
        },
        {
          icon: "washing.svg",
          title: "Electroménager",
          to: "/traducteurs"
        },
        {
          icon: "computer.svg",
          title: "Informatique",
          to: "/traducteurs"
        },

        {
          icon: "supermarket.svg",
          title: "Supermarché",
          to: "/traducteurs"
        },
        {
          icon: "sport.svg",
          title: "Sports & Loisirs ) ",
          to: "/traducteurs"
        },
        {
          icon: "television.svg",
          title: "TV & High Tech ",
          to: "/traducteurs"
        },
        {
          icon: "baby.svg",
          title: "Bébé & Jouets",
          to: "/traducteurs"
        },
        {
          icon: "other.svg",
          title: "Autres catégories",
          to: "/traducteurs"
        }
      ],
      products1: [
        {
          image: "101.jpg",
          priceN: "456 000 FCFA",
          priceR: "1000.0000 FCFA",
          name: "Appareil Connecte a Bluetooth"
        },
        {
          image: "101.jpg",
          priceN: "456 000 FCFA",
          priceR: "1000.0000 FCFA",
          name: "Appareil Connecte a Bluetooth"
        },
        {
          image: "101.jpg",
          priceN: "456 000 FCFA",
          priceR: "1000.0000 FCFA",
          name: "Appareil Connecte a Bluetooth"
        },
        {
          image: "102.jpg",
          priceN: "10 000 FCFA",
          priceR: "100.0000 FCFA",
          name: "Appareil mobile "
        },
        {
          image: "103.jpg",
          priceN: "30 000 FCFA",
          priceR: "40.0000 FCFA",
          name: "Televion togolaise "
        },
        {
          image: "104.jpg",
          priceN: "60 000 FCFA",
          priceR: "320.0000 FCFA",
          name: "Montr moderne a Banger "
        },
        {
          image: "105.jpg",
          priceN: "596 000 FCFA",
          priceR: "2309.0000 FCFA",
          name: "Vetement de sport "
        },
        {
          image: "106.jpg",
          priceN: "496 000 FCFA",
          priceR: "309.0000 FCFA",
          name: "Chaussures de sport "
        },
        {
          image: "107.jpg",
          priceN: "496 000 FCFA",
          priceR: "309.0000 FCFA",
          name: "Chaussures  "
        },
        {
          image: "108.jpg",
          priceN: "496 000 FCFA",
          priceR: "309.0000 FCFA",
          name: "Chaussures  "
        },
        {
          image: "109.jpg",
          priceN: "496 000 FCFA",
          priceR: "309.0000 FCFA",
          name: "Chaussures  "
        },
        {
          image: "110.jpg",
          priceN: "496 000 FCFA",
          priceR: "309.0000 FCFA",
          name: "Chaussures  "
        },
        {
          image: "111.jpg",
          priceN: "30 000 FCFA",
          priceR: "40.0000 FCFA",
          name: "Televion togolaise "
        },
        {
          image: "101.jpg",
          priceN: "60 000 FCFA",
          priceR: "320.0000 FCFA",
          name: "Montr moderne a Banger "
        },
        {
          image: "107.jpg",
          priceN: "596 000 FCFA",
          priceR: "2309.0000 FCFA",
          name: "Vetement de sport "
        },
        {
          image: "114.jpg",
          priceN: "596 000 FCFA",
          priceR: "2309.0000 FCFA",
          name: "Vetement de sport "
        }
      ],
      products2: [
        {
          image: "102.jpg",
          priceN: "10 000 FCFA",
          priceR: "100.0000 FCFA",
          name: "Appareil mobile"
        },
        {
          image: "103.jpg",
          priceN: "30 000 FCFA",
          priceR: "40.0000 FCFA",
          name: "Televion togolaise "
        },
        {
          image: "104.jpg",
          priceN: "60 000 FCFA",
          priceR: "320.0000 FCFA",
          name: "Montr moderne a Banger "
        },
        {
          image: "105.jpg",
          priceN: "596 000 FCFA",
          priceR: "2309.0000 FCFA",
          name: "Vetement de sport "
        },
        {
          image: "106.jpg",
          priceN: "496 000 FCFA",
          priceR: "309.0000 FCFA",
          name: "Chaussures de sport "
        },
        {
          image: "107.jpg",
          priceN: "496 000 FCFA",
          priceR: "309.0000 FCFA",
          name: "Chaussures  "
        }
      ]
    };
  },
  methods: {
    changer(n) {
      this.affiche = n;
    },
    carroussel() {
      this.affiche = this.affiche == 5 ? 1 : this.affiche + 1;
    }
  },
  created() {
    setInterval(() => {
      this.carroussel();
    }, 5000);
    setInterval(() => {
      this.dateRemain = this.expireIn - Math.round(Date.now() / 1000);
    }, 1000);
  }
};
</script>


<style scoped>
.banner {
  margin-top: 80px;
  height: 392px;
  justify-content: center;
}

.v-application {
  background-color: #f5f5f5;
}
</style>


