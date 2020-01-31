<template>
<v-card flat>
  <v-carousel cycle hide-delimiters show-arrows>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    >
    <v-layout align-center>
    <v-flex><div>{{ item.text }}</div></v-flex>
    </v-layout>
    </v-carousel-item>
  </v-carousel>
  <v-toolbar height="220" flat>
    <v-spacer></v-spacer>
    <v-img src="https://ifh.cc/g/L3Zw0.png"
          max-width="300"
          max-height="500"
           position="center"
    ></v-img>
    <v-spacer></v-spacer>
  </v-toolbar>
  <v-container>
    <v-row centered>
    </v-row>
  </v-container>
</v-card>
</template>
<script>
export default {
  data () {
    return {
      items: [
        {
          src: 'https://ifh.cc/g/olWeL.jpg',
          text: 'gdgd'
        },
        {
          src: 'https://ifh.cc/g/3QMao.jpg',
          text: 'gdasdd'
        }
      ]
    }
  }
}
</script>
