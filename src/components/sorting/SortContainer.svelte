<script>

import Buttons from './Buttons.svelte'
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
            age: 88,
            bio: "flushed face emoji",
        },
        {
            name: "Jessica",
            position: "Ligma",
            age: 27,
            bio: "pleading face emoji",
        },
        {
            name: "Hector",
            position: "Slugma",
            age: 47,
            bio: "wet emoji",
        },
        {
            name: "Jeff",
            position: "CMO",
            age: 17,
            bio: "wet emoji",
        },
    ];
</script>

<Buttons/>

<section>
    {#each peopleData as person, i}
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
