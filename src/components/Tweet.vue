<template>
  <div class="alert alert-primary">
    <div v-on="tweeted" class="tweet">
        <p>{{tweeted}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Tweet",
  props:['tweeted'],
  data() {
    return {
      // tweeted: "a",
    };
  },
};
</script>

<style>
.tweet {
  border: 1px solid gray;
  height: 50px;
  margin: 0;
  padding: 10px;
}
</style>