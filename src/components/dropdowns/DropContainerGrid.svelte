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
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-auto-rows: min-content;
        gap: 10px;
        padding: 5px;
        max-width: 600px;
        margin: 0 auto;
    }
</style>
