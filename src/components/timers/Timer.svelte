<script>
    let timerState = 0;
	let elapsedTime = 0;
	// rounded dependent var ??^
	let interval = 0;
	function handleStart() {
		let startTime = Date.now()
		interval = setInterval(() => {
			const now = Date.now()
			elapsedTime = now - startTime
			console.log(elapsedTime)
		}, 1000)
		timerState = 1
	}
</script>

<section>
    <p class="time">{Math.round(elapsedTime/1000)}</p>
    <button on:click={handleStart}>Start</button>
</section>

<style>
    section{
        margin: .5em;
    }
</style>