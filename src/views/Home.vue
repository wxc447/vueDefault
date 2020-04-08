<template>
  <div class="home">
    <div>
      
   
    </div>
  </div>
</template>

<script>


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
