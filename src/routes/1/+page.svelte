<script>
	import Button from './Button.svelte'
	let name = 'world';
</script>

<h1>Hello, {name}!</h1>
<Button>
	Toggle
</Button>

<style>
	:global(body) {
		background-color: #f2eee2;
		color: #0084f6;
		transition: background-color 0.3s
	}
	:global(body.dark-mode) {
		background-color: #1d3040;
		color: #bfc2c7;
	}
</style>