<script>
import TheHeader from './components/layout/TheHeader.vue';
import TodoList from './components/Todo/TodoList.vue';

export default {
  components: { TheHeader, TodoList },
};
</script>

<template>
  <div class="layout">
    <TheHeader />
    <main>
      <TodoList />
    </main>
  </div>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@400;600;700&display=swap');

:root {
  --bright-blue: hsl(220, 98%, 61%);
  --bright-purple: hsl(280, 87%, 65%);
  --bright-cyan: hsl(192, 100%, 67%);

  --gradient-checkbox: linear-gradient(hsl(192, 100%, 67%), hsl(280, 87%, 65%));

  --dark-blue: hsl(235, 21%, 11%);
  --deep-dark-blue: hsl(235, 24%, 19%);
  --light-grayish-blue: hsl(234, 39%, 85%);
  --light-grayish-blue-hover: hsl(236, 33%, 92%);
  --dark-graylish-blue: hsl(234, 11%, 52%);
  --very-dark-graylish-blue: hsl(233, 14%, 35%);
  --deep-dark-graylish-blue: hsl(237, 14%, 26%);
}

*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

html {
  font-size: 62.5%;
}

body {
  box-sizing: border-box;
  font-family: 'Josefin Sans', sans-serif;
}

.layout {
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
}

main {
  padding: 0 2rem;
  width: 100%;
  height: 100%;
  background-color: var(--dark-blue);
}
</style>
