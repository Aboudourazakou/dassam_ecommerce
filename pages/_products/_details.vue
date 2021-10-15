<template>
  <v-app>
    <SecondHeader />
    <v-main>
      <v-container class="main-wrapper d-flex justify-center mt-5" style="background:#ffffff">
        <div class="wrapper d-flex" style="width:1160px">
          <div class="left-card d-flex justify-center" style="width:70%;">
            <ProductdetailsProductCard/>
            <ProductdetailsProductinfos />
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
* {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
}
/*c*/

.v-application {
  background-color: #f5f5f5;
}
</style>
