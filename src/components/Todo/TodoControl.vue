<script>
export default {};
</script>

<template>
  <section class="filter">
    <button class="filter__button">All</button>
    <button class="filter__button">Active</button>
    <button class="filter__button">Completed</button>
  </section>
</template>

<style scoped lang="scss">
.filter {
  margin: 2rem auto;
  width: 100%;
  background-color: var(--deep-dark-blue);
  border-radius: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  padding: 1.5rem;
  max-width: 70rem;

  &__button {
    font-family: inherit;
    background-color: transparent;
    border: none;
    font-size: 1.6rem;
    font-weight: 700;
    color: var(--very-dark-graylish-blue);
  }
}
</style>
