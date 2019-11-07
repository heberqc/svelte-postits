<script>
	import Post from './Post.svelte'
	export let title
	let postsCount = 0
	const addPostIt = async () => {
		await new Post({
			target: document.querySelector('.postItBoard'),
			props: {
				message: prompt('Enter a message:'),
			},
		})
		postsCount += 1;
	}
</script>

<style>
	h1 {
		background-color: #42dee1;
		/* color: #3fc5f0; */
	}
	.postItBoard {
		padding: 1rem;
		display: flex;
		flex-wrap: wrap;
		justify-content: start;
	}
</style>

<h1>{title} ({postsCount})</h1>
<button on:click={addPostIt}>Add Post</button>
<div class="postItBoard"></div>
