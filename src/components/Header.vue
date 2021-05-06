<template>
  <div>
    <v-navigation-drawer class="hidden-md-and-up" app v-model="drawer" mobile-breakpoint="1920">
      <v-list dense>
        <v-list-group
          class="hidden-md-and-up"
          v-for="nav_list in nav_lists"
          :key="nav_list.name"
          :prepend-icon="nav_list.icon"
          no-action
          :append-icon="nav_list.lists ? undefined : ''"
        >
          <template v-slot:activator>
            <v-list-item :to="nav_list.link">
              <v-list-item-title>{{ nav_list.name }}</v-list-item-title>
            </v-list-item>
          </template>
        </v-list-group>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar color="accent-4" dense dark fixed app>
      <v-toolbar-title style="overflow:initial; padding-left:0;">Morishita Riku Portfolio</v-toolbar-title>

      <v-tabs right class="hidden-sm-and-down">
        <v-tab v-for="nav_list in nav_lists" :key="nav_list.name" :to="nav_list.link">{{ nav_list.name }}</v-tab>
      </v-tabs>
      <v-spacer></v-spacer>
      <v-app-bar-nav-icon right class="hidden-md-and-up" @click="drawer = !drawer"></v-app-bar-nav-icon>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      drawer: null,
      nav_lists: [
        {
          name: "HOME",
          icon: "mdi-home",
          link: "/",
        },
        {
          name: "ABOUT",
          icon: "mdi-information",
          link: "/about",
        },
        {
          name: "WORK",
          icon: "mdi-semantic-web",
          link: "work",
        },
        {
          name: "CONTACT",
          icon: "mdi-human-greeting-proximity",
          link: "/contact",
        },
      ],
    };
  },
};
</script>
