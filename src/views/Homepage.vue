<template>
  <div class="container">
    <div class="main">
        <!-- 整个注册盒子 -->
      
      <div class="loginbox">
        <div>你好{{this.name}}</div>
       <button class="register_btn" @click="exit_login">退出登陆</button>
       <div class="title">Welcome to WH System Management Center</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Homepage",
  
  data:function (){
    return{
     message:'已登陆',
     name:'',
    }
  },

  //  created:function (){
  //   var routerParams = this.$route.query.name;
  //   this.name = routerParams;
  //  },

  methods:{
      exit_login(){
          alert("您已退出登录")
          
          this.$router.push({
            path: '/',
          }
        )
      },
       
  
  }
}
</script>

<style scoped>
.register_btn{
    background-color: #5f8276; /* Green */
    border: none;
    color: #FAFAFA;
    padding: 7px 35px;
    text-align: center;
    text-decoration: none;
    font-size: 13px;
    border-radius: 20px;
    outline:none;
    margin-top:10px;
}
.register_btn:hover{
    box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
    cursor: pointer;
     background-color: #0b5137;
    transition: all 0.2s ease-in;
}

.loginbox{
    position:absolute;
    width:770px;
    height:500px;
    top:40%;
    left:50%;
    transform:translate(-50%,-50%);
    box-shadow: 0 12px 16px 0  rgba(0,0,0,0.24), 0 17px 50px 0 #4E655D;
    background-image:url('./img/Christmas_Trees.png');
    background-size:cover;
    font-family:sans-serif;
}



.title{
    margin-top:370px;
    font-weight:bold;
    font-size:20px;
    color:#4E655D;
     width:800px;
    
}
.title:hover{
     font-size:21px;
     transition: all 0.4s ease-in-out;
     cursor: pointer;
}



</style>