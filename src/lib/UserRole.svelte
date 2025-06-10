<script>
  let role = "admin"
</script>

{#if role == "admin"}
  <h1>Welcome, {role}!</h1>
  <p>You have full access to the system.</p>
{:else if role == "user"}
  <h1>Welcome, {role}!</h1>
  <p>Your access is limited.</p>
{:else if role == "editor"}
  <h1>Welcome, {role}!</h1>
  <p>You can edit content but have limited access.</p>
{:else if role == "guest"}
  <h1>Welcome, {role}!</h1>
  <p>You have view-only access.</p>
{/if}

<select bind:value={role}>
  <option value="admin">Admin</option>
  <option value="user">User</option>
  <option value="editor">Editor</option>
  <option value="guest">Guest</option>
</select>
