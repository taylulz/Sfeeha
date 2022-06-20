<script lang="ts">
  import logo from './assets/svelte.png'
  import Counter from './lib/Counter.svelte'
  let count = 0;
  $: doubled = count * 2;

	function incrementCount() {
    count += 1;
  }
</script>

<button on:click={incrementCount}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

<p> reactive declaration using $: syntax</p>
<p>the count: {count} has been doubled: {doubled}</p>