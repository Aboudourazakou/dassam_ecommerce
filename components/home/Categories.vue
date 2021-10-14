<template>
  <v-card rounded flat width="220" color="white" class="cat mr-3" id="cat">
    <v-list color="white" class="list">
      <div
        v-for="item in items"
        :key="item.title"
        class="d-flex list-wrapper"
        style="padding-left:8px;"
      >
        <v-list-item-content class="menu-item-content" :id="item.icon.split('.')[0]">
          <v-list-item-title class="menu-item">
            <v-avatar size="16" class="mr-1">
              <v-img :src="'/iconsmenu/' + item.icon"></v-img>
            </v-avatar>
            {{ item.title }}
          </v-list-item-title>
        </v-list-item-content>
      </div>
    </v-list>
  </v-card>
</template>

<script>
export default {
  props: {
    items: Array
  }
};
</script>

<style >
/*c*/
.card {
  position: relative;
}

/*i*/
.icon {
  font-size: 8px;
  margin-left: 8px;
  background: #c7c7cd;
  border-radius: 100%;
  color: #c7c7cd;
}

/*m*/
.menu {
  padding-bottom: 0px !important;
}
.menu-item-content {
  margin-bottom: 15px;
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
.list-wrapper {
  cursor: pointer;
}

</style>
