<template>
  <div>
    <h2
      class="ml-3"
      style="font-size: 14px;font-weight: 500;height:25px;color: #282828; "
    >LIVRAISON ET RETOUR</h2>
    <div class="hr">
      <hr class="interline" style="height:1px" />
    </div>
    <h2
      class="mt-2 express-shippment ml-3"
      style="font-size: 12px;font-weight: 500;height:25px;color: #282828; "
    >JUMIA EXPRESS</h2>
    <p
      class="shippment-place ml-3 mt-0"
      style="font-size: 12px;font-weight: 400;height: 20px;color: #282828; "
    >
      Livraison rapide dans les grandes villes.
      <a>Détails</a>
    </p>
    <div class="hr" style="margin-top:-10px">
      <hr class="interline" style="height:1px" />
    </div>
    <h3
      class="recommandation ml-3 mt-2"
      style="font-size: 15px;font-weight: 500;height: 25px;color: #282828;"
    >Choisissez le lieu</h3>

    <!--First select input -->
    <div class="select mr-2 ml-3 d-flex" style="height:40px ;border-radius:5px;position:relative">
      <div
        class="down-icon"
        style="position:absolute;height:16px;width:16px;right:20px;top:10%;z-index:0"
      >
        <v-img src="/icons/down.svg"></v-img>
      </div>
      <select
        class="pl-5"
        style="height:40px;width:100%;border:none;z-index:3"
        name="cars"
        id="cars"
        form="carform"
      >
        <option value="volvo">Grand Casablanca</option>

        <option value="saab">Tanger Tetouan taza Al Hoceima</option>

        <option value="opel">Fes et Djoula</option>

        <option value="audi">Marrakech -Temara-Rabat</option>
      </select>
    </div>
    <!--End First select input -->

    <!--Second select input -->
    <div
      class="select mt-2 mr-2 ml-3 d-flex"
      style="height:40px ;border-radius:5px;position:relative"
    >
      <div
        class="down-icon"
        style="position:absolute;height:16px;width:16px;right:20px;top:10%;z-index:0"
      >
        <v-img src="/icons/down.svg"></v-img>
      </div>
      <select
        class="pl-5"
        style="height:40px;width:100%;border:none;z-index:3"
        name="cars"
        id="cars"
        form="carform"
      >
        <option value="volvo">Grand Casablanca</option>

        <option value="saab">Tanger Tetouan taza Al Hoceima</option>

        <option value="opel">Fes et Djoula</option>

        <option value="audi">Marrakech -Temara-Rabat</option>
      </select>
    </div>
    <!--End select input -->

    <!--shipment retour -->
    <div class="house-delivery mt-3 ml-3 d-flex">
      <div
        class="icon-wrapper d-flex"
        style="height:40px;width:40px;border:1px solid black;justify-content:center;align-items:center"
      >
        <div class="ico" style="height:25px;width:25px;">
          <v-img src="/icons/car.svg"></v-img>
        </div>
       
      </div>
    </div>
    <!--end articles retour -->
  </div>
</template>


<style scoped>
* {
  color: #282828;
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
}
select:focus {
  border: 1px solid #f68b1e !important;
  outline: none;
}

select {
  font-size: 14px;
  font-weight: 400;
  height: 40px;
  line-height: 19.6px;
  border: 1px solid black !important;
  border-radius: 5px;
}
</style>

