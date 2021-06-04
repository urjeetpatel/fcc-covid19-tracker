<script context="module">
	export function load({ error, status }) {
		return {
			props: {
				title: `${status}: ${error.message}`,
				status: status,
				error: error
			}
		};
	}
</script>

<script>
	export let title;
	export let status;
	export let error;
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<h1>{title}</h1>
<h2>Code: {status}</h2>
<pre>{error.stack}</pre>
