<template>
  <v-app>
    <MainHeader />
    <v-main>


      <!--Banner container -->
      <v-container class="banner d-flex mx-auto mt-3">

        <!--Menu on big devices not include mobile containing categories-->
           <HomeCategories  :items="items"/>
        <!--End menu-->

       <!--Caroussel-->
       <HomeCaroussel/>
       <!--End Caroussel-->

        <!--Right column-->
        <HomeBannerRightColumn :infos="infos"/>
        <!--End Right column-->

      </v-container>
      <!--End banner container-->

       <!--Container for differents services -->
       <HomeServices :services="services"/>
       <!--End container for differents services-->
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      affiche: 1,
         services: [
        {
          title: "Nos marques",
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
}

.v-application {
  background-color: #f5f5f5;
}
</style>


