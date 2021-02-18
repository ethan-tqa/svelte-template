<script lang="typescript">
  import './Tw.svelte';

  import { onMount } from "svelte";
  let count: number = 0;
  onMount(() => {
    const interval = setInterval(() => count++, 1000);
    return () => {
      clearInterval(interval);
    };
  });
</script>

<div class="App my-2 bg-gray-400">
  <header class="App-header ring-offset-red-800 h-14">
    <img src="/logo.svg" class="App-logo h-8" alt="logo" />
    <p>Edit <code>src/App.svelte</code> and save to reload.</p>
    <p>Page has been open for <code>{count}</code> seconds.</p>
    <p>
      <a
        class="App-link"
        href="https://svelte.dev"
        target="_blank"
        rel="noopener noreferrer"
      >
        Learn Svelte
      </a>
    </p>
  </header>
</div>

<style>
</style>