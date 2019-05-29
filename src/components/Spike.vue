<template>
   <div class="spikeBar">
       <!-- title -->

        <el-card shadow="always">
            <div class='spiketitle'>
                <div class='title-left'>
                    <i class="iconfont icon-miaosha"></i>
                    <span>秒杀</span>
                    <span>2019-5-23</span>
                </div>
                <div class='title-right'>查看更多<i class="iconfont icon-youfanye"></i></div>
            </div>
        <!-- body -->
            <ul class="spikeBody">
                <li v-for="item in items" :key="item">
                    <a href="" class="spimg">
                        <img :src=item.img alt="">
                    </a>
                    <div class="newPrice">
                        <span>￥</span>
                        <span class="pricemun">{{item.newPrice}}</span>
                    </div>
                    <div class="oldPrice">
                         <span>￥</span>
                        <span>{{item.oldPrice}}</span>
                    </div>
                </li>
            </ul>
        </el-card>


   </div>
</template>

<script type="text/ecmascript">

import img01 from '../assets/spike.jpg'

export default {
   name: '',
   data() {
       return {
           items:[
               {img:img01, newPrice:'139', oldPrice:'299'},
               {img:img01, newPrice:'139', oldPrice:'299'},
               {img:img01, newPrice:'139', oldPrice:'299'},
               {img:img01, newPrice:'139', oldPrice:'299'},
               {img:img01, newPrice:'139', oldPrice:'299'},
               {img:img01, newPrice:'139', oldPrice:'299'},
               {img:img01, newPrice:'139', oldPrice:'299'}
           ]
       }
   },
  components: {},

  methods:{




  }
}
</script>



<style>

.spikeBar{
    padding: 0 10px;
    margin-top: 10px;
}

.el-card__body{
    padding: 10px;
}

.spiketitle{
    display: flex;
    display: -webkit-flex;
    justify-content: space-between;
    align-items: center;
}
.spiketitle .title-left i{
    font-size: 30px;
    color: blueviolet;
}

.spiketitle .title-right{
    color: #e93b3d;
}

.spiketitle .title-right i{
    margin-left: 3px;
}

.spikeBody{
    display: flex;
    display: -webkit-flex;
    padding: 0;
    overflow-y: scroll;
}
/* 隐藏滚动条同时又可以滚动 */
.spikeBody::-webkit-scrollbar {
    display:none
    }

.spikeBody li{
    list-style-type: none;
    padding: 5px;
    display: flex;
    display: -webkit-flex;
    flex-direction: column;
    align-items: center;
    width: 80px;
}

.spimg{
    display: inline-block;
}
.spimg img{
    width: 70px;
    height: 70px;
}



.newPrice{
    color: #e93b3d;
    font-size: 12px;
}

.newPrice .pricemun{
    font-size: 18px;
    font-weight: 800;
     
}

.oldPrice{
    color: #696969;
    font-size: 12px;
    text-decoration: line-through;
}



</style>
