<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <router-view />
  </div>
</template>
<script>
export default {
  name: 'App'
}

</script>
<style>
.container {
  width: 20%;
  border: 1px solid black;
}

.btn {
  width: 25%;
}

.bigbtn {
  width: 50%;
}

.display {
  height: 2em;
}

</style>
