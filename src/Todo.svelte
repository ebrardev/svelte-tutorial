<script>
    import TodoItem from './TodoItem.svelte';
    let todos = [
        {
            id: 1,
            title: "Todo 1",
            completed: false
        },
        {
            id: 2,
            title: "Todo 2",
            completed: false
        },
        {
            id: 3,
            title: "Todo 3",
            completed: false
        }
    ]
    const clickHandler = () => {
     todos= todos.slice(1)
    }
</script>
<button on:click={clickHandler}>Delete todo</button>

    <ul>
        {#each todos as todo,i}
         <TodoItem {todo} {i} />
           
        {/each}
    </ul>
