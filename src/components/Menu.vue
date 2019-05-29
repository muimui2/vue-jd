<template>
   <div class="menuBar">
       <div class="menu-item" v-for="list in menu" :key="list">
           <div class="itemImg">
              <img :src=list.img alt="">
           </div>
           <span class="itemTitle">{{list.title}}</span>
       </div>
   </div>
</template>

<script type="text/ecmascript">

import img01 from '../assets/1.png'
import img02 from '../assets/2.png'
import img03 from '../assets/3.png'
import img04 from '../assets/4.png'
import img05 from '../assets/5.png'
import img06 from '../assets/6.png'
import img07 from '../assets/7.png'
import img08 from '../assets/8.png'
import img09 from '../assets/9.png'
import img10 from '../assets/10.png'

export default {
   name: '',
   data() {
       return {
        menu:[
            {img:img01, title:'京东超时'},
            {img:img02, title:'海囤全球'},
            {img:img03, title:'京东服饰'},
            {img:img04, title:'京东生鲜'},
            {img:img05, title:'京东到家'},
            {img:img06, title:'充值缴费'},
            {img:img07, title:'9.9元拼'},
            {img:img08, title:'领卷'},
            {img:img09, title:'赚钱'},
            {img:img10, title:'全部'}
        ]
       }
   },
  components: {}
}
</script>

<style>

.menuBar{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
    grid-template-rows: 70px;
    border-radius: 10px;
    margin: 15px 0;
}

.menu-item{
    display: flex;
    display: -webkit-flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
}



.itemImg img{
    width: 35px;
}

.itemTitle{
    font-size: 12px;
}







</style>
