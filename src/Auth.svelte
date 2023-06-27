<script>
    let user = {
        logged: false
    }

    const login = () => {
        user.logged = true;
    }

    const logout = () => {
        user.logged = false;
    }
</script>

{#if user.logged}
    <button style="background: blue; color:white" on:click={logout}>Logout</button>
{:else}
    <button   style="background: blue; color:white" on:click={login}>Login</button>
{/if}
