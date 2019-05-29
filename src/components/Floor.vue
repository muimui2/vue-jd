<template>
   <div class="floor">
       <div>
           <img class="f_img" :src=f_img alt="">
       </div>
       <div class="floor-container">
           <div class="item" v-for="item in items" :key="item">
                <div class="title">{{item.title}}</div>
                <span class="description">{{item.description}}</span>
                <div class="pic">
                    <img :src=item.pic alt="">
                </div>
           </div>
           
       </div>
   </div>
</template>

<script type="text/ecmascript">

import f_img01 from '../assets/smallhouse01.jpg'
import f_img02 from '../assets/smallhouse02.jpg'

export default {
   name: '',
   data() {
       return {
           f_img:f_img01,
           items:[
               {title:'免息星球', description:'白条免息', pic:'https://picsum.photos/100/100.jpg'},
               {title:'金牌秒杀', description:'低价抢', pic:'https://picsum.photos/100/100.jpg'},
               {title:'金牌秒杀', description:'低价抢', pic:'https://picsum.photos/100/100.jpg'},
               {title:'免息星球', description:'白条免息', pic:'https://picsum.photos/100/100.jpg'},
               {title:'金牌秒杀', description:'低价抢', pic:'https://picsum.photos/100/100.jpg'},
               {title:'金牌秒杀', description:'低价抢', pic:'https://picsum.photos/100/100.jpg'},
               {title:'免息星球', description:'白条免息', pic:'https://picsum.photos/100/100.jpg'},
               {title:'金牌秒杀', description:'低价抢', pic:'https://picsum.photos/100/100.jpg'}


           ]
       }
   },
  components: {}
}
</script>

<style>


.floor{
    background-color: #f0f0f0;
    padding: 10px;
}

.floor .f_img{
    width: 100%
}


.floor-container{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-template-rows: auto;
    grid-gap: 1px;
    border-radius: 8px;
    background-color: white;
    padding: 10px 5px;
}

.floor-container .item{
    padding: 6px;
}


.floor-container .title{
    font-size: 16px;
    font-weight: 800;
    background: linear-gradient(to right, #d703f3, #fa2c29);
    -webkit-background-clip: text;
    color: transparent;
}

.floor-container .description{
    line-height: 12px;
}



.floor-container .pic img{
    width: 100%;
}



</style>
