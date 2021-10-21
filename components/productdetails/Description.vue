<template>
  <div style="width:100%;">
    <!--Details content -->
    <div class="details pt-3">
      <h5 class="pl-3 details-title">Details</h5>
      <div class="hr">
        <hr class="interline mt-4" style="height:1px" />
      </div>
      <div class="details-content pl-5 pr-5">
        <p>Je vais vous raconter cette histoire.Je vais</p>

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
    <div class="technical-details mt-5 pt-3 pb-5">
      <h5 class="pl-3 details-title">Fiche technique</h5>
      <div class="hr">
        <hr class="interline mt-4" style="height:1px" />
      </div>
      <div class="technical-details-content mt-5 pl-5 pr-5 d-flex justify-space-between">
        <div
          class="main-caracteristiques pr-3 pl-3 pt-3 pb-3"
          style="border:1px solid gray;width:49%;border-radius:4px"
        >
        <h5>PRINCIPALES CARACTÉRISTIQUES</h5>
         <div class="hr">
        <hr class="interline mt-4" style="height:1px" />
        </div>
        <div class="real-content">
           <ul>
             <li>Processeur:2.95 Ghz</li>
           </ul>
        </div>
        </div>
        <div
          class="descriptif-caracteristiques"
          style="border:1px solid gray;width:49%;border-radius:4px"
        >jE NE sais pas</div>
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
.technical-details {
  background: #ffffff;
}

.technical-details-content {
  font-size: 14px;
  font-weight: 400;
}

.technical-details-title {
  font-size: 20px;
  font-weight: 500;
  height: 25px;
}
</style>
