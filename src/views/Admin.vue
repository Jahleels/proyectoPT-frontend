<template>
  <v-card
    class="mx-auto overflow-hidden" height="100%"
  >
    <v-app-bar
      color="indigo lighten-1"
      dark
    >
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

      <v-toolbar-title>Administracion</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn text @click="salir">
        <span class="mr-2">Salir</span>
        <v-icon>mdi-logout</v-icon>
      </v-btn>
    </v-app-bar>

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
          <v-list-item exact :to="{name: 'Home'}">
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Inicio</v-list-item-title>
          </v-list-item>

          <v-list-item 
          v-if="isAdmin"
          exact :to="{name: 'Admin'}">
            <v-list-item-icon>
              <v-icon>mdi-shield-key</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Admin</v-list-item-title>
          </v-list-item>

          <v-list-item :to="{name: 'Usuarios'}">
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Usuarios</v-list-item-title>
          </v-list-item>

          <v-list-item :to="{name: 'Consultantes'}">
            <v-list-item-icon>
              <v-icon>mdi-account-multiple-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Consultantes</v-list-item-title>
          </v-list-item>

        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container>
        <admin-hello v-if="$route.name === 'Admin'" />
        
        <router-view></router-view>
      </v-container>
    </v-main>
    
  </v-card>
</template>

<script>

import decode from "jwt-decode";
import AdminHello from '../components/AdminHello.vue';

  export default {
  components: { AdminHello },
    name: 'Admin',
    data: () => ({
      drawer: false,
      group: null,
    }),
    computed: {
      isAdmin(){
        let token = decode(localStorage.getItem('token'));
        return token.rol === 'Administrador' ? true : false;
      },
    },
    methods: {
      salir(){
        localStorage.removeItem('token');
        this.$router.push({name: 'Login'})
      }
    }
  };
</script>