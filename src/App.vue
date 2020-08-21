<template>
  <body>
    <nav class="navbar navbar-expand-md navbar-dark bg-dark fixed-top ">
  <a class="navbar-brand " href="#">Herose</a>
</nav>

  <div class="starter-template">
    <div id="app">
    <div class="row">
      <div class="card col-md-3 container">
        <div id="app2">
          <img alt="img2" src="./img/64036fa1.jpg" width="250px" />
          <HelloWorld msg="Captain America" />
          <div class="row">
            <div>
              <cs-button @cc="sum" />
            </div>
          </div>
          <h1>{{ total1 }}</h1>
        </div>
      </div>

      <div class="card col-md-3 container">
        <div id="app2">
          <img alt="img2" src="./img/IMG_1719.jpg" width="250px" />
          <HelloWorld msg="I Ron Man" />
          <div class="row ">
            <div>
              <cs-button @cc="sum1" />
            </div>           
          </div>
          <h1>{{ total2 }}</h1>
        </div>
      </div>

      <div class="card col-md-3 container">
        <div id="app3">
          <img alt="img3" src="./img/0j2rfg.jpg" width="250px" height="375px" />
          <HelloWorld msg="Thor" />
          <div class="row">
            <div>
              <cs-button @cc="sum2" />
            </div>
          </div>
          <h1>{{ total3 }}</h1>
        </div>      
      </div>
    </div>
  </div>
  </div>


</body>

</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import CsButton from "./components/CsButton.vue";


export default {
  name: "App",
  components: {
    HelloWorld,
    CsButton,
  },

  data: function() {
    return {
      total1: 0,
      total2: 0,
      total3: 0,
    };
  },

  methods: {
    sum(counterValue) {
      this.total1 = counterValue;
    },
    sum1(counterValue) {
      this.total2 = counterValue;
    },
    sum2(counterValue) {
      this.total3 = counterValue;
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
  color: #110e07;
  margin-top: 50px;
}
#app2 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #110e07;
  margin-top: 60px;
}
#app3 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #110e07;
  margin-top: 60px;
}
.starter-template {
  background-color: rgb(58, 2, 2);
}
.card{
  margin-top: 30px;
  margin-bottom: 30px;
}
</style>
