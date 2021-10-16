<template>
  <div class="pt-3 " style="background:#ffffff;">
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
        <option v-for="city in cities" :key="city.id" :value="city">{{city.name}}</option>
      </select>
    </div>
    <!--End First select input -->

    <!--Second select input -->
    <div
      class="select mt-2 mr-2 ml-3 d-flex mb-4"
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
        <option v-for="city in cities" :key="city.id" :value="city">{{city.name}}</option>
      </select>
    </div>
    <!--End select input -->

    <!--shipment delivery -->
    <div
      class="house-delivery ml-3 d-flex"
      style="align-items:start"
      v-for="shipment in shipments"
      :key="shipment.id"
    >
      <!--icon wrapper -->
      <div class="icon-wrapper d-flex">
        <div class="ico" style="height:25px;width:25px;">
          <v-img :src="shipment.icon"></v-img>
        </div>
      </div>
      <!--end icon-wrapper -->

      <!--infos shipment wrapper -->
      <div class="infos-shipment-wrapper mr-3" style="width:100%">
        <!--main title -->
        <div
          class="main-title d-flex"
          style="align-items:center;justify-content:space-between;width:100%;"
        >
          <h3
            class="recommandation ml-3"
            style="font-size: 13px;font-weight: 500;color: #282828;"
          >{{shipment.title}}</h3>
          <a class="details" href="#">Details</a>
        </div>
        <!--end main title -->
        <!--shipment price -->
        <div class="shipment-price">
          <p
            class="shippment-place ml-3 mt-0 mb-0"
            style="font-size: 12px;font-weight: 400;height: 20px;color: #282828; "
          >
            Livraison
            <span style="font-weight:600">{{shipment.price}} Dhs</span>
          </p>
        </div>
        <!--end shipment price -->
        <!--shipment extra infos -->
        <div class="shipment-extra-infos">
          <p
            class="shippment-extra-infos-content ml-3 mt-0"
            style="font-size: 12px;font-weight: 400;color: #282828; "
          >{{shipment.infos}}</p>
        </div>
        <!--end shipment extra infos -->
      </div>
      <!--end infos shipment -->
    </div>
    <!--end articles delivery -->
    <div class="hr" style="margin-top:-10px">
      <hr class="interline" style="height:1px" />
    </div>
    <!--Return policy -->
    <div class="mt-3">
      <div
        class="house-delivery ml-3 d-flex"
        style="align-items:start"
        v-for="policy in policies"
        :key="policy.id"
      >
        <!--icon wrapper -->
        <div class="icon-wrapper d-flex">
          <div class="ico" style="height:25px;width:25px;">
            <v-img :src="policy.icon"></v-img>
          </div>
        </div>
        <!--end icon-wrapper -->

        <!--infos shipment wrapper -->
        <div class="infos-shipment-wrapper mr-3" style="width:100%">
          <!--main title -->
          <div
            class="main-title d-flex"
            style="align-items:center;justify-content:space-between;width:100%;"
          >
            <h3
              class="recommandation ml-3"
              style="font-size: 13px;font-weight: 500;color: #282828;"
            >{{policy.title}}</h3>
          </div>
          <!--end main title -->

          <!--shipment extra infos -->
          <div class="shipment-extra-infos">
            <p
              class="shippment-extra-infos-content ml-3 mt-0"
              style="font-size: 12px;font-weight: 400;color: #282828; "
            >
              {{policy.infos}}
              <a class="details" href="#">En savoir plus</a>
            </p>
          </div>
          <!--end shipment extra infos -->
        </div>
        <!--end infos shipment -->
      </div>
    </div>
    <!--end return  policy -->
  </div>
</template>
<script>
export default {
  props: {
    cities: Array,
    shipments: Array,
    policies: Array
  }
};
</script>


<style scoped>
* {
  color: #282828;
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
}

a {
  text-decoration: none;
  font-size: 12px;
  font-weight: 400;
  height: 20px;
}

.details {
  font-size: 12px;
  font-weight: 400;
  height: 16px;
  color: #264996;
}

.icon-wrapper {
  height: 40px;
  width: 40px;
  border: 1px solid black;
  justify-content: center;
  align-items: center;
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
.shipment-extra-infos-content {
  font-size: 12px;
  font-weight: 400;
  height: 52px;
  line-height: normal;
}
</style>

