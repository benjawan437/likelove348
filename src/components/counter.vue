<template>
  <div id="example-1">
    <button v-on:click="$like" class="button-a" id="a">LIKE</button>
    <button v-on:click="$love" class="button-a" id="b">LOVE</button>
    <button v-on:click="$haha" class="button-a" id="c">HAHA</button>
    <button v-on:click="$wow" class="button-a" id="d">WOW</button>
    <button v-on:click="$sad" class="button-a" id="e">SAD</button>
    <button v-on:click="$angry" class="button-a" id="f">ANGRY</button>
  </div>
</template>
<script>
export default {
  data: function () {
    return {
      like: 0,
      love: 0,
      haha: 0,
      wow: 0,
      sad: 0,
      angry: 0,
      count: 0,
    };
  },
  methods: {
    $like: function () {
      this.like = 1;
      this.$emit("t1", this.like);
      this.$emit("t2", this.like);
      this.$emit("t3", this.like);
    },
    $love: function () {
      this.love = 10;
      this.$emit("t1", this.love);
      this.$emit("t2", this.love);
      this.$emit("t3", this.love);
    },
    $haha: function () {
      this.haha = 5;
      this.$emit("t1", this.haha);
      this.$emit("t2", this.haha);
      this.$emit("t3", this.haha);
    },
    $wow: function () {
      this.wow = 20;
      this.$emit("t1", this.wow);
      this.$emit("t2", this.wow);
      this.$emit("t3", this.wow);
    },
    $sad: function () {
      this.sad = -5;
      this.$emit("t1", this.sad);
      this.$emit("t2", this.sad);
      this.$emit("t3", this.sad);
    },
    $angry: function () {
      this.angry = -50;
      this.$emit("t1", this.angry);
      this.$emit("t2", this.angry);
      this.$emit("t3", this.angry);
    },
  },
};
</script>
<style scoped>
.b {
  font-size: 50px;
}
.button-a {
  background-color: rgb(255, 255, 255);
  border: none;
  padding: 5px 5px 5px 5px;
  text-align: center;
  display: inline-block;
  margin: 4px 2px;
  cursor: pointer;
  border-radius: 10px;
  border: 0.5px solid white;
  width: 70px;
}
.button-a-font-dd {
  background-color: rgb(241, 236, 236);
  border: none;
  color: #646363;
  padding: 5px 5px 5px 5px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  margin: 4px 2px;
  cursor: pointer;
  border-radius: 10px;
  border: 0.5px solid #ffffff;
  width: 50px;
}
button:hover#a {
  color: rgb(60, 60, 228);
}
button:hover#b {
  color: rgb(245, 88, 237);
}
button:hover#c {
  color: #47e942;
}
button:hover#d {
  color: #e7e544;
}
button:hover#e {
  color: #7113bd;
}
button:hover#f {
  color: #ee2c25;
}
</style>

