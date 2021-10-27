<template>
  <Form v-on:tweeted="appAction" />
  <p>{{tweeted}}</p>
  <Tweet msg/>
</template>

<script>
import Form from './components/Form.vue'
import Tweet from './components/Tweet.vue'

export default {
  name: 'App',
  components: {
    Form,
    Tweet
  },
  data() {
    return {
      tweeted: '',
    }
  },
  methods: {
    appAction(tweet){
      console.log(tweet);
      this.tweeted = tweet
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
