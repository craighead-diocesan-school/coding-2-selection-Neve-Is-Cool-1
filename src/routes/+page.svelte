<script>
  import Header from "$lib/Header.svelte"
  import UserRole from "$lib/UserRole.svelte"
  let name = "Alice"
</script>

<Header />

<main class="content section">
  <div class="box">
    <input bind:value={name} placeholder="Enter your name" />
    {#if name == "Alice"}
      <h1>Welcome back, Alice!</h1>
    {:else if name == "Bob"}
      <h1>Not you again!</h1>
    {:else}
      <h1>Hello, {name}!</h1>
    {/if}
  </div>
  <div class="box">
    <UserRole />
  </div>
</main>

<footer class="footer">
  <p class="has-text-centered">&copy; Craighead Diocesan School 2025</p>
</footer>
