<script>
import { PhCheck, PhPaperPlaneRight } from 'phosphor-vue';
import AddTodo from './AddTodo.vue';

export default {
  components: {
    AddTodo,
  },
  props: ['addTask'],
};
</script>

<template>
  <header class="header">
    <div class="header__container">
      <div class="header__control">
        <h1 class="header__title">TODO</h1>
      </div>
      <AddTodo :add-task="addTask" />
    </div>
  </header>
</template>
<style scoped lang="scss">
.header {
  width: 100%;
  background-image: url('/assets/bg-mobile-dark.jpg');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  padding: 5rem 2rem;

  @media only screen and (min-width: 1080px) {
    background-image: url('/assets/bg-desktop-dark.jpg');
    padding: 8rem 2rem 5rem;
  }

  &__container {
    max-width: 70rem;
    margin: 0 auto;
  }

  &__control {
    margin-bottom: 3rem;
  }

  &__title {
    color: var(--light-grayish-blue-hover);
    font-size: 2.5rem;
    letter-spacing: 0.8rem;

    @media only screen and (min-width: 1080px) {
      font-size: 3.5rem;
    }
  }
}
</style>
