<template>
  <div>
  
    <h3 class="head">{{$route.params.gz[$route.params.index].title}}</h3>
    <div class="pic"><img :src="$route.params.gz[$route.params.index].img"/></div>
    <div class="content">{{$route.params.gz[$route.params.index].text}}</div>
	<div class="back" @click="back">返回</div>
    
  </div>
</template>

<script>
  export default {
    data(){
      return{

      }
    },
    methods:{
      back(){
        this.$router.go(-1)
      }
    }
  }
</script>

<style>
.head{
  text-align: center;
  color: #666;
  height: 50px;
  line-height: 50px;
  font-size: 18px;
}
.content{
  color: #666;
  font-size: 15px;
  text-align: center;
}
.time{
  text-align: center;
  color: #666;
}
.back{
  width: 50px;
  height: 20px;
  line-height: 20px;
  text-align: center;
  background: #c01920;
  color: #fff;
  border-radius: 10px;
  margin: 0 auto;
  margin-top: 20px;
}
.pic img{
	width: 100px;
	height: 150px;
	margin: 0 auto;
	margin-bottom: 10px;
}
</style>
