<template>
  <div>
      <div @click="change" data-id="1" class="ddu">ddu</div>
      <div @click="change" data-id="2" class="tmc">tmc</div>

      <div v-show="tab==1" class="des">
        {{des}}
      </div>

      <div v-show="tab==2" class="sth">
        {{sth}}
      </div>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      des: 'Welcome to Your Vue.js App',
      sth: 'talk sth',
      tab:1
    }
  },
  methods:{
    change:function(e){
      let tabid = e.target.dataset.id
      this.tab = tabid
    }
  }
}
</script>

<style>
  .des{
    width: 200px;
    height: 200px;
    background: red;
  }
  .sth{
    width: 200px;
    height: 200px;
    background: yellow;
  }
</style>


