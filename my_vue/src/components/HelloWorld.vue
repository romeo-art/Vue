<template>
  <div class="hello">
    <test @change="getValue" :value="value"></test><br />
    <test2 @change="getValue" :value="value"></test2><br />
    <test3 @change="getValue" :value="value"></test3><br />

    <p>{{ value.name }}</p>
    <p>{{ value.age }}</p>
    <p>{{ value.gender }}</p>
    <p>{{ value.status }}</p>
    <p>{{ value.school }}</p>
    <p>{{ value.address.brgy }}</p>
    <p>{{ value.address.town }}</p>
    <p>{{ value.address.city }}</p>

  </div>
</template>

<script>
import test from "./test";
import test2 from "./test2";
import test3 from "./test3";

export default {
  name: "HelloWorld",
  data() {
    return {
      value: {
        name: "name",
        age: 'age',
        gender: "gender",
        status: "status",
        school: "school",
        address: {
          brgy: "brgy",
          town: "town",
          city: "city",
          
        },
        
      },
    };
  },
  props: {
    msg: String,
  },

  components: { test, test2, test3 },
  methods: {
    getValue: function(val) {
      this.value = { ...this.value, val };
    },
  },
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
