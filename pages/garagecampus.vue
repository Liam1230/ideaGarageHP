<template>
<v-container fill-height fill-width fluid grid-list-xl>
  <v-layout justify-center row wrap>
    <v-flex xs12 md12>
      <v-parallax class="toppic" dark src="/toppagebg2.jpg">
          <v-row align="center" justify="center">
            <v-expand-transition>
              <v-img v-show="titleshow" class="logoImage" src="/garageCampuslogo.png" contain></v-img>
            </v-expand-transition>
          </v-row>
          <v-row align="center" justify="center">
            <v-expand-transition>
              <p v-show="titleshow" class="display-1 font-weight-bold title_description grey--text text--darken-1">本物の「技術」を身につけて<br>あなたの「アイデア」を<br>「カタチ」にしよう</p>
            </v-expand-transition>
          </v-row>
      </v-parallax>
    </v-flex>
    <v-flex xs12 md12>
      <p id="carriculum_title" class="text-center display-1 font-weight-bold grey--text text--darken-1"> 3ヶ月でゼロからプログラミング基礎習得</p>
      <v-layout justify-center row wrap>
        <v-flex xs12 md6>
          <p class="text-center headline font-weight-bold grey--text text--darken-1">GarageCampusでは現役のエンジニアが対面形式で指導を行い、全くの未経験者、PCが苦手な方でも安心してプログラミングの基礎を身に付けることができます。</p>
          <p class="text-center headline font-weight-bold grey--text text--darken-1">最新のハイクラスなスキルを超低価格で習得</p>
        </v-flex>
      </v-layout>
    </v-flex>
    
    <!-- カリキュラム -->
    <v-flex xs12 md12>
      <v-divider class="my-5"></v-divider>
      <p id="carriculum_title" class="text-center display-3 font-weight-bold grey--text text--darken-1"> スクールの特徴</p>
      <v-layout justify-center row wrap>
        <v-flex xs6 md4>
          <v-img height="40vh" src="/skill.png"></v-img>
          <v-layout justify-center row wrap>
            <v-flex xs11 md11>
              <p class="text-left body-1 font-weight-bold grey--text text--darken-1">HTML/Javascriptなどの基本的なWeb制作からNuxt/Firebase/GoogleCloudPlatformなどを使った機械学習などの最新技術までが学べます。</p>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex xs6 md4>
          <v-img height="40vh" src="/school.jpg"></v-img>
          <v-layout justify-center row wrap>
            <v-flex xs11 md11>
              <p class="text-left body-1 font-weight-bold grey--text text--darken-1">対面式のスクール形式なので、聞きたいことがすぐ聞ける。同じようにプログラムを学ぶ仲間と繋がって共に成長ができます。</p>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-flex>
    <!-- Profile -->
    <v-flex xs12 md12>
      <v-divider class="my-5"></v-divider>
      <p id="profile_title" class="text-center display-3 font-weight-bold grey--text text--darken-1"> Profile</p>
      <v-layout justify-center row wrap>
        <v-flex xs12 md4>
          <p class="text-center display-1 font-weight-bold grey--text text--darken-1">現役のフリーランスエンジニアから学ぶ</p>
          <p class="text-center headline font-weight-bold grey--text text--darken-1">講師 木下大地 DaichiKinoshita</p>
          <p class="text-left body-1 grey--text text--darken-1">
            プログラマの父の影響で小学3年生からプログラミング教育を受ける
            ゲームの専門学校を卒業した後プログラマとしてゲーム開発会社に就職、多くのアプリの開発に携わる
            フリーランス転向後は物販支援ツールなどの業務システムや、クラウド技術に興味をもち仕事をこなす
            現在はフリーランスとして社内のシステム開発や、アプリ開発を行う。
          </p>
        </v-flex>
        <v-flex xs12 md6>
          <v-img src="/profileimage.jpg" height="60vh"></v-img>
        </v-flex>
      </v-layout>
    </v-flex>
    <!-- 料金システム -->
    <!-- <v-flex xs12 md12>
      <v-divider class="my-5"></v-divider>
      <p id="profile_title" class="text-center display-3 font-weight-bold grey--text text--darken-1"> 料金/システム</p>
    </v-flex> -->
    <!--アクセス-->
    <v-flex xs12 md12>
      <v-divider class="my-5"></v-divider>
      <p id="access_title" class="text-center display-3 font-weight-bold grey--text text--darken-1"> Access</p>
      <v-layout justify-center row wrap>
        <v-flex xs12 md6>
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1640.7943502530284!2d135.52252079044644!3d34.66508876776722!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6000e7535ac9f307%3A0x6c58e389c6d41081!2z44CSNTQzLTAwMjcg5aSn6Ziq5bqc5aSn6Ziq5biC5aSp546L5a-65Yy6562G44Kx5bSO55S677yV4oiS77yT77yYIOODreOCpOODpOODq-ODkeODvOOCr-OCueahg-Wdgg!5e0!3m2!1sja!2sjp!4v1569518576502!5m2!1sja!2sjp"
            width="100%" height="450" frameborder="0" style="border:0;" allowfullscreen=""></iframe>
        </v-flex>
        <v-flex xs12 md6>
          <p class="text-left body-1 font-weight-bold grey--text text--darken-1">〒543-0027</p>
          <p class="text-left body-1 font-weight-bold grey--text text--darken-1">大阪府大阪市天王寺区筆ヶ崎町5-38 ロイヤルパークス桃坂605</p>
          <p class="text-left body-1 font-weight-bold grey--text text--darken-1">最寄り駅:<br>大阪メトロ 鶴橋駅 谷町九丁目<br>近鉄線 大阪上本町</p>
        </v-flex>
      </v-layout>
    </v-flex>
  </v-layout>
</v-container>
</template>

<script>
import CoreToolbar from '~/components/Toolbar.vue'

export default {
    components:{
        CoreToolbar
    },
  mounted: function(){
    console.log(this.posts)
    setTimeout(()=>{
      this.titleshow = true;
    }, 800)
    setTimeout(()=>{
      this.titleDescAnim1 = true;
    }, 2000)
    setTimeout(()=>{
      this.titleDescAnim2 = true;
    }, 3200)
    setTimeout(()=>{
      this.titleDescAnim3 = true;
    }, 4400)
  },
	data: ()=>({
    titleshow: false,
    titleDescAnim1: false,
    titleDescAnim2: false,
    titleDescAnim3: false,
  }),
  methods: {
  }
}
</script>

<style>
.logoImage{
  height: 40vh;
}
.text_title{
    padding: 0.5em 0.7em;
    margin: 1em 0;
    color: rgb(105, 105, 105);/*文字色*/
    background: rgba(0,0,0,0);
    border: solid 5px #FFF;/*線*/
    border-radius: 10px;/*角の丸み*/
}
#toolbar{
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  z-index: 3;
}
</style>