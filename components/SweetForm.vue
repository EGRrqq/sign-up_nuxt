<script lang="ts"></script>

<style>
:root {
  --form-gap: 0.25rem;
}

form {
  background-color: white;
  box-shadow: 0.25px 0.25px 0 0px rgba(0, 0, 0, 0.75),
    0.5px 0.5px 0 0px rgba(0, 0, 0, 0.5);

  border: black solid;
  border-radius: 0.05rem;
  padding: var(--form-gap);
}

input {
  border: solid;
}

fieldset {
  display: grid;
  gap: var(--form-gap);
}

.legend {
  background: lightblue;
  border: solid;
  text-align: center;
}

.input-wrapper {
  display: grid;
  border: solid;
  padding: var(--form-gap);
  background: lightyellow;
}

.block {
  background:
    radial-gradient(circle at center, #000 25%, transparent 1%);
  background-size: 2rem 2rem;
  background-position: 0 center;
}

#confirm-btn {
  background: salmon;
  border: solid;
}
</style>

<template>
  <form class="block">
    <fieldset>
      <!-- <legend>sign up</legend> -->
      <section class="legend">
        <h4>sign up</h4>
      </section>

      <section class="input-wrapper">
        <!-- <label for="username">username</label> -->
        <input id="username" placeholder="username" type="text" required />
      </section>
      <section class="input-wrapper">
        <!-- <label for="email">email</label> -->
        <input id="email" placeholder="email" type="email" required />
      </section>
      <section class="input-wrapper">
        <!-- <label for="password">password</label> -->
        <input id="password" placeholder="password" type="password" required />
      </section>

      <button id="confirm-btn">confirm</button>
    </fieldset>
  </form>
</template>
