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
      <TodoItem id="test1" />
      <TodoItem id="test2" />
      <TodoItem id="test3" />
      <TodoItem id="test4" />
      <TodoItem id="test5" />
      <TodoItem id="test6" />
      <footer class="todo__footer">
        <p class="todo__lenght">5 items left</p>
        <button class="todo__clear">Clear Combuttonleted</button>
      </footer>
    </ul>
  </section>
</template>

<style scoped lang="scss">
.todo {
  background-color: var(--deep-dark-blue);
  border-radius: 0.5rem;
  margin-top: -3rem;
  overflow: hidden;

  &__list {
    list-style: none;
  }

  &__footer {
    padding: 1.5rem 2rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__clear {
    border: none;
    background-color: transparent;
  }

  &__lenght,
  &__clear {
    font-size: 1.2rem;
    font-family: 'Josefin Sans', sans-serif;
    color: var(--dark-graylish-blue);
  }
}
</style>
