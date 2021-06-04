<script lang="ts">
	import { page, navigating } from '$app/stores';
	import '../global.scss';
	import Nav from '../components/Nav.svelte';

	$: section = $page.path.split('/')[1];
</script>

<Nav {section} />
<main>
	<slot />
</main>
