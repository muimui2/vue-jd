<template>
   <div class="inviteBar">
       <div v-for="item in items" :key="item">
        <div class="itemBox">
            <img :src=item alt="">
        </div>
       </div>
       
   </div>
</template>

<script type="text/ecmascript">

import img01 from '../assets/redbag01.jpg'
import img02 from '../assets/redbag02.jpg'

export default {
   name: '',
   data() {
       return {
           items:[
               img01,
               img02
           ]
       }
   },
  components: {}
}
</script>

<style>
.inviteBar{
    padding: 0 10px;
    display: grid;
    grid-template-columns: 1fr 1fr; 
    grid-gap: 2px;
}

.inviteBar div{
    border-radius: 6px;
    overflow: hidden;
}
.itemBox img{
    width: 100%
}

</style>
