<template>
    <div>
        <div class="greeting">Hello {{name}}{{exclamationMarks}}</div>
        <button @click="decrement">-</button>
        <button @click="increment">+</button>
    </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator';

@Component
export default class HelloDecorator extends Vue {
  // props
  @Prop() name!: string;
  @Prop() initialEnthusiasm!: number;

  // data
  enthusiasm = this.initialEnthusiasm;

  // methods
  increment() {
    this.enthusiasm++;
  }
  decrement() {
    if (this.enthusiasm > 1) {
      this.enthusiasm--;
    }
  }

  // computed
  get exclamationMarks(): string {
    return Array(this.enthusiasm + 1).join('!');
  }
}
</script>

<style>
.greeting {
  font-size: 20px;
}
</style>
