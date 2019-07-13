<template>
  <div class="hello">
    
   
  </div>
</template>

<script>
import axios from "axios";
import { APIURL } from './variables.js'

export default {
  props: {
    msg: String
  },
  methods: {
    // callRestApi function that makes API call
    callRestApi: function () {
      axios({
        method: "GET",
        url: APIURL,
        headers: { "content-type": "application/json" }
      }).then(
        result => {
          if(result.status == 200) {
          this.response = result.data;
          console.log(this.response);
          }
          else {
            alert(result.statusText);
          }
        },
        error => {
          alert("An error occured: " + error.toString());
        }
      );
    }
  },
  beforeMount() {
    // Call the callRestApi function on load of page
    this.callRestApi()
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
