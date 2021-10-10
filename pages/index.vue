<template>
  <v-app>
    <MainHeader />
    <v-main>
      <v-container class="banner d-flex mx-auto mt-3">
        <!--Menu on big devices not include mobile-->
        <v-card flat width="222" class="mr-3">
          <v-list style="background:#ffffff">
            <span v-for="item in items" :key="item.title" class="d-flex" style="padding-left:8px">
              <v-list-item-content class="menu-item-content" :id="item.icon.split('.')[0]">
                <v-list-item-title class="menu-item">
                  <v-avatar size="16" class="mr-1">
                    <v-img :src="'/iconsmenu/' + item.icon"></v-img>
                  </v-avatar>
                  {{ item.title }}
                </v-list-item-title>
              </v-list-item-content>
            </span>
          </v-list>
        </v-card>

        <!--End menu-->

        <!--Caroussel-->
        <v-card flat height="384" width="712">
          <!-- carroussel Buttons-->
          <div class="arrows d-flex">
            <a v-for="n in 5" :key="n">
              <v-icon
                v-on:click="changer(n)"
                class="icon"
                :class="{ active: affiche == n }"
              >mdi-checkbox-blank-circle-outline</v-icon>
            </a>
          </div>
          <!--End caroussel buttons-->
          <transition name="component-fade" mode="out-in">
            <v-img class="c-image" v-show="affiche == 1" src="/5.png"></v-img>
          </transition>

          <transition name="component-fade" mode="out-in">
            <v-img class="c-image" v-show="affiche == 2" src="/2.jpg"></v-img>
          </transition>

          <transition name="component-fade" mode="out-in">
            <v-img class="c-image" v-show="affiche == 3" src="/3.jpg"></v-img>
          </transition>

          <transition name="component-fade" mode="out-in">
            <v-img class="c-image" v-show="affiche == 4" src="/6.jpg"></v-img>
          </transition>

          <transition name="component-fade" mode="out-in">
            <v-img class="c-image" v-show="affiche == 5" src="/7.jpg"></v-img>
          </transition>
        </v-card>
        <!--End Caroussel-->

        <!--Right column-->
        <div class="d-block ml-3">
          <v-card width="218" height="auto" style="border-radius:5px" class="mb-4">
            <div
              class="list-wrapper d-flex pt-4 pl-2"
              style="padding-bottom:14.5px"
              v-for="info in infos"
              :key="info.title"
            >
              <v-avatar size="30" class="mr-3">
                <v-img :src="'/' + info.image"></v-img>
              </v-avatar>
              <div class="list-content d-block">
                <h4 class="pb-0 m-0 infotitle">{{ info.title }}</h4>
                <h5 class="pt-0 mt-0 infosubtitle">{{ info.info }}</h5>
              </div>
            </div>
          </v-card>
          <v-img style="border-radius:5px" src="/4.jpg" width="auto" height="auto"></v-img>
        </div>
        <!--End Right column-->
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      affiche: 1,
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
/*a*/
.active {
  background: #f68b1e !important;
  border-radius: 100%;
  color: #f68b1e !important;
}
.arrows {
  position: absolute;
  z-index: 10;
  left: 45%;
  bottom: 15px;
}
/*b*/
.banner {
  margin-top: 80px;
  height: 392px;
}

/*c*/
.card {
  position: relative;
}
.carroussel-card {
  height: inherit;
  width: auto;
  position: relative;
}
.c-image {
  position: absolute;
  height: auto;
  width: auto;
  border-radius: 5px;
}
.component-fade-enter-active,
.component-fade-leave-active {
  transition: opacity 0.7s ease;
}
.component-fade-enter, .component-fade-leave-to
/* .component-fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
/*i*/
.icon {
  font-size: 8px;
  margin-left: 8px;
  background: #c7c7cd;
  border-radius: 100%;
  color: #c7c7cd;
}
.infosubtitle {
  font-size: 12px;
  font-weight: 400 !important;
}
.infotitle {
  font-size: 14px;
  font-weight: 500 !important;
}

/*m*/
.menu {
  padding-bottom: 0px !important;
}
.menu-item-content {
  margin-bottom: 16px;
  padding-bottom: 0px;
  padding-top: 0px;
}

.menu-item:hover {
  color: #f68b1e;
}
.menu-item {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
  font-weight: 400;
  padding: 0px;
  margin: 0px;
  line-height: normal;
  font-size: 12px !important;
  color: #282828;
}
/*v*/
.v-application {
  background-color: #f5f5f5;
}
</style>


