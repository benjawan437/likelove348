<template>
  <div id="app">
    <carout />
    <hr />
    <div class="row mb-2 ml-auto mr-auto">
      <div class="col-md-2"></div>
      <div class="col-md-4">
        <div class="mr-1 mt-2 ml-1 mb-2">
          <div class="card">
            <img alt="img1" src="./assets/a3.jpg" />
          </div>
        </div>
      </div>
      <div class="card-body">
        <counter @t1="aggregate" />
        <br />
        <div class="fortext">{{total}}</div>
      </div>
    </div>

    <hr />
    <div class="row mb-3 ml-auto mr-auto">
      <div class="col-md-2"></div>
      <div class="col-md-4">
        <div class="mr-1 mt-2 ml-1 mb-2">
          <div class="card">
            <img alt="img1" src="./assets/a2.jpg" />
          </div>
        </div>
      </div>
      <div class="card-body">
        <counter @t2="sum" />
        <br />
        <div class="fortext">{{to2}}</div>
      </div>
    </div>

    <hr />
    <div class="row mb-3 ml-auto mr-auto">
      <div class="col-md-2"></div>
      <div class="col-md-4">
        <div class="mr-1 mt-2 ml-1 mb-2">
          <div class="card">
            <img alt="img1" src="./assets/a1.jpg" />
          </div>
        </div>
      </div>
      <div class="card-body">
        <counter @t3="summary" />
        <br />
        <div class="fortext">{{tal3}}</div>
      </div>
    </div>
  </div>
</template> 

<script>
import counter from "./components/counter";
import carout from "./components/carout";

export default {
  name: "App",
  components: {
    counter,
    carout,
  },

  data: function () {
    return {
      total: 0, //ผลรวมทั้งหมด ---> เอาไปแสดงผล{{}}
      to2: 0,
      tal3: 0,
    };
  },

  methods: {
    aggregate(counterValue) {
      this.total += counterValue;
    },
    sum(counterValue) {
      this.to2 += counterValue;
    },
    summary(counterValue) {
      this.tal3 += counterValue;
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
  color: #ffffff;
}
.fortext{
  font-size: 60px;
}
</style>
