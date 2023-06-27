<script>
    let count = 0
    let count2 = 0
// reactta use mmemo gibi 
    $: doubled = count * 2;

    $:console.log(`The count is ${count}`);
    $:console.log(`The count is ${count2}`);
    const  handleClick = () => {
        count += 1;
    }
    const  handleClick2 = () => {
        count2 += 1;
    }
</script>

<button on:click={handleClick}>
    Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

{#if count % 2 === 0}
    <p style="background: blue; color:white">{count} is even</p>
{:else}
    <p style="background: yellow;"> {count} is odd</p>
{/if}

<p>
    Bu sayı {doubled} değerindedir.
</p>
<button on:click={handleClick2}>
    Clicked {count2} {count2 === 1 ? 'time' : 'times'}
</button>