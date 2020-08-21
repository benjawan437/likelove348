<template>
  <div id="app">
    <carousel-section></carousel-section>

    <hr />
    <div class="row mb-2 ml-auto mr-auto">
      <div class="col-md-2"></div>
      <div class="col-md-4">
        <div class="card">
          <div class="mr-1 mt-2 ml-1 mb-2">
            <img alt="img1" src="./assets/20.jpg" height="350px" width="350px" />
          </div>
        </div>
      </div>
      <div class="card-body">
        <counter @p1="sum" />
        <br />
        {{total}}
      </div>
    </div>

    <hr />
    <div class="row mb-3 ml-auto mr-auto">
      <div class="col-md-2"></div>
      <div class="col-md-4">
        <div class="card">
          <div class="mr-1 mt-2 ml-1 mb-2">
            <img alt="img1" src="./assets/15.jpg" height="350px" width="350px" />
          </div>
        </div>
      </div>
      <div class="card-body">
        <counter @p2="sum" />
        <br />
        {{total}}
      </div>
    </div>

    <hr />
    <div class="row mb-3 ml-auto mr-auto">
      <div class="col-md-2"></div>
      <div class="col-md-4">
        <div class="card">
          <div class="mr-1 mt-2 ml-1 mb-2">
            <img alt="img1" src="./assets/3.jpg" height="350px" width="350px" />
          </div>
        </div>
      </div>
      <div class="card-body">
        <counter @p3="sum" />
        <br />
        {{total}}
      </div>
    </div>
  </div>
</template> 

<script>
import counter from "./components/counter.vue";

export default {
  name: "App",
  components: {
    counter,
  },

  data: function () {
    return {
      total: 0, //ผลรวมทั้งหมด ---> เอาไปแสดงผล{{}}
    };
  },

  methods: {
    sum(counterValue) {
      this.total += counterValue;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 70px;
}
</style>
