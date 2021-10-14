<template>
  <!-- App.vue -->

  <!--App-bar-->
  <v-container fluid class="header-container">
    <v-card class="header-card" height="72" flat>
      <v-container class="d-flex mx-auto" style="justify-content:center;position:relative">
        <!--Logo Dunia-->
        <div class="logo-wrapper d-flex" style="align-items:center;position:relative">
          <!--Categories--->
          <div
            @mouseover="displayCategories()"
            @mouseleave="disableCategories()"
            class="categories"
            id="categories"
            style="position:absolute;bottom:-400px;padding-top:20px;margin-top:-20px"
          >
            <div class="list-categories" id="list-categories">
              <HomeCategories :items="items" />
            </div>
          </div>
          <!--End Categories -->
          <div
            class="brand"
           
            @mouseover="displayCategories()"
            @mouseleave="disableCategories()"
          >
            <v-img src="/icons/brand.svg"></v-img>
          </div>
          <div class="logo">
            <v-img src="/dunia.jpeg" />
          </div>
        </div>
        <!--End logo Dunia-->
        <!--Search bar-->
        <div class="find d-flex">
          <div class="search">
            <v-img src="/shop/search.svg"></v-img>
          </div>
          <input
            class="input"
            type="text"
            placeholder="Chercher un produit,une marque,ou une categorie"
          />
        </div>
        <!-- End search bar-->
        <!--Search button-->
        <div>
          <v-btn class="btn-search ml-2" elevation="5" height="40">Rechercher</v-btn>
        </div>
        <!--End search button-->

        <!--logged in user icon and indications-->
        <div class="user d-flex ml-3">
          <v-img src="/shop/user.svg"></v-img>
          <h3 class="username d-inline-block text-truncate">Bonjour, Aboudourazakou</h3>
          <v-img height="5px" src="/shop/dropdown.svg"></v-img>
        </div>
        <div class="help d-flex ml-3">
          <v-img src="/shop/help.svg" class="mr-2"></v-img>
          <h3>Aide</h3>
          <v-img src="/shop/dropdown.svg"></v-img>
        </div>
        <div class="basket d-flex mt-2">
          <v-badge color="#f68b1e" content="5" overlap>
            <v-img src="/shop/basket.svg"></v-img>
          </v-badge>
          <h3 class="ml-3">Panier</h3>
        </div>
        <!--end logged in icon and indications -->
      </v-container>
      <!--End menu container-->

      <!--menu container-->
    </v-card>
  </v-container>
  <!--End App-bar-->
</template>


<script>
export default {
  data() {
    return {
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
    displayCategories() {
      document.getElementById("list-categories").style.display = "block";
    },
    disableCategories() {
      document.getElementById("list-categories").style.display = "none";
    }
  }
};
</script>




<style scoped>
/*a*/
a {
  list-style: none;
  text-decoration: none;
  color: black;
}

/*c*/

/*b*/
.basket > h3 {
  font-size: 16px;
  font-weight: 500;
  color: #000000;
}

.btn-search {
  background: #e4811c !important;
  color: #ffffff;
  font-size: 14px;
}
.brand {
  cursor: pointer;
}

/*c*/
.cat::before {
  content: "";
  top: -20px;
  left: 0px;
  position: absolute;
  border: 10px solid transparent;
  border-bottom-color: white;
}
.list-categories {
  display: none;
  width: 218px;
  padding-right: 0px;
  box-shadow: 0 -2px 20px rgba(0, 0, 0, 0.12), 0px 4px 8px rgba(0, 0, 0, 0.06);
}

/*d*/
/*e*/
/*f*/
.find {
  align-items: center;
  border-radius: 5px;
  border: 1px solid #c7c7cd;
  background: rgba(0, 0, 0, 0) none repeat scroll 0% 0% / auto padding-box
    border-box;
  background-attachment: scroll;
  background-image: none;
  background-position: 0% 0%;
  background-repeat: repeat;
  color: #282828;
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
  font-size: 14px;
  font-weight: 400;
  height: 40px;
  line-height: normal;
  margin: 0px;
  padding: 0px;
  width: 350px;
}
/*g*/
/*h*/
.header-card {
  background: #ffffff;
}
.header-container {
  padding: 0;
}
.help {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  font-weight: 500;
  height: 40px;
  line-height: normal;
  margin: 0px;
  padding: 10px;
  width: 107px;
}
.help > h3 {
  font-size: 16px;
  font-weight: 500;
  color: #000000;
}
/*i*/
.input {
  border: none;
  background: rgb(255, 255, 255) none repeat scroll 0% 0% / auto padding-box
    border-box;
  background-attachment: scroll;
  background-color: #ffffff;
  background-image: none;
  background-position: 0% 0%;
  background-repeat: repeat;
  color: #000000;
  font-family: Arial;
  font-size: 16px;
  font-weight: 400;
  height: 38px;
  line-height: normal;
  margin: 0px 8px 0px 0px;
  padding: 1px 2px;
  width: 399px;
}
input:focus {
  outline: none !important;
}
/*j*/
/*k*/
/*l*/
.logo {
  width: 180px;
}

.logo-wrapper {
  width: 190px;
  padding-left: 0px;
  margin-left: 0px;
  margin-right: 25px;
}

/*m*/
/*n*/
/*o*/
/*p*/
::placeholder {
  text-overflow: ellipsis;
}
[placeholder] {
  text-overflow: ellipsis;
}
/*q*/
/*r*/
/*s*/
.search {
  margin: 0px 8px;
  align-items: center;
}
/*t*/
/*u*/
.user {
  align-items: center;
  text-transform: capitalize;
}
.username {
  background: rgba(0, 0, 0, 0) none repeat scroll 0% 0% / auto padding-box
    border-box;
  background-attachment: scroll;
  background-repeat: repeat;
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  font-weight: 500;
  height: 40px;
  line-height: normal;
  padding: 10px;
  width: 183px;
  color: #000000;
}
.username:hover {
  color: #f68b1e;
}
/*v*/
/*w*/
/*x*/
</style>

