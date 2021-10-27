<template>
<div class="form-group">
  <textarea v-model="tweet" rows="5" col="10" class="form-control" placeholder="いま何してる？"></textarea>
  <button class="btn btn-info text-white mt-2" v-on:click="doAction">ツイートする</button>
  <p>これまでのツイート</p>
</div>
</template>

<script>
export default {
  name: 'Form',
  data() {
    return {
      tweet: '',
    }
  },
  methods: {
    doAction(){
      this.$emit('tweeted',this.tweet)
      // console.log(this.tweet)
    }
  },
}
</script>