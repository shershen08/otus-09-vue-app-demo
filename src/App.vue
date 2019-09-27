<template>
  <div id="app">
    <p>test</p>
    <!-- HERE: non dynamic props pass-->
    <HelloWorld msg="Hello" v-on:customEvent="onCustomEvent"/>
    <!-- HERE: dynamic  props pass -->
    <HelloWorld v-bind:msg="secondTitle" v-on:customEvent="onCustomEvent"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
//import MyFancyModal from 'npm-package'

export default {
  name: 'app',

  data() {
    return {
      secondTitle: 'Salut',
      links: ['https://codepen.io/shershen08/pen/exzMzr?editors=1011']
    }
  },

  methods: {
    // HERE: method that is called on 
    // v-on:customEvent from template
    onCustomEvent(data){
      console.log(data)
    }
  },

  components: {
    HelloWorld, // >> <hello-world/> || <HelloWorld/>
    
    //HERE: renaming components
    //MyFancyModal,
    //'app-modal-v2': MyFancyModal
  }
}
</script>
