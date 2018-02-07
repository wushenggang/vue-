<template>
    <div id="WebDetail">
      <img class="bigImg" :src="news.img">
      <div class="right">
        <img class="icon" :src="news.icon" alt="">
        <p class="title">{{news.title}}</p>
        <p class="line"></p>
        <p class="desc">{{news.desc}}</p>
        <p class="line"></p>
        <div class="icon-box">
          <img src="../assets/icon1.png" alt="">
          <img src="../assets/icon2.png" alt="">
          <img src="../assets/icon3.png" alt="">
          <img src="../assets/icon4.png" alt="">
          <img src="../assets/icon5.png" alt="">
          <img src="../assets/icon6.png" alt="">
        </div>
      </div>
  </div>
</template>

<script>
    export default {
        name: "WebDetail",
        data(){
          return {
          news:[]
        }
      },
      methods:{
      loadNews(id){
        this.axios.get("../../static/data/web-detail.json").then((response)=>{
        id=id-1;
        this.news=response.data.webNews[id];
      })
    }
    },
    mounted(){
      this.$nextTick(function(){
        this.loadNews(this.$route.params.id);
        $('.web-btn').addClass('router-link-active');
    })
  },
  destroyed(){
      $('.web-btn').removeClass('router-link-active');
    }
  }
</script>

<style scoped>
  #WebDetail{
    width:calc(100vw - 180px);
    margin-left:160px;
  }
  .bigImg{

    width:calc(90% - 380px);
   margin-left:6%;
    margin-top:40px
  }
  .right{
    position:fixed;
    top:40px;
    right:5%;
    width:300px;
    border-radius:3px;
    background:#fff;
    box-shadow:0 0 20px rgba(0,0,0,0.1);
  }
  .right .icon{
    margin:50px 100px;
    width:100px;
    height:100px;
    background:#f2f2f2;
  }
  .right .title{
    margin:5px 30px;
    font-size:24px;
    opacity:0.8;
    letter-spacing:1px;
    font-family:"customFont"
}
.right .line{
  margin:10px 30px;
  height:1px;
  background:#000;
  opacity:0.1;
}
.right .desc{
  margin:30px 30px;
  text-align:justify;
  font-size:14px;
  opacity:0.7;
  letter-spacing:1px;
}
.icon-box{
  margin:30px 30px;
  letter-spacing:1px;
}
.icon-box img{
  padding-right:5px;
  width:30px;
  height:30px;
}

</style>
