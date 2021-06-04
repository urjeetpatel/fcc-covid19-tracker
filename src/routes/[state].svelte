<script lang="ts" context="module">
	export async function load({ page }) {
		let retval = { props: { state: page.params['state'] } };
		return retval;
	}
</script>

<script lang="ts">
	import CovidStat from '../components/CovidStat.svelte';
	import CovidChart from '../components/CovidChart.svelte';
	export let state: string;
</script>

<h1>{state}</h1>

<CovidChart />
<CovidStat />
