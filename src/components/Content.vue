<template>
  <div>
    <!-- Single -->
    <div class="container">
      <div class="row">
        <div class="col-sm-6">
          <Select2 :options="options" v-model="single_selected"/>
          <pre class="code">
            <p v-text="single_selected"></p>
        </pre>
        </div>
      </div>
    </div>

    <!-- Multiple -->
    <div class="container">
      <div class="row">
        <div class="col-sm-6">
          <Select2 :options="options" v-model="multiple_selected" :multiple="true"/>
          <pre class="code">
            <p v-text="multiple_selected"></p>
        </pre>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Select2 from "./select2.vue";

export default {
  name: "Content",
  components: {
    Select2
  },
  data() {
    return {
      single_selected: "1",
      multiple_selected: [1],
      options: {
        1: "VueJS",
        2: "JavaScript",
        3: "Python",
        4: "Ruby"
      }
    };
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
