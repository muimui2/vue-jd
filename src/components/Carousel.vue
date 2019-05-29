<template>
    <div class="block">
        <el-carousel height="200px" arrow="never">
            <el-carousel-item v-for="item in items" :key="item">
                <img :src=item alt="">
            </el-carousel-item>
        </el-carousel>
  </div>
</template>

<script type="text/ecmascript">
export default {
   name: '',
   data() {
       return {
           items:[
               'https://picsum.photos/500/200.jpg',
               'https://picsum.photos/450/200.jpg',
               'https://picsum.photos/500/300.jpg'
           ]
       }
   },
  components: {}
}
</script>

<style>
  .el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 150px;
    margin: 0;
  }

  .el-carousel__item:nth-child(2n) {
     background-color: #99a9bf;
  }
  
  .el-carousel__item:nth-child(2n+1) {
     background-color: #d3dce6;
  }

  .el-carousel__arrow--right:focus,
  .el-carousel__arrow--left:focus,
  .el-carousel__arrow--left:active,
  .el-carousel__arrow--right:active{
    border: none;
    outline: none;
  }

</style>
