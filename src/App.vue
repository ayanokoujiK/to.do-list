<template>
  <div class="wrapper">
    <Header />
    <Description />
    <Functional />
  </div>
</template>

<script>

import Header from "@/components/Header";
import Description from "@/components/content-components/Description";
import Functional from "@/components/content-components/Functional";

export default {
  name: 'App',
  components: {
    Header,
    Description,
    Functional
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
    height: 950px;
    margin: 0 auto;
  }
</style>
