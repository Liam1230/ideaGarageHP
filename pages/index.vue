<template>
<v-container fill-height fill-width fluid grid-list-xl>
  <v-layout justify-center row wrap>
    <v-flex xs12 md12>
      <v-parallax class="toppic" dark src="/toppagebg2.jpg">
          <v-row align="center" justify="center">
            <v-expand-transition>
              <!-- <p v-show="titleshow" class="text_title display-3 font-weight-bold">ideaGarage</p> -->
              <v-img v-show="titleshow" class="logoImage" src="/ideaGaragelogo.png" contain></v-img>
            </v-expand-transition>
          </v-row>
          <v-row align="center" justify="center">
            <v-expand-transition>
              <p v-show="titleshow" class="display-1 font-weight-bold title_description grey--text text--darken-1">あなたのアイデアを<br>カタチにする</p>
            </v-expand-transition>
          </v-row>
      </v-parallax>
    </v-flex>
    <CoreToolbar />
    <!--業種-->
    <v-flex xs12 md12>
      <v-divider class="my-5"></v-divider>
      <v-layout justify-center row wrap>
        <v-flex xs12 md12>
          <p id="business_title" class="text-center display-3 font-weight-bold grey--text text--darken-1"> Business</p>
        </v-flex>
        <v-flex xs6 md3>
          <p class="text-center headline font-weight-bold grey--text text--darken-1">ホームページ制作</p>
          <v-img  src="/hp.jpg" contain></v-img>
          <v-layout justify-center row wrap>
            <v-flex xs11 md11>
              <p class="text-left body-1 font-weight-bold grey--text text--darken-1">HTML,Javascriptを使ったHP制作に加え、Nuxt,Firebaseなどを活用したハイクオリティのHPの作成が可能です</p>
            </v-flex>
          </v-layout>
          <v-layout justify-center row wrap>
            <v-btn color="light-blue white--text font-weight-bold">もっと見る</v-btn>
          </v-layout>
        </v-flex>
        <v-flex xs6 md3>
          <p class="text-center headline font-weight-bold grey--text text--darken-1">Webアプリケーション開発</p>
          <v-img  src="/web.jpg" contain></v-img>
          <p class="text-left body-1 font-weight-bold grey--text text--darken-1">お客様の要望にあわせて事業を加速させるAndroid,iOS,PCに対応したシステムを手の届く価格で制作しています。</p>
          <v-layout justify-center row wrap>
            <v-btn color="light-blue white--text font-weight-bold">もっと見る</v-btn>
          </v-layout>
        </v-flex>
        <v-flex xs6 md3>
          <p class="text-center headline font-weight-bold grey--text text--darken-1">プログラミング教育</p>
          <nuxt-link to="/garagecampus"><v-img src="/study.jpg" contain></v-img></nuxt-link>
          <p class="text-left body-1 font-weight-bold grey--text text--darken-1">大阪を拠点に未経験者からフリーランス独立までの支援事業をおこなっています。</p>
          <v-layout justify-center row wrap>
            <v-btn color="light-blue white--text font-weight-bold" to="/garagecampus">もっと見る</v-btn>
          </v-layout>
        </v-flex>
        <v-flex xs6 md3>
          <p class="text-center headline font-weight-bold grey--text text--darken-1">モバイルアプリ開発</p>
          <v-img  src="/appdev.jpg" contain></v-img>
          <p class="text-left body-1 font-weight-bold grey--text text--darken-1">Flutterを使用したAndroid,iOS両対応ネイティブアプリの開発をおこなっています。</p>
          <v-layout justify-center row wrap>
            <v-btn color="light-blue white--text font-weight-bold">もっと見る</v-btn>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-flex>
    <!--開発実績-->
    <v-flex xs12 md12>
      <v-divider class="my-5"></v-divider>
      <p id="works_title" class="text-center display-3 font-weight-bold grey--text text--darken-1"> Works</p>
      <PostPreview :posts="posts"></PostPreview>
      <p class="text-center display-1 font-weight-bold grey--text text--darken-1"> もっと見る</p>
    </v-flex>
    <!--プロフィール-->
    <v-flex xs12 md12>
      <v-divider class="my-5"></v-divider>
      <p id="profile_title" class="text-center display-3 font-weight-bold grey--text text--darken-1"> Profile</p>
      <v-layout justify-center row wrap>
        <v-flex xs12 md4>
          <p class="text-center headline font-weight-bold grey--text text--darken-1">代表 木下大地 DaichiKinoshita</p>
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
    <!--アクセス-->
    <!-- <v-flex xs12 md12>
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
    </v-flex> -->
  </v-layout>
</v-container>
</template>

<script>
import CoreToolbar from '~/components/Toolbar.vue'
import PostPreview from '~/components/PostPreview.vue'

export default {
	components:{
    CoreToolbar,
    PostPreview
	},
	asyncData(env){
		return env.app.$contentful.getEntries({
			'content_type': 'myWorks',
			'limit': 3
		}).then(entries => {
			return {
				posts: entries.items
			}
		}).catch(console.error)
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
    posts:[],
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