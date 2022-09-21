<script lang="ts">
  import Input from "../components/Input.svelte";

  $: form = { email: "", name: "" };

  function submit(e) {
    console.log(form);
  }
</script>

<form on:submit={submit}>
  <Input bind:value={form.name} label="name" required />
  <Input bind:value={form.email} label="email" required />
  <button type="submit">join</button>
</form>

<style scoped>
  form {
    padding: var(--size-3);
    background: #00000022;
    box-shadow: var(--shadow-2);
    max-width: 40ch;
    border-radius: var(--radius-3);
    margin-top: var(--size-3);
    margin-bottom: var(--size-3);
  }
</style>
