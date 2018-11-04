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
