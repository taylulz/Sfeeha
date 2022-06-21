<script>
	let x = 1;
$: displayCount = x;

function incrementCount() {
  x += 1;
}
</script>

{#if x > 10}
	<p>{x} is greater than 10</p>
{:else if 5 > x}
	<p>{x} is less than 5</p>
{:else}
	<p>{x} is between 5 and 10</p>
{/if}

<button on:click={incrementCount}>
  the count is {displayCount}
</button>