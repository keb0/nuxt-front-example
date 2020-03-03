<template>
  <v-app>
    <v-app-bar fixed app>
      <v-app-bar-nav-icon
        class="hidden-md-and-up"
        @click="drawer = !drawer"
      ></v-app-bar-nav-icon>
      <v-toolbar-title>Title</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items
        v-for="(item, i) in items"
        :key="i"
        class="hidden-sm-and-down"
      >
        <v-btn link :to="item.to">{{ item.title }} </v-btn>
      </v-toolbar-items>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app>
      <v-list nav>
        <v-list-item v-for="(item, i) in items" :key="i" :to="item.to"
          ><v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" /> </v-list-item-content
        ></v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <v-footer color="primary" dark app>
      Vuetify
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    items: [
      { title: 'Home', icon: 'fa-home', to: '/' },
      { title: 'About', icon: 'fa-question', to: '/about' },
      { title: 'Test', icon: 'fa-search', to: '/test' }
    ]
  })
}
</script>
