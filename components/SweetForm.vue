<script lang="ts"></script>

<style>
:root {
  --form-gap: 1rem;
  --form-border: 0.05rem;
}

form {
  display: grid;
  background-color: white;
  box-shadow: 0.05rem 0.05rem 0 0.05rem, 0.1rem 0.1rem 0 0.05rem;
}

input {
  min-height: calc(var(--form-gap) * 2);
}

fieldset {
  display: grid;
}

.input-wrapper {
  display: grid;

  border: var(--form-border) solid;
  border-top: 0;
  border-bottom: 0;

  /* padding: 0 var(--form-gap); */
  background: olivedrab;
}

.block-bg {
  background:
    radial-gradient(circle at center, #051c56 50%, transparent 1%);
}

.block-bg_separator {
  background:
    radial-gradient(circle at center, #051c56 50%, transparent 1%),
    linear-gradient(90deg, #051c56 var(--form-border), transparent 1%),
    linear-gradient(270deg, #051c56 var(--form-border), transparent 1%),
    linear-gradient(-180deg, #051c56 var(--form-border), transparent 1%),
    linear-gradient(360deg, #051c56 var(--form-border), transparent 1%);
}

.block {
  background-size: var(--form-gap) var(--form-gap);
  /* background-position: 0 center; */
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

  background-color: white;
  border: calc(var(--form-border) * 2) solid;
  border-top: 0;
  border-bottom: 0;
}

#submit-btn:hover {
  background-color: lightgray;
  cursor: pointer;
}
</style>

<template>
  <form>
    <fieldset>
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
</template>
