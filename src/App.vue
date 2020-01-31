<template>
<v-app>
  <v-card flat>
    <v-toolbar height="100" style="border-bottom: 1px solid #E3DFDE" flat>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <div style="color:orange; cursor:pointer">LOGIN</div>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-toolbar-title><img src="https://ifh.cc/g/ywJDY.png" width="200"></v-toolbar-title>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <div>JOIN</div>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
  </v-toolbar>
  <v-toolbar flat style="border-bottom: 10px solid #E3DFDE" height="50">
    <v-tabs grow centered>
      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
      <v-tab v-for="bar in title" :key="bar.title" :to="bar.to">{{ bar.titleName }}</v-tab>
      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
  </v-tabs>
  </v-toolbar>
  <router-view></router-view>
  <br><br><br><br>

   <v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      class="indigo lighten-1 white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size  ="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-card-text>
    </v-card>
  </v-footer>

  </v-card>
  </v-app>
</template>
<script>
export default {
  data () {
    return {
      title: [
        {
          titleName: 'ABOUT',
          to: '/about'
        },
        {
          titleName: 'STORE',
          to: '/a'
        },
        {
          titleName: 'EDUCATION',
          to: '/education'
        },
        {
          titleName: 'HELP',
          to: '/help'
        },
        {
          titleName: 'Q&A'
        },
        {
          titleName: 'ABOUT',
          to: '/about'
        }
      ],
      icons: [
        'mdi-facebook',
        'mdi-instagram',
        'mdi-google-plus'
      ]
    }
  }
}
</script>
