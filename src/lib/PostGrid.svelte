<script lang="ts">
	import PostTile from './PostTile.svelte';

	export let posts;
</script>

<div class="post-grid">
	{#each posts as item}
		<PostTile post={item} />
	{/each}
</div>

<style>
	.post-grid {
		display: grid;
		grid-gap: 50px;
		grid-template-columns: repeat(auto-fit, minmax(300px, 45%));
		margin: 50px 50px;
	}
</style>
