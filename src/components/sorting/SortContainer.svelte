<script>

import SortCard from "./SortCard.svelte";

    let peopleData = [
        {
            name: "Jeremy",
            position: "CMO",
            age: 25,
            bio: "eye emoji",
        },
        {
            name: "Jaime",
            position: "Slugma",
            age: 28,
            bio: "flushed face emoji",
        },
        {
            name: "Jessica",
            position: "Ligma",
            age: 27,
            bio: "pleading face emoji",
        },
    ];
</script>

<section>
    {#each peopleData as person, i}
        <!-- <SortCard /> -->
        <SortCard {...person} />
    {/each}
</section>

<style>
    section {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 0.5rem;
        max-width: 750px;
        margin: 0 auto;
    }
</style>
