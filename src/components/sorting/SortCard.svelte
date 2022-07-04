<script>
export let name = 'Name'
export let position = 'Position'
export let age = 0
export let bio = 'bio'
</script>

<section>
    <div class="flexy">
        <h2>{name}</h2>
        <div><h1>{position}</h1><h1>{age}</h1></div>
    </div>
    <p class="bio">{bio}</p>
</section>

<style>
    section{
        border: .25rem solid #000;
        padding: .75rem;
        text-align: left;
    }
    .flexy{
        display: flex;
        justify-content: space-between;
    }
</style>