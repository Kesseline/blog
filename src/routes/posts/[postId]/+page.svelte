<script lang="ts">
	import type { LayoutData } from './$types';
	import Header from '../../../lib/Header.svelte';

	export let data: LayoutData;
	$: post = data.post;
</script>

<Header />

<div class="post">
	<h1 class="title">{post?.title}</h1>
	<div class="content">
		{post?.content}
	</div>
</div>

<style>
	.post {
		color: black;
		border-radius: 25px;
		padding-top: 20px;
		background-color: #f5f4f0;
		border: 2px solid black;
		height: fit-content;
		text-decoration: none;
		margin: 50px 30px;
	}

	.title {
		text-align: center;
		margin: 0 10px;
	}

	.content {
		bottom: 10px;
		font-size: medium;
		margin: 50px;
	}
</style>
