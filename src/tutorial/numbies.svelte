<!-- Svelte's reactivity is triggered by assignments. Methods that mutate arrays or objects will not trigger updates by themselves.

Two ways to tell the compiler it has changed are by assigning the variable to itself, or using ES6 spread syntax -->

<script>
	let numbers = [1, 2, 3, 4];

	function addNumber() {
		numbers.push(numbers.length + 1);
    // numbers = numbers;
    numbers = [...numbers, numbers.length + 1];

	}

	$: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}>
	Add a number
</button>