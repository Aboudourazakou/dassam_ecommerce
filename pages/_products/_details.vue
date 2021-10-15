<template>
  <v-app>
    <SecondHeader />
    <v-main>
      <v-container class="main-wrapper d-flex justify-center" style="background:green">
        <div class="wrapper d-flex" style="width:1160px">
          <div class="left-card d-flex justify-center" style="width:70%;background:red">
            <div class="product-card" style="width:40%;background:gray">product</div>
            <div class="product-infos" style="width:60%;background:white">
              <div class="chip">
                <p
                  style="background-color: #b60000;max-width:124px;font-size: 14px;
                font-weight: 500;height: 20px;line-height: 16.8px;margin: 8px 0px 0px;padding: 0px 4px;"
                >Boutique officielle</p>
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
            </div>
          </div>

          <div class="right-card" style="width:30%;background:blue">Oui,je suis ici</div>
        </div>
      </v-container>
    </v-main>
  </v-app>
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
/*a*/
a {
  text-decoration: none;
}
/*c*/
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
.v-application {
  background-color: #f5f5f5;
}
</style>
