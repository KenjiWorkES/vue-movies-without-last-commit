<script>
export default {
  props: ['id', 'text', 'isCompleted'],
  inject: ['updateTaskHandler'],
  data() {
    return {
      checkedState: this.isCompleted,
    };
  },
};
</script>

<template>
  <li class="todo__item">
    <div class="todo__checkboxControl">
      <input
        :id="id"
        type="checkbox"
        class="todo__checkbox"
        v-model="checkedState"
        @change="updateTaskHandler(id, checkedState)"
      />
      <label class="todo__checkboxLabel" :for="id">
        <ph-check class="todo__icon" :size="20" color="white" weight="fill" />
      </label>
    </div>
    <p :class="{ todo__text: true, 'todo__text--active': checkedState }">
      {{ text }}
    </p>
  </li>
</template>

<style scoped lang="scss">
.todo {
  &__item {
    padding: 1.5rem 2rem;
    border-bottom: 1px solid var(--very-dark-graylish-blue);
    display: flex;
    align-items: center;
  }

  &__checkboxControl {
    margin-right: 1rem;
  }

  &__checkbox {
    position: absolute;
    height: 0;
    width: 0;
  }

  &__checkboxLabel {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 2.2rem;
    height: 2.2rem;
    border: 1px solid var(--light-grayish-blue);

    border-radius: 9999px;
    cursor: pointer;

    @media only screen and (min-width: 1080px) {
      width: 2.4rem;
      height: 2.4rem;
    }
  }

  &__icon {
    display: none;
  }

  &__checkbox:checked ~ &__checkboxLabel {
    background-image: var(--gradient-checkbox);
    border: none;
  }

  &__checkbox:checked ~ &__checkboxLabel > &__icon {
    display: block;
  }

  &__text {
    color: var(--light-grayish-blue);
    font-size: 1.4rem;
    font-weight: 400;

    &--active {
      text-decoration: line-through;
      color: var(--dark-graylish-blue);
    }

    @media only screen and (min-width: 1080px) {
      font-size: 1.6rem;
    }
  }
}
</style>
