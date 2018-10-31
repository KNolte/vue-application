<template>
  <div class="components">
    <h1>Components</h1>
    <Counter />
  </div>
</template>

<script lang="ts">
    import { Component, Vue } from 'vue-property-decorator';
    import Counter from '@/components/Counter.vue'; // @ is an alias to /src

    @Component({
        components: {
            Counter,
        },
    })
    export default class Components extends Vue {}
</script>

