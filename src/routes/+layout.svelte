<script>
	import "../lib/fonts.css";
	let { children } = $props();
</script>

<style>
	nav {
		background: orange;
		overflow: hidden;
	}
</style>


<nav>
		<p>FriendShip</p>
</nav>

{@render children()}