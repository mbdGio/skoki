<template>
  <v-app>
    <v-card color="grey lighten-4" flat height="100px">
        <v-toolbar :color='primary' :dark='true'>
          <v-app-bar-nav-icon></v-app-bar-nav-icon>
          <v-toolbar-title>Ski Chart</v-toolbar-title>
          <v-spacer></v-spacer>
          <v-btn icon>
            <v-icon>mdi-bluetooth</v-icon>
          </v-btn>
          <v-btn icon>
            <v-icon>mdi-content-save-settings</v-icon>
          </v-btn>
          <v-btn icon>
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </v-toolbar>
      </v-card>
    <v-content>
      <SkiChart/>
    </v-content>
  </v-app>
</template>

<script>
import SkiChart from './components/SkiChart';

export default {
  name: 'App',

  components: {
    SkiChart,
  },

  data: () => ({
    //
  }),
};
</script>
