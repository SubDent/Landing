<script lang="ts">
  export let label: string;
  export let value: string;
  export let required: boolean;
</script>

<div class="input">
  <label for={label}>{label}</label>
  <input
    type="text"
    name={label}
    id={label}
    bind:value
    autocomplete="email"
    inputmode="email"
    {required}
  />
</div>

<style>
  .input {
    display: flex;
    padding-bottom: var(--size-3);
    flex-direction: column;
    width: 100%;
  }
  input {
    border: none;
    padding: 0.4rem;
    width: auto;
  }
</style>
