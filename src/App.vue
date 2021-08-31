<template>
  <v-app>
    <!--　header　-->
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-app-bar-nav-icon @click="drawer = true">
        </v-app-bar-nav-icon>
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="../src/assets/logo.png"
          transition="scale-transition"
          width="50"
        />
        </div>
        <div class="text-h4 -weight-medium">
          Portfolio
        </div>
      <v-spacer></v-spacer>
    </v-app-bar>
    <!--　nav展開部　-->
    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>
          <!--<v-list-item>-->
          <!--  <v-list-item-icon>-->
          <!--    <v-icon>mdi-account</v-icon>-->
          <!--  </v-list-item-icon>-->
          <!--  <v-list-item-title>Account</v-list-item-title>-->
          <!--</v-list-item>-->
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <!--　メインコンテンツ描画 -->
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    drawer: false,
    group: null,
  }),
};
</script>
