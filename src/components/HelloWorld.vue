<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button @click="onClick">close</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  
  methods: {
    onClick(){
      // HERE: passing data to event
      this.$emit('customEvent', {myMessage: this.msg})
      //console.info(this.msg)
    }
  },

  props: {
    //HERE: simple props geclaration
    msg: String,

    // HERE: detailed prop declarations
    // complexProp: {
    //   default: '',
    //   type: Number,
    //   validator: function(){
    //     //
    //   }
    // }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
