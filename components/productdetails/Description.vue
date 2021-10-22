<template>
  <div style="width:100%;">
    <!--Details content -->
    <div class="details pt-3" style="border-radius:5px">
      <h5 class="pl-3 details-title">Details</h5>
      <div class="hr">
        <hr class="interline mt-4" style="height:1px" />
      </div>
      <div class="details-content pl-5 pr-5">
        <p>Je vais vous raconter cette histoire.Je vais</p>

        <p>voir ce que vous en pensez ,puis on va terminer le job ensemble</p>
        <p>voir ce que vous en pensez ,puis on va terminer le job ensemble</p>
        <p>voir ce que vous en pensez ,puis on va terminer le job ensemble</p>

        <p>
          <img
            alt
            src="https://ckeditor.com/apps/ckfinder/userfiles/files/0_dtbGisnIfG0utbdi.png"
            style="border-style:solid; border-width:3px; height:142px; margin:4px 23px; width:200px"
          />
        </p>
      </div>
    </div>
    <!-- end Details content -->

    <!--technical Details content -->
    <div class="technical-details mt-5 pt-3 pb-5" style="border-radius:5px">
      <h5 class="pl-3 details-title">Fiche technique</h5>
      <div class="hr">
        <hr class="interline mt-4" style="height:1px" />
      </div>
      <div class="technical-details-content mt-5 pl-5 pr-5 d-flex justify-space-between">
        <div
          class="main-caracteristiques pt-3 pb-3 mb-4"
          style=" border: 1px solid #c7c7cd;;width:49%;border-radius:4px;height:auto"
        >
          <h5 class="main-caracteristique pr-3 pl-3">PRINCIPALES CARACTÉRISTIQUES</h5>
          <div class="hr">
            <hr class="interline mt-4" style="height:1px" />
          </div>
          <div class="real-content pr-3 pl-3" style="height:auto">
            <ul>
              <li>
                Modem:
                <strong>Remis neuf</strong>
              </li>
              <li>
                Batterie
                <strong>&nbsp;:A charge plein</strong>
              </li>
              <li>
                Chargeur
                <strong>:</strong>10 mA
              </li>
            </ul>
          </div>
        </div>
        <div
          class="main-caracteristiques pt-3 pb-3 mb-4"
          style=" border: 1px solid #c7c7cd;;width:49%;border-radius:4px;height:auto"
        >
          <h5 class="main-caracteristique pr-3 pl-3">DESCRIPTIF TECHNIQUE</h5>
          <div class="hr">
            <hr class="interline mt-4" style="height:1px" />
          </div>
          <div class="real-content pr-3 pl-3" style="height:auto">
            <ul>
              <li>
                Modem:
                <strong>Remis neuf</strong>
              </li>
              <li>
                Batterie
                <strong>&nbsp;:A charge plein</strong>
              </li>
              <li>
                Chargeur
                <strong>:</strong>10 mA
              </li>
            </ul>
          </div>
        </div>
        <div
          class="main-caracteristiques pt-3 pb-3 mb-4"
          style=" border: 1px solid #c7c7cd;;width:49%;border-radius:4px;height:auto"
        >
          <h5 class="main-caracteristique pr-3 pl-3">VENDU AVEC LE PRODUIT</h5>
          <div class="hr">
            <hr class="interline mt-4" style="height:1px" />
          </div>
          <div class="real-content pr-3 pl-3" style="height:auto">
            <ul>
              <li>
                Modem:
                <strong>Remis neuf</strong>
              </li>
              <li>
                Batterie
                <strong>&nbsp;:A charge plein</strong>
              </li>
              <li>
                Chargeur
                <strong>:</strong>10 mA
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <!-- end technical Details content -->
  </div>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>

<style scoped>
* {
  font-family: Roboto, -apple-system, BlinkMacSystemFont, "Segoe UI",
    "Helvetica Neue", Arial, sans-serif;
}
.details {
  background: #ffffff;
}

.details-content {
  font-size: 14px;
  font-weight: 400;
}

.details-title {
  font-size: 20px;
  font-weight: 500;
  height: 25px;
}

.interline {
  border: 1px solid #c7c7cd;
  border-bottom: none;
}
.main-caracteristique {
  font-size: 14px;
  font-weight: 500;
  height: 25px;
}

.real-content {
  font-size: 16px;
  font-weight: 400;
  height: 21px;
}

.technical-details {
  background: #ffffff;
}

.technical-details-content {
  font-size: 14px;
  font-weight: 400;
  flex-wrap: wrap;
}

.technical-details-title {
  font-size: 20px;
  font-weight: 500;
  height: 25px;
}
</style>
