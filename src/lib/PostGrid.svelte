<script lang="ts">
	import type { Post } from './post';
	import PostTile from './PostTile.svelte';

	export let posts: Array<Post>;
</script>

<div class="post-grid">
	{#each posts as item}
		<PostTile post={item} />
	{/each}
</div>

<style>
	.post-grid {
		display: grid;
		grid-gap: 25px;
		grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
	}
</style>
