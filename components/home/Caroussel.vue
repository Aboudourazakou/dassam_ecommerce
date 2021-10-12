<template>
  <!--Caroussel-->
  <v-card flat width="712" class="card-caroussel">
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

    <!--Arrow right-->
    <div class="arrow-right d-flex">
      <v-fab-transition>
        <v-btn fab small dark class="v-btn--example" v-on:click="next()">
          <v-avatar size="12">
            <v-img src="/icons/arrow-right.svg"></v-img>
          </v-avatar>
        </v-btn>
      </v-fab-transition>
    </div>
    <!--End arrow right-->
    <!--Arrow left-->
    <div class="arrow-left d-flex">
      <v-fab-transition>
        <v-btn fab small dark class="v-btn--example2" v-on:click="back()">
          <v-avatar size="12">
            <v-img src="/icons/arrow-left.svg"></v-img>
          </v-avatar>
        </v-btn>
      </v-fab-transition>
    </div>
    <!--End arrow left-->
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
</template>

<script>
export default {
  components: true,
  data() {
    return {
      affiche: 1
    };
  },
  methods: {

   
    back() {
      this.affiche = this.affiche == 1 ? 5 : this.affiche - 1;
    },

    next() {
      this.affiche = this.affiche == 5 ? 1 : this.affiche + 1;
    },
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
.arrow-right {
  position: absolute;
  right: 0px;
  z-index: 10;
  width: 15%;
  height: 100%;
  justify-content: right;
  align-items: center;
  padding-right: 15px;
}
.arrow-left {
  position: absolute;
  left: 0px;
  z-index: 10;
  width: 15%;
  height: 100%;
  justify-content: left;
  align-items: center;
  padding-left: 15px;
}
.v-btn--example {
  display: none;
}
.v-btn--example2 {
  display: none;
}
.arrow-right:hover .v-btn--example {
  display: block;
}
.arrow-left:hover .v-btn--example2 {
  display: block;
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
.card-caroussel {
  height: 390px;
  position: relative;
}
.c-image {
  position: absolute;
  height: 100%;
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

/*v*/
.v-application {
  background-color: #f5f5f5;
}
</style>

