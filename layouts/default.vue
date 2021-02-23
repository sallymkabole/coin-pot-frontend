<template>
      <v-app class="bg">
        <v-app-bar app color="primary" dark elevation="0">
            <v-app-bar-nav-icon @click.stop="sidebarMenu = !sidebarMenu"></v-app-bar-nav-icon>
            <v-spacer></v-spacer>
            <v-icon>mdi-account</v-icon>
        </v-app-bar>
        <v-navigation-drawer 
            v-model="sidebarMenu" 
            app
            floating
            :permanent="sidebarMenu"
            :mini-variant.sync="mini"
            class="nav-drawer"
            >
            <v-list dense color="primary" dark>
                <v-list-item>
                    <v-list-item-action>
                        <v-icon @click.stop="sidebarMenu = !sidebarMenu">mdi-chevron-left</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                        <v-list-item-title>
                            <h3 class="font-weight-thin">Vuetify Dashboard</h3>
                        </v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
            <v-list-item class="px-2" @click="toggleMini = !toggleMini">
                <v-list-item-avatar>
                    <v-icon  class="white">mdi-account-outline</v-icon>
                </v-list-item-avatar>
                <v-list-item-content class="text-truncate white--text">
                    Jane Githinji
                </v-list-item-content>
                <v-btn icon small>
                    <v-icon>mdi-chevron-left</v-icon>
                </v-btn>
            </v-list-item>
            <v-divider></v-divider>
            <v-list>
                <v-list-item v-for="item in items" :key="item.title" link :to="item.href">
                    <v-list-item-icon>
                        <v-icon color="white">{{ item.icon }}</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <v-list-item-title class="white--text font-weight-thin">{{ item.title }}</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
        <v-content>
            <v-container class="px-4 py-0 fill-height" fluid>
                <nuxt/>
            </v-container>
        </v-content>
        <v-footer class="py-3">
            <span class="ml-auto overline">CoinPot &copy;2021</span>
        </v-footer>
    </v-app>
</template>

<script>
export default {
    computed: {
    mini() {
        return (this.$vuetify.breakpoint.smAndDown) || this.toggleMini
    },
    buttonText() {
        return !this.$vuetify.theme.dark ? 'Go Dark' : 'Go Light'
    }
  },
  data() {
    return {
      sidebarMenu: true,
      toggleMini: false,
      fixed: false,
      sidebarMenu: true,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/",
        },
        {
          icon: "mdi-chart-bubble",
          title: "Buy Coins",
          to: "/buycoins",
        },
        {
          icon: "mdi-chart-bubble",
          title: "Sell Coins",
          to: "/sellcoins",
        },
        {
          icon: "mdi-chart-bubble",
          title: "Bought Coins",
          to: "/boughtcoins",
        },
        {
          icon: "mdi-chart-bubble",
          title: " Referrals",
          to: "/referrals",
        },
        {
          icon: "mdi-chart-bubble",
          title: "How It Works",
          to: "/howitworks",
        },
        {
          icon: "mdi-chart-bubble",
          title: "My Wallet",
          to: "/mywallet",
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js",
    };
  },
};
</script>
<style scoped>
.bg {
  background-color: #161d31;
}
.nav-drawer {
  background-color: #26314c;
}

</style>
