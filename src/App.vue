<template>
  <div id="app">
    <Dimmer v-bind:show=0></Dimmer>
    <TopBar></TopBar>
    <Content :posts_data=my_data.posts></Content>


  </div>
</template>

<script>
import TopBar from './components/TopBar'
import Dimmer from './components/Dimmer'
import Content from './components/Content'
export default {
  name: 'App',
  components :{TopBar,Dimmer,Content},
  data:function(){
    return {
      my_data:{}
    }
  },
  methods:{
    init:function(){

    },
    getData:function(){
      let self=this;
      this.axios.get('/static/data.json').then(function(response){
        self.my_data=response.data;
      })
    }
  },
  mounted:function(){
    let self=this;
    self.getData();
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
<style lang="scss">
  $header_bg_color: #36465d;
  $header_text_color: #9aa2ae;
  $divider_color: #505e72;
  $body_color: #36465d;
  $font_light_color: #afb5be;
  $font_darker_color: #687486;
  $hover_color: #529ecc;
  body{
      background-color: $body_color;
  }


  #k_header{
      height: 55px;
      margin-top: 0;
      background-color: $header_bg_color;
      border-bottom: 1px solid $divider_color;
      .right.menu .item .icon{
          color:$header_text_color;
          margin-right: 0;
      }
      .header{
          color: white;
      }
      .item:last-child{
          color:white;
          background-color: $hover_color;
      }
  }
  #k_head_message{
      margin-bottom: 0
  }

  #k_content{
      padding: 0px 8px 0 8px;
      width: 990px;
      margin: auto;
      // padding: 0 5px;
      // padding-top: 92px;

      .post_wrapper{
          position: relative;
      }
      .post_avatar{
          position: absolute;
          left: -85px;
          width: 64px;
          height: 100%;
          top: 0;
          .post_avatar_wrapper{
              position: sticky;
              top: 0;
              width: 64px;
              height: 64px;
              a{
                  display: block;
                  width: 100%;
                  height: 100%;
                  background-size:cover;
                  border-radius: 5%;
              }
          }
      }
  }
  .k_left_column{
      float: left;
      width: 640px;
      background-color: $header_bg_color;
      ul li{
          display: block;
          list-style: none;
          background-color: white;
          width: 100%;
          border-radius: 5px;
      }
      .post_header{
          color: #8f8f8f;
          max-width: 475px;
          word-wrap: normal;
          white-space: nowrap;
          font-size: 13px;
          vertical-align: middle;
          text-rendering: optimizeLegibility;
          box-sizing: border-box;
          text-align: left;
          .post_title{
              display: inline-block;
              font-weight: bold;
              height: 42px;
              line-height: 42px;
              padding:0 10px 0 20px;

          }
      }
  }
  .post_content{
      .photo{
          
      }
  }
  .post_footer{
    padding:5px 10px;
    text-align: left;

    span{
      display: inline-block;
    }
    .right.floated{
      float: right;
    }
  }

  .k_right_column{
      float: right;
      width: 320px;
      background-color: $header_bg_color;
  }
</style>