<script>
	import Nested from "../lib/Nested.svelte";
  import Info from "../lib/Info.svelte";

  const pkg = {
    name: 'svelte-tutorial',
    version: '0.0.1',
    speed: 'fast',
    website: 'https://svelte.dev'
  };
</script>

<Nested answer={42}/>
<Nested/>
<Info {...pkg} />