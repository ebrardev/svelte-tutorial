<script>

    export let comp = 'svelte';
</script>

<div>
    <h1>{comp.toUpperCase()}</h1>   
</div>

<style lang="scss">
    @import "styles/variables";

    div {
        text-align: center;
        padding: 1em;
        max-width: 240px;
        margin: 0 auto;
    }

    h1 {
        color: orangered  ;
        text-transform: uppercase;
        font-size: 4em;
        font-weight: 100;
    }

</style>
