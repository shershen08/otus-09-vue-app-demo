<template>
<div>
  <a v-bind:href="url">{{origin(url)}}</a>
  </div>
</template>

<script>
export default {
  name: 'my-link',
  props: {
    url: String
  },
//   computed: {
//       origin(){
//           return new URL(this.url).origin
//       }
//   }
  methods: {
      origin(url){
          return new URL(this.url).origin
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a {
  color: #42b983;
}
</style>
