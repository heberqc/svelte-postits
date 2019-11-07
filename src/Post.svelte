<script>
	export let message
</script>

<style>
	.postit {
		background-color: #eef5b2;
		box-shadow: 5px 5px 10px #282828;
		box-shadow: 5px 5px 10px rgba(40,40,40,.8);
		padding: 1rem;
		margin: .5rem;
		width: 16rem;
	}
	.message {
		min-height: 3rem;
		max-height: 3rem;
	}
</style>

<div class="postit">
	<span class="message">{message}</span>
</div>
