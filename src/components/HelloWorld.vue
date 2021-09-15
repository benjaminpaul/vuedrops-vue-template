<template>
  <div class="p-4">
    <text-input placeholder="Hello world" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TextInput from "./TextInput.vue";

export default defineComponent({
  name: "HelloWorld",
  components: {
    TextInput,
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
