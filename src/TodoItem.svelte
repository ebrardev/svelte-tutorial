<script>
    export let todo;
    export let i;
    const emojis = ['🥵','😁','😘']
    const emoji = emojis[i]
</script>
<li>{todo.title} - {todo.completed} - {emoji} </li>