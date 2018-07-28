<template>
  <nav class="main-header sidebar" id="side">
    <div class="list">
      <div class="item menu"><nuxt-link to="/"><h1>Menu</h1></nuxt-link></div>
      <div class="item" ><nuxt-link to="/blog">Blog</nuxt-link></div>
      <div class="item" ><nuxt-link to="/about">About</nuxt-link></div>
    </div>
  </nav> 
</template>

<script>

</script>

<style scoped>
* {
  margin:0px;
  padding:0px;
  box-sizing:border-box;
  font-family:sans-serif;
}
body {
  transition:all 300ms linear;  
}
.sidebar {
  position: absolute;;
  top:0px;
  left:0px;
  width:200px;
  height:100%;
  background:#151719;
  transition:all 300ms linear;
}
a {
  color:#fcfcfc;
  text-decoration: none;
}
a:hover {
  color: lightgrey;
}
h1 {
  text-align: center;
}
#side div.list div.item {
  padding:15px 10px;
  border-bottom:1.25px solid #444;
  color:#fcfcfc;
  text-transform:uppercase;
  font-size:15px;
  text-decoration: none;
}
</style>
