<template>
  <div id="example-1">
    <button v-on:click="$like" class="button-a" id="01">
      LIKE
      <i class="far fa-thumbs-up fa-2x"></i>
    </button>
    <button v-on:click="$love" class="button-a" id="02">
      LOVE
      <i class="fas fa-heart fa-2x"></i>
    </button>
    <button v-on:click="$haha" class="button-a" id="03">
      HAHA
      <i class="fas fa-laugh-squint fa-2x"></i>
    </button>
    <button v-on:click="$wow" class="button-a" id="04">
      WOW
      <i class="fas fa-surprise fa-2x"></i>
    </button>
    <button v-on:click="$sad" class="button-a" id="05">
      SAD
      <i class="fas fa-sad-tear fa-2x"></i>
    </button>
    <button v-on:click="$angry" class="button-a" id="06">
      ANGRY
      
    </button>
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
      this.$emit("p1", this.like);
      this.$emit("p2", this.like);
      this.$emit("p3", this.like);
    },
    $love: function () {
      this.love = 10;
      this.$emit("p1", this.love);
      this.$emit("p2", this.love);
      this.$emit("p3", this.love);
    },
    $haha: function () {
      this.haha = 5;
      this.$emit("p1", this.haha);
      this.$emit("p2", this.haha);
      this.$emit("p3", this.haha);
    },
    $wow: function () {
      this.wow = 20;
      this.$emit("p1", this.wow);
      this.$emit("p2", this.wow);
      this.$emit("p3", this.wow);
    },
    $sad: function () {
      this.sad = -5;
      this.$emit("p1", this.sad);
      this.$emit("p2", this.sad);
      this.$emit("p3", this.sad);
    },
    $angry: function () {
      this.angry = -50;
      this.$emit("p1", this.angry);
      this.$emit("p2", this.angry);
      this.$emit("p3", this.angry);
    },
  },
};
</script>
<style scoped>
.b {
  font-size: 50px;
}
.button-a {
  background-color: white;
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
  background-color: white;
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
button:hover#blue {
  color: blue;
}
button:hover#red {
  color: red;
}
button:hover#yellow {
  color: #ffcc66;
}
button:hover#purple {
  color: #9370db;
}
button:hover#green {
  color: #13bd5f;
}
</style>

