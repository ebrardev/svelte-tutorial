<script>
    let data = null;
    let error = null;
  
    const getPost = () =>
      fetch('https://jsonplaceholder.typicode.com/posts')
        .then((res) => res.json())
        .then((response) => {
          data = response;
        })
        .catch((err) => {
          error = err;
        });
  </script>
  
  <h3>await block</h3>
  
  {#if data}
    {#each data as post (post.id)}
      <div>
        <h3>{post.title}</h3>
        <p>{post.body}</p>
      </div>
    {/each}
  {:else if error}
    <p style="color: red">{error.message}</p>
  {:else}
    <p>Waiting for post...</p>
  {/if}
  
  <button on:click={getPost}>Get Post</button>
  