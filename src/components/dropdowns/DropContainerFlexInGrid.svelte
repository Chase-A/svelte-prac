<script>
    import Dropdown from "./Dropdown.svelte";
</script>

<section>
    <div class="col">
        {#each { length: 6 } as _, i}
            <Dropdown margined={true}/>
        {/each}
    </div>
    <div class="col">
        {#each { length: 7 } as _, i}
            <Dropdown margined={true}/>
        {/each}
    </div>
</section>

<style>
    section {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-auto-rows: min-content;
        max-width: 600px;
        margin: 0 auto;
    }
    .col{
        margin: 0;
    }
</style>
