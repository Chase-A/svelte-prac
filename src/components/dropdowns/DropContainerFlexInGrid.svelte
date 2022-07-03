<script>
    import Dropdown from "./Dropdown.svelte";
</script>

<section>
    <div class="col">
        {#each { length: 3 } as _, i}
            <Dropdown/>
        {/each}
    </div>
    <div class="col">
        {#each { length: 3 } as _, i}
            <Dropdown />
        {/each}
    </div>
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
    .col section{
        padding-bottom: 10px;
    }
</style>
