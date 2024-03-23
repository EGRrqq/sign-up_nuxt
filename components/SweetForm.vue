<script lang="ts"></script>

<style>
:root {
  --blue-800: #051c56;
  --blue-400: #0047e1;
  --blue-200: #c9eaff;

  --green-400: #a7df34;

  --red-400: #ff6958;
  --pink-200: #ffe5e9;

  --yellow-100: #fffcf7;

  --form-gap: 1rem;
  --form-border: 0.05rem;

  --plate: black;
}

body {
  background: var(--yellow-100);
}

form {
  display: grid;
  background-color: var(--blue-800);
}

input {
  min-height: calc(var(--form-gap) * 2);
  padding: 0 0.25rem;
  outline: calc(var(--form-border) * 2) solid;
}

fieldset {
  display: grid;
}

.input-wrapper {
  display: grid;

  border: var(--form-border) solid;
  border-top: 0;
  border-bottom: 0;

  padding: var(--form-gap);
  background: var(--green-400);
}

.block-bg_separator {
  background:
    linear-gradient(90deg, var(--blue-800) var(--form-border), transparent 1%),
    linear-gradient(270deg, var(--blue-800) var(--form-border), transparent 1%),
    linear-gradient(-180deg, var(--blue-800) var(--form-border), transparent 1%),
    linear-gradient(360deg, var(--blue-800) var(--form-border), transparent 1%);
}

.block {
  background-size: var(--form-gap) var(--form-gap);
  background-repeat: round;

  min-height: var(--form-gap);
}

.row {
  display: flex;
  padding: 0 var(--form-gap);
  outline: var(--form-border) solid;
}

#submit-btn {
  flex-grow: 1;
  min-height: calc(var(--form-gap) * 2);

  background-color: var(--red-400);
  border: var(--form-border) solid;
  border-top: 0;
  border-bottom: 0;
}

#submit-btn:hover {
  background-color: salmon;
  cursor: pointer;
}

.header {
  flex-grow: 1;
  background-color: var(--blue-200);
  text-align: center;

  border: var(--form-border) solid;
}

.plate {
  padding: calc(var(--form-gap) * 2);
  background-color: var(--pink-200);
  background-image:
    radial-gradient(circle at center,
      transparent 39%,
      var(--plate) 40%,
      var(--plate) 50%,
      transparent 1%),
    linear-gradient(90deg, var(--plate) var(--form-border), transparent 1%),
    linear-gradient(270deg, var(--plate) var(--form-border), transparent 1%),
    linear-gradient(-180deg, var(--plate) var(--form-border), transparent 1%),
    linear-gradient(360deg, var(--plate) var(--form-border), transparent 1%);

  box-shadow: 0.05rem 0.05rem 0 0rem, 0.1rem 0.1rem 0 0rem;
}
</style>

<template>

  <div class="plate block block-bg_separator">
    <form>
      <fieldset>
        <div class="row block block-bg_separator"></div>
        <div class="row block block-bg_separator">
          <section class="header">
            <h2>Sign Up</h2>
            <p>Have an account?</p>
          </section>
        </div>

        <div>
          <div class="row block block-bg_separator"></div>
          <div class="row block block-bg_separator">
            <section class="input-wrapper">
              <input id="username" placeholder="username" type="text" required />
            </section>
          </div>
          <div class="row block block-bg_separator"></div>

          <div class="row block block-bg_separator">
            <section class="input-wrapper">
              <input id="email" placeholder="email" type="email" required />
            </section>
          </div>
          <div class="row block block-bg_separator"></div>

          <div class="row block block-bg_separator">
            <section class="input-wrapper">
              <input id="password" placeholder="password" type="password" required />
            </section>
          </div>

          <div class="row block block-bg_separator"></div>

          <div class="row block block-bg_separator">
            <button id="submit-btn">submit</button>
          </div>
          <div class="row block block-bg_separator"></div>
        </div>
      </fieldset>
    </form>
  </div>
</template>
