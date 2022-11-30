<script>
export default {
  props: ['addTask'],
  data() {
    return {
      enteredTask: '',
      isChecked: false,
    };
  },
  methods: {
    addTaskHandler() {
      this.addTask(this.enteredTask, this.isChecked);
    },
  },
};
</script>

<template>
  <form @submit.prevent="addTaskHandler" class="header__form">
    <div class="header__checkboxControl">
      <input
        id="checkboxAdd"
        type="checkbox"
        class="header__checkbox"
        v-model="isChecked"
      />
      <label class="header__checkboxLabel" for="checkboxAdd">
        <ph-check class="header__icon" :size="20" color="white" weight="fill" />
      </label>
    </div>
    <input
      v-model="enteredTask"
      type="text"
      class="header__input"
      aria-label="Add a new Todo"
      placeholder="Create a new todo"
    />
    <button class="header__button">
      <ph-paper-plane-right :size="20" color="white" weight="fill" />
    </button>
  </form>
</template>

<style scoped lang="scss">
.header {
  &__form {
    background-color: var(--deep-dark-blue);
    padding: 1.5rem 2rem;
    border-radius: 0.5rem;
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

  &__input {
    font-family: inherit;
    background-color: transparent;
    border: none;
    width: 100%;
    color: var(--light-grayish-blue-hover);

    @media only screen and (min-width: 1080px) {
      font-size: 1.6rem;
    }
  }

  &__button {
    background-color: transparent;
    border: none;
  }
}
</style>
