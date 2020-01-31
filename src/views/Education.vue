<template>
<v-app>
  <v-container fluid style="padding:0px">
    <v-layout frow wrap>
      <v-flex>
        <v-img src="https://ifh.cc/g/I3TY4.jpg"
          max-height="400" min-height="400">
          <br><br><br><br><br><br>
            <v-card-text align="center" id="title">교육</v-card-text>
            <v-card-text align="center" id="subTitle">반 려 견 과  반 려 인 의  행 복 한  동 행 을  위 해  교 육 강 의 와  우 수 한  교 육  시 설 을  소 개 해  드 립 니 다.</v-card-text>
        </v-img>
      </v-flex>
    </v-layout>
    <v-tabs grow id="tabs" dark>
      <v-tab id="tab" v-for="tabs in tab" :key="tabs.title" :to="tabs.to">{{ tabs.title }}</v-tab>
    </v-tabs>
    <br><br><br><br>
    <v-card align="center" flat>
      <v-img src="https://ifh.cc/g/9ksel.png"
            max-width="250"
            min-width="100"></v-img>
    </v-card>
    <br><br><br><br>
    <!-- <v-row height="150"> -->
      <!-- <v-col cols="12" offset-md="10"> -->
        <div id="app" style="height:100px">
        <v-app>
          <EduVodAll></EduVodAll>
        </v-app>
        </div>
      <!-- </v-col> -->
    <!-- </v-row> -->
  </v-container>
  </v-app>
</template>
<script>
import EduVodAll from '../components/EduVodAll.vue'

export default {
  components: {
    EduVodAll
  },
  data () {
    return {
      tab: [
        {
          title: '전체보기'
        },
        {
          title: '기본지식 배우기'
        },
        {
          title: '견종별 모아보기'
        },
        {
          title: '전문 교육 기관'
        }
      ]
    }
  }
}
</script>
<style>
#tab{
  /* background-color:azure; */
  color: white;
  border-right: 0.5px solid gray;
}
#title{
  color:white;
  font-size:40px;
}
#subTitle{
  color:white;
  font-size:15px;
}

</style>