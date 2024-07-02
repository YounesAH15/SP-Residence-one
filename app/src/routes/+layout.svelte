<script>
	import '../app.css';
</script>

<main>
	<slot></slot>
</main>

<style>
	main {
		width: 80vw;
		max-width: 80vw;
		margin: auto;
		font-size: medium;
	}
	:global(label) {
        margin: 20px 10px
    }

    :global(input) {
        border: 0px;
        border-bottom: 1px dashed black;
        margin-left: 15px;
        justify-self: center;
        align-self: center;
    }


</style>
