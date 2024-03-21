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
  padding: var(--form-gap) 0;
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
  background: radial-gradient(circle at center, #000 50%, transparent 1%), white;
  background-size: 1rem 1rem;
  background-position: center;
  background-repeat: repeat-x;
}

#confirm-btn {
  background: salmon;
  border: solid;
}

.row {
  display: grid;
  padding: 0 var(--form-gap);
}
</style>

<template>
  <form>
    <fieldset>
      <!-- <legend>sign up</legend> -->
      <div class="row block">
        <section class="legend">
          <h4>sign up</h4>
        </section>
      </div>

      <div class="row block">
        <section class="input-wrapper">
          <!-- <label for="username">username</label> -->
          <input id="username" placeholder="username" type="text" required />
        </section>
      </div>
      <div class="row block">
        <section class="input-wrapper">
          <!-- <label for="email">email</label> -->
          <input id="email" placeholder="email" type="email" required />
        </section>
      </div>
      <div class="row block">
        <section class="input-wrapper">
          <!-- <label for="password">password</label> -->
          <input id="password" placeholder="password" type="password" required />
        </section>
      </div>

      <div class="row block">
        <button id="confirm-btn">confirm</button>
      </div>
    </fieldset>
  </form>
</template>
