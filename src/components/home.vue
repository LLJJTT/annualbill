<template>
  <div class="home">
    <div class="fullpage-container">
      <div class="fullpage-wp" v-fullpage="opts">
        <div class="page-1 page">
          <p class="part-1" v-animate="{value: 'fadeIn'}">
            <img src="static/img/page1.png" alt="">
          </p>
        </div>
        <div class="page-2 page">
          <p class="part-2" v-animate="{value: 'fadeIn'}">
            <img src="static/img/page2.png" alt="">
          </p>
        </div>
        <div class="page-3 page">
          <p class="part-3" v-animate="{value: 'fadeIn'}">
            <img src="static/img/page3.jpg" alt="">
          </p>
        </div>
      </div>
    </div>
    </div>
</template>

<script>
  export default {
    data() {
      return {
        opts: {
          start: 0,
          dir: 'v',//垂直滚动
          duration: 200,
          beforeChange: function (prev, next) {
            console.log(prev+"-"+next)
          },
          afterChange: function (prev, next) {
            console.log(prev+"-"+next)
          }
        }
      }
    },
    methods:{

    }
  }
</script>

<style scoped>
  .page-container {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
  }
  .home{
    height: 100%;

  }
  .page p{
    height: 100%;
  }
  img{
    width: 100%;
    height: 100%;
    display: inline-block;
  }
</style>
