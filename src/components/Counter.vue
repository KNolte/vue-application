<template>
  <div class="counter">
    <h2>Counter</h2>
    <input type="number" v-model="count">
    <button @click="addToCount(1)">increment</button>
  </div>
</template>

<script lang="ts">
import {Component, Emit, Vue} from 'vue-property-decorator';

@Component
export default class Counter extends Vue {
  private count = 0;

  @Emit()
  private addToCount(n: number) {
    this.count += n;
  }
}
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
