<template>
   <div id="searchBar">
        <i class="iconfont icon-menu"></i>
        <div class="searchBox">
            <i class="iconfont icon-xiazai17 search-icon"></i>
            <el-input class="search-input" v-model="input" placeholder="请输入内容"></el-input>
        </div>
        <span class="login">登陆</span>
                 
   </div>
</template>

<script type="text/ecmascript">
export default {
   name: '',
   data() {
       return {
            input: ''
       }
   },
  components: {}
}
</script>

<style>

#searchBar{
    padding: 10px 10px;
    display: flex;
    display: -webkit-flex;
    justify-content: space-between;
    align-items: center;
    position: fixed;
    left: 0;
    right: 0;
    z-index: 999;
}

.searchBox{
    position: relative;
    width: 80%;
    display: flex;
    display: -webkit-flex;
    align-items: center;
    justify-content: left;
}

.search-icon{
    position: absolute;
    z-index: 1;
    left: 10px;
    
}

.search-input{
    width: 100%;
}


.search-input input{
    border-radius: 30px;
    padding-left: 40px;
    border: none;
    height: 30px;
}

.search-input input:focus{
    border: none;
    outline: none;
}

.login,
.icon-menu{
    color: white;
}


</style>
