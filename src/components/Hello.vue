<template>
  <div class="hello" v-on:mouseover="focusIn" v-on:mouseleave="focusOut">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
//import { TweenMax } from 'gsap'
import motion from 'lumi/libs/motion';

export default {
  data () {
    return {
      // note: changing this line won't causes changes
      // with hot-reload because the reloaded component
      // preserves its current state and we are modifying
      // its initial state.
      msg: 'Hello World!'
    }
  },
  methods: {
    focusIn() {
  //    TweenMax.to(this.$el, 0.3, { x: 50 });
      motion.engine.to(this.$el, 0.3, { x: 50 });
    },
    focusOut() {
  //    TweenMax.to(this.$el, 0.3, { x: 0 });
      motion.engine.to(this.$el, 0.3, { x: 0 });
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: #42b983;
}
</style>
