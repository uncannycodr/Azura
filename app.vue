<template>
  <div class="hello">
    <NuxtPage />
  </div>
</template>

<style scoped>
.hello {
  /* Create the gradient in the top right corner */
  background: radial-gradient(
    circle at top right,
    #42a5f5,
    #90caf9 30%,
    #e3f2fd 70%,
    #ffffff 80%
  );

  /* Control the gradient's size and position */
  background-size: 1400px 1100px; /* Adjust dimensions to control spread */
  background-repeat: no-repeat;
  background-position: top right; /* Place it in the top right */

  /* Ensure gradient stays in top half without affecting content */
  height: 80vh; /* Set the height to viewport height */
}
</style>
