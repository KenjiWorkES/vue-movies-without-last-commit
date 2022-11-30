<script>
import TodoItem from './TodoItem.vue';
import TodoControl from './TodoControl.vue';

export default {
  components: {
    TodoItem,
    TodoControl,
  },
  props: ['tasks'],
  data() {
    return {
      length: this.tasks.lenght,
    };
  },
};
</script>

<template>
  <section class="todo">
    <ul class="todo__list">
      <TodoItem
        v-for="task in tasks"
        :key="task.id"
        :id="task.id"
        :text="task.task"
        :is-completed="task.isCompleted"
      />
      <footer class="todo__footer">
        <p class="todo__lenght">0 items left</p>
        <button class="todo__clear">Clear Completed</button>
      </footer>
    </ul>
  </section>
  <TodoControl />
</template>

<style scoped lang="scss">
.todo {
  background-color: var(--deep-dark-blue);
  border-radius: 0.5rem;
  overflow: hidden;
  max-width: 70rem;
  margin: -3rem auto 0;

  &__list {
    list-style: none;
  }

  &__footer {
    padding: 1.5rem 2rem 2rem;
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
