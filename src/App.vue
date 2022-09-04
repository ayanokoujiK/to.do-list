<template>
  <div class="wrapper">
    <Header />
    <Description />
  </div>
</template>

<script>

import Header from "@/components/Header";
import Description from "@/components/content-components/Description";

export default {
  name: 'App',
  components: {
    Header,
    Description
  }
}
</script>

<style>
  *{
    font-family: monospace;
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }


  .wrapper{
    background-color: #5DC8CD;
    width: 700px;
    height: 100vh;
    margin: 0 auto;
  }
</style>
