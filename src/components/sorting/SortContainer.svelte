<script>

import ButtonContainer from './ButtonContainer.svelte'
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
        {
            name: "Antonio",
            position: "CMO",
            age: 56,
            bio: "moist emoji",
        },
        {
            name: "Augustus",
            position: "Ligma",
            age: 26,
            bio: "moisturizer emoji",
        },
    ];

    const categories = ['All', 'CMO', 'Slugma', 'Ligma']
    let selected = 'All'

    function filterSelection(e) {
        console.dir(e.target.dataset.name)
        selected = e.target.dataset.name
    }
</script>

<ButtonContainer>
    {#each categories as category}
        <button class="btn" class:active={selected === category} data-name={category} on:click={filterSelection}>{category}</button>
    {/each}
</ButtonContainer>

<section>
    {#each peopleData as person, i}
    {#if person.position === selected || selected === 'All'} 
        <SortCard {...person} />
    {/if}
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

    /* Style the buttons */
.btn {
	text-transform: uppercase;
	font-weight: 900;
	font-size: 1.2rem;
	border: 4px solid #000;
	margin: 5px;
	padding: 12px 10px 10px 10px;
	background-color: white;
	cursor: pointer;
    line-height: 1rem;
}


	/* Add a dark background color to the active button */
.btn:active,
.active {
	background-color: #000;
	color: white;
}
</style>
