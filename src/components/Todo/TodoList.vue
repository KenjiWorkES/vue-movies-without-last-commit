<script>
import TodoItem from './TodoItem.vue';

export default {
  components: {
    TodoItem,
  },
};
</script>

<template>
  <section class="todo">
    <ul class="todo__list">
      <TodoItem />
      <TodoItem />
      <TodoItem />
      <TodoItem />
      <TodoItem />
      <TodoItem />
    </ul>
  </section>
</template>

<style scoped lang="scss">
.todo {
  background-color: var(--deep-dark-blue);
  border-radius: 0.5rem;
  margin-top: -3rem;

  &__list {
    list-style: none;
  }
}
</style>
