<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div>
      <el-button @click="startHacking" v-bind:name="start1">Start1</el-button>
      <el-button @click="startHacking" v-bind:name="start3">Start2</el-button>
      <el-button @click="startHacking" v-bind:name="start3">Start3</el-button>
    </div>
  </div>
</template>
/*按钮上的元素怎么才能传递到弹出层？*/


<script>
export default {
  methods: {
    startHacking () {
      this.$notify({
        title: 'It works!'+this.name,
        type: 'success',
        message: 'We\'ve laid the ground work for you. It\'s time for you to build something epic!',
        duration: 5000
      })
    }
  }
}
</script>

<style>
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
}
</style>
