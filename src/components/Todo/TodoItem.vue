<script>
export default {};
</script>

<template>
  <li class="todo__item">
    <div class="todo__checkboxControl">
      <input id="checkboxAdd" type="checkbox" class="todo__checkbox" />
      <label class="todo__checkboxLabel" for="checkboxAdd">
        <ph-check class="todo__icon" :size="20" color="white" weight="fill" />
      </label>
    </div>
    <p class="todo__text">This is a test</p>
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
  }
}
</style>
