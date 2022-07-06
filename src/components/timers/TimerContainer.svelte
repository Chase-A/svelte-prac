<script>
    import Timer from "./Timer.svelte";
</script>

<section>
    {#each {length: 3} as _}
    <Timer />
    {/each}
</section>

<style>
    section{
        display: flex;
        margin: 0 auto;
        width:fit-content;
        border: 1px solid slateblue;
    }
</style>