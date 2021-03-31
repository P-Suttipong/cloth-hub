<template>
  <q-layout view="hHh lpR fFf">
    <q-header bordered class="page text-white header-border">
      <q-toolbar>
        <!-- <q-btn dense flat round icon="menu" @click="left = !left" /> -->

        <q-toolbar-title>
          <img class="logo" src="~assets/ClothHubLogo.png" />
        </q-toolbar-title>

        <div>
          <q-btn>Login</q-btn>
          <q-btn>Register</q-btn>
          <q-btn><i class="fas fa-shopping-cart fa-lg"></i></q-btn>
          <q-btn><i class="fas fa-bars fa-lg"></i></q-btn>
        </div>
      </q-toolbar>
    </q-header>

    <q-drawer
      content-class="bg-black text-white"
      show-if-above
      v-model="left"
      side="left"
    >
      <div class="q-mt-lg row">
        <p class="main-btn">Popular Shop</p>
        <p class="main-btn">Children Cloth</p>
        <p class="main-btn">Men Cloth</p>
        <p class="main-btn">Women Cloth</p>
        <p class="main-btn">Shoes</p>
        <p class="main-btn">Watches</p>
        <p class="main-btn">Dressing</p>
        <p class="main-btn">Swimwear</p>
      </div>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  data() {
    return {
      left: false
    };
  }
};
</script>

<style scoped>
.page {
  background-color: black;
}

.header-border {
  border-bottom: 3px solid white;
}

.logo {
  width: 250px;
}

.drawer {
  background-color: black;
}
.main-btn {
  letter-spacing: 3px;
  font-size: 16px;
  width: 200px;
  padding: 10px 0px 10px 30px;
  margin-bottom: 0px;
}
.main-btn:hover {
  background-color: #303030;
  color: white;
  letter-spacing: 3px;
  font-size: 16px;
  width: 200px;
  padding: 10px 0px 10px 30px;
  margin-bottom: 0px;
  cursor: pointer;
}
</style>
