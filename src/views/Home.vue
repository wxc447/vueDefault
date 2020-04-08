<template>
  <div class="home">
 
  </div>
</template>

<script>
// @ is an alias to /src

// import http from '@/utils/request'

export default {
  name: 'Home',
  created(){
    this.$http({
      method:"post",
      url:"/backLogin",
      data:{
     
      }
    }).then(res=>{
      console.log(res)
    }).catch(err=>{
      console.log(err)
    })
  }
}
</script>
