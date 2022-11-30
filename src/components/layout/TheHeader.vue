<script>
import { PhCheck, PhPaperPlaneRight } from 'phosphor-vue';
import AddTodo from './AddTodo.vue';

export default {
  components: {
    AddTodo,
  },
};
</script>

<template>
  <header class="header">
    <div class="header__control">
      <h1 class="header__title">TODO</h1>
    </div>
    <AddTodo />
  </header>
</template>
<style scoped lang="scss">
.header {
  width: 100%;
  background-image: url('/assets/bg-desktop-dark.jpg');
  padding: 5rem 2rem;

  &__control {
    margin-bottom: 3rem;
  }

  &__title {
    color: var(--light-grayish-blue-hover);
    font-size: 2.5rem;
    letter-spacing: 0.8rem;
  }
}
</style>
