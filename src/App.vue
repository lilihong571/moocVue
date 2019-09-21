<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
    list-style: none;
  }
  /* 给所有的a标签去掉下划线  */
  a{
    text-decoration: none;
  }

</style>
