<script>
	import Intro from './component/Intro.svelte';
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';

	onMount(() => {
		const location = window.location.href;

		if (location != `${location}/login`) {
			if (localStorage.getItem('isLogin') != 'true') {
				goto('/login');
			}
		}
	});
</script>

<svelte:head>
	<title>Beranda</title>
</svelte:head>

<section>
	<Intro />
</section>
