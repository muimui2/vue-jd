<template>
   <div class="itemlist">
        <div v-for="list in lists" :key="list">
            <div><img :src=list.pic alt=""></div>
            <div>
                <span>{{list.title}}</span>
                <div class="fooder">
                    <div fooder-left>
                        <div class="price">
                            <span>￥</span>
                            <span class="mun">{{list.price}}</span>
                        </div>
                        <el-button type="danger">{{list.group}}</el-button>
                    </div>
                    <el-button>看相似</el-button>
                </div>
            </div>
        </div>
   </div>
</template>

<script type="text/ecmascript">
export default {
   name: '',
   data() {
       return {
           list:[
               {pic:'https://picsum.photos/500/200.jpg', title:'你快乐过生活我拼命去生存',price:'130', group:'拼团'},
               {pic:'https://picsum.photos/500/200.jpg', title:'你快乐过生活我拼命去生存',price:'130', group:'拼团'},
               {pic:'https://picsum.photos/500/200.jpg', title:'你快乐过生活我拼命去生存',price:'130', group:'拼团'},
           ]
       }
   },
  components: {}
}
</script>

<style>

.itemlist{
    display: grid;
    grid-template-columns: 1fr 1fr;
    /* grid-template-rows: auto; */
    grid-gap: 4px;

}

</style>
