<script>
	export let name;
	export let version;
	export let speed;
	export let website;
</script>

<style>
  * {
    font-size: 2em;
  }

  .header {
    color: red;
  }
  
</style>

<h1 class="header">
  ALL THIS IS PLACEHOLDER TEXT IN INFO COMPONENT. The variables are set up, but not defined, here. The props actually come from the Propies component 
</h1>
<p class="content">
	Name: {name} 
  Speed: {speed} fast.
	Version: {version} 
  Link: <a href="https://www.npmjs.com/package/{name}">npm</a>
	and <a href={website}>learn more here</a>
</p>