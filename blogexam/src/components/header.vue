<template>
  <nav>
      <ul>
          <li><router-link to="/" exact>Blog</router-link></li>
          <li><router-link to="/add" exact>Add a New Blog</router-link></li>
      </ul>
  </nav>
</template>

<script>
export default {
  
}
//원래는 a 태그의 href속성을 이용했던 반면, vue-router는
//router-link태그의 to속성을 이용한다.
//exact를 붙혀주면 정확한 url만 인식한다.
</script>

<style scoped>
ul{
    list-style-type: none;
    text-align: center;
    margin: 0;
}
li{
    display: inline-block;
    margin: 0 10px;
}
a{
    color: #fff;
    text-decoration: none;
    padding: 6px 8px;
    border-radius: 10px;
}
nav{
    background: #444;
    padding: 14px;
    margin-bottom: 40px;
}
.router-link-active{
    background: #eee;
    color:#444;
}

</style>



