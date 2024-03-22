<script lang="ts"></script>

<style>
:root {
  --form-gap: 1rem;
}

form {
  background-color: white;
  box-shadow: 0.25px 0.25px 0 0px rgba(0, 0, 0, 0.75),
    0.5px 0.5px 0 0px rgba(0, 0, 0, 0.5);
}

input {
  border-left: solid;
  border-right: solid;
}

fieldset {
  display: grid;
}

.legend {
  background: lightblue;
  text-align: center;

  flex-grow: 1;
}

.input-wrapper {
  display: grid;
  padding: 0 var(--form-gap);
  background: lightyellow;

  border-left: solid;
  border-right: solid;
}

.block-bg_separator {
  background:
    radial-gradient(circle at center, #051c56 50%, transparent 1%),
    linear-gradient(90deg, #051c56 1px, transparent 1px);
}

.block-bg {
  background:
    radial-gradient(circle at center, #051c56 50%, transparent 1%);
}

.block {
  background-size: var(--form-gap) var(--form-gap);
  background-position: 0 center;
  background-repeat: space;

  min-height: var(--form-gap);
}

#confirm-btn {
  background: salmon;

  flex-grow: 1;
}

.row {
  display: flex;
  padding: 0 var(--form-gap);
  border: solid;
}
</style>

<template>
  <form>
    <fieldset>
      <div class="row block block-bg_separator"></div>

      <div class="row block block-bg">
        <section class="legend">
          <h4>sign up</h4>
        </section>
      </div>

      <div class="row block block-bg_separator"></div>

      <div class="row block block-bg">
        <section class="input-wrapper">
          <input id="username" placeholder="username" type="text" required />
        </section>
      </div>

      <div class="row block block-bg_separator"></div>

      <div class="row block block-bg">
        <section class="input-wrapper">
          <input id="email" placeholder="email" type="email" required />
        </section>
      </div>

      <div class="row block block-bg_separator"></div>

      <div class="row block block-bg">
        <section class="input-wrapper">
          <input id="password" placeholder="password" type="password" required />
        </section>
      </div>

      <div class="row block block-bg_separator"></div>

      <div class="row block block-bg">
        <button id="confirm-btn">confirm</button>
      </div>

      <div class="row block block-bg_separator"></div>

    </fieldset>
  </form>
</template>
