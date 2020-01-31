<template>
    <v-dialog v-model="dialog" persistent max-width="600px">
      <template v-slot:activator="{ on }" ali>
        <v-btn color="primary" dark v-on="on">작성하기</v-btn>
      </template>
      <v-card>
        <v-card-title>
          <span class="headline">Education Video Insert</span>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
              <v-col cols="12">
                <v-text-field label="URL*" required v-model="vod.url"></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field label="Title*" required v-model="vod.title"></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-textarea
                  outlined
                  name="input-7-4"
                  label="Content"
                  value="The Woodman set to work at once, and so sharp was his axe that the tree was soon chopped nearly through."
                  v-model="vod.content"
        ></v-textarea>
              </v-col>
              <v-col cols="12">
                <v-select
                  :items="['기본지식 배우기','견종별 모아보기']"
                  label="Item*"
                  required
                  v-model="vod.item"
                ></v-select>
              </v-col>
            </v-row>
          </v-container>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="blue darken-1" text @click="dialog = false">Close</v-btn>
          <v-btn color="blue darken-1" text @click="insert">insert</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
</template>
<script>
  export default {
    data : function () {
      return {
        dialog: false,
        vod:{
        url: '',
        title: '',
        content: '',
        item: ''
        }
      }
    },
    methods: {
        insert: function (event) {
          this.$http.post('/api/vods/insert',{
            vod: this.vod
          })
          .then((res) => {
            if(res.data.success == true){
              alert(res.data.message);
              this.$router.push(-1)
            }
            if(res.data.success == false){
              alert(res.data.message);
            }
          })
          .catch(function (error) {
            alert('error')
          })
        }
      }
  }
</script>