<template>
  <div>
    <div class="supplier mt-3 pt-3 pb-5" style="background:#ffffff;border-radius:5px">
      <!--main title -->
      <div
        class="main-title d-flex pr-3 pl-3"
        style="align-items:center;justify-content:space-between;width:100%;"
      >
        <h3
          style="font-size: 14px;font-weight: 500;height:25px;color: #282828; "
        >INFORMATIONS SUR LE VENDEUR</h3>

        <div class="img" style="height:12px;width:12px;cursor:pointer">
          <v-img src="/icons/arrow-right-black.svg"></v-img>
        </div>
      </div>
      <!--end main title -->
      <div class="hr">
        <hr class="interline" style="height:1px" />
      </div>
      <!--supplier name -->
      <h3
        class="supplier-name ml-3 mt-2"
        style="font-size: 15px;font-weight: 500;color: #282828;"
      >Tetereou Aboudourazakou</h3>
      <!-- end supplier name -->
      <!--supplier follower -->
      <div class="supplier-followers ml-3 mt-3 d-flex mr-3" style="justify-content:space-between">
        <div>
          <p class="mb-0" style="font-size: 12px;font-weight: 400;color: #282828;">
            <span style="font-weight:500">80%</span> Evaluation vendeur
          </p>
          <p style="font-size: 12px;font-weight: 400;color: #282828;" class="mt-0">
            <span style="font-weight:500">378</span> Abonnés
          </p>
        </div>
        <div class="follow-btn">
          <v-btn
            class="btn-follow ml-2"
            elevation="5"
            height="30"
            style=" background: #e4811c !important;"
          >Suivre</v-btn>
        </div>
      </div>
      <!--end supplier follower -->
      <div class="hr">
        <hr class="interline" style="height:1px" />
      </div>

      <!-- supplier performances -->
      <div>
        <!-- title -->
        <div
          class="d-flex justify-content-space-between align-items-center mr-3"
          style="align-items:center;justify-content:start"
        >
          <h3
            class="supplier-name ml-3 mt-2"
            style="font-size: 15px;font-weight: 500;color: #282828;"
          >Performances vendeur</h3>
          <div class="exclamation-icon mt-2 ml-2" style="height:16px;width:16px;cursor:pointer">
            <v-img class="svg" src="/icons/exclamation.svg"></v-img>
          </div>
        </div>
        <!--title -->
        <div class="mr-3 ml-3 mt-3">
          <div class="skills-rating d-flex" v-for="i in 3" :key="i">
            <div class="skills-icon" style="height:16px;width:16px">
              <v-img src="/icons/star.svg"></v-img>
            </div>
            <p class="ml-2 mb-1" style="font-size: 12px;font-weight: 400;color: #282828;">
              Taux d'expedition des commandes :
              <span style="font-weight:600">Excellent</span>
            </p>
          </div>
        </div>
      </div>
      <!--end supplier performances -->
    </div>

    <!--suggestion to become supplier -->
    <div class="suggestion pt-3 mt-3" style="background:#ffffff;border-radius:5px;">
      <div class="supplier-followers ml-3 mt-3 d-flex mr-3" style="justify-content:space-between;">
        <div>
          <p class="mb-0" style="font-size: 12px;font-weight: 500;color: #282828;">Vous en avez un?</p>
          <p
            style="font-size: 11px;font-weight: 300;color: #282828;cursor:pointer"
            class="mt-0"
          >Cliquer ici pour le vendre</p>
        </div>
        <div class="img" style="height:12px;width:12px;cursor:pointer">
          <v-img src="/icons/arrow-right-black.svg"></v-img>
        </div>
      </div>
    </div>
    <!-- end suggestion to become supplier -->
  </div>
</template>
<style >
* {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
}

html{
   scroll-behavior: smooth!important;
}

.interline {
  border: 1px solid #c7c7cd;
  border-bottom: none;
}
.svg :hover path {
  fill: #e4811c;
}
</style>
