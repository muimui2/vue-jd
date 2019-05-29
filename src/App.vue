<template>
  <div id="app">
      <Header />
      <Carousel />
      <Menu />
      <Invite />
      <Spike />
      <Floor />
      <Itemlist />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Carousel from './components/Carousel.vue'
import Menu from './components/Menu.vue'
import Invite from './components/Invite.vue'
import Spike from './components/Spike.vue'
import Floor from './components/Floor.vue'
import Itemlist from './components/Itemlist.vue'

export default {
  name: 'App',
  components: {
    Header,
    Carousel,
    Menu,
    Invite,
    Spike,
    Floor,
    Itemlist
  },
  mounted(){
    this.getTop();
  },
  methods:{
    getTop:function(){
        $(window).scroll(function(){
          if($(window).scrollTop() > 50){
              $("#searchBar").addClass("headerbg")
          }
          if($(window).scrollTop() == 0){
            $("#searchBar").removeClass("headerbg")
          }
        })
        
    }
  }
}
</script>

<style>
.headerbg{
  background-color: rebeccapurple;
}

</style>
