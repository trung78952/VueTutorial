<template>
  <div>
    <div class="topnav">
      <a class="active" href="#home">{{ text }}</a>
      <a href="#news">News</a>
      <a href="#contact">Contact</a>
      <a href="#about">About</a>
    </div>

    <div style="padding-left:16px">
      <h2>{{ msg }}</h2>
      <button @click="handlereset">reset</button>
      
    </div>

  </div>
</template>

<script>
export default {
  data() {
    return {
      text: 'Home'
    }
  },
  props:{
    msg:String,
    handlereset:Function

  }
}
</script>

<style>
body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}

.topnav {
  overflow: hidden;
  background-color: #333;
}

.topnav a {
  float: left;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

.topnav a:hover {
  background-color: #ddd;
  color: black;
}

.topnav a.active {
  background-color: #04AA6D;
  color: white;
}
</style>