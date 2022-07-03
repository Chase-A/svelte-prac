<script>
    import Dropdown from "./Dropdown.svelte";
</script>

<section>
    {#each { length: 6 } as _, i}
        <Dropdown />
    {/each}
</section>

<style>
    section {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        gap: 10px;
        padding: 5px;
        width: 700px;
        margin: 0 auto;
        border: 2px solid fuchsia;
    }
</style>
