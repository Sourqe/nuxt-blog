<template>
<div>
  <nav class="main-header sidebar" id="sidebar"
    v-bind:class="{ activeSidebar: showMobileMenu }">
    <div class="toggle-btn"
      v-bind:class="{ active: showMobileMenu }"
      v-on:click="showMobileMenu = !showMobileMenu">
      <span></span>
      <span></span>
      <span></span>
    </div>
    <div class="list">
      <div class="item" ><nuxt-link to="/blog">Posts</nuxt-link></div>
      <div class="item" ><nuxt-link to="/about">About</nuxt-link></div>
    </div>
  </nav>
  <div class="content">
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Veritatis eaque esse aliquam! Quam tempora quas asperiores reprehenderit natus, dignissimos provident vel voluptates sequi aspernatur est, iste quasi odio eum voluptatibus.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Veritatis eaque esse aliquam! Quam tempora quas asperiores reprehenderit natus, dignissimos provident vel voluptates sequi aspernatur est, iste quasi odio eum voluptatibus.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Veritatis eaque esse aliquam! Quam tempora quas asperiores reprehenderit natus, dignissimos provident vel voluptates sequi aspernatur est, iste quasi odio eum voluptatibus.</p>
  </div>
</div>  
</template>

<script>
export default {
  data() {
    return {
      showMobileMenu: false
    }
  }, 
  methods: {
    toggleSidebar() {
      document.getElementById("sidebar").classList.toggle('active');
      console.log("working")
    }
  }
};
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
  position:absolute;
  top:0px;
  left:-200px;
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
a:active {
  color: lightgrey;
}
#sidebar .toggle-btn {
  position:absolute;
  left:220px;
  top:10px;
}
#sidebar .toggle-btn span {
  display:block;
  width:30px;
  height:5px;
  background:#151719;
  margin:5px 0px;
  cursor:pointer;
}
.activeSidebar {
  left:0px;
}
#sidebar div.list div.item {
  padding:15px 10px;
  border-bottom:1px solid #444;
  color:#fcfcfc;
  text-transform:uppercase;
  font-size:15px;
  text-decoration: none;
}

.content {
  padding:10px;
  margin-top:60px;
}
</style>
