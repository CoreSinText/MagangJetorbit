<script>
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';
	const profileImage = '/razak_profile.jpeg';

	onMount(() => {
		const location = window.location.href;

		if (location != `${location}/login`) {
			if (localStorage.getItem('isLogin') != 'true') {
				goto('/login');
			}
		}
	});
</script>

<section class="w-full h-screen flex justify-center items-center px-36">
	<figure class="flex w-[800px] space-x-4 border-2 p-2 rounded-lg shadow-lg">
		<img src={profileImage} alt="photo-profile" class="w-[200px] rounded-lg" />
		<figcaption class="font-roboto text-lg">
			Saya adalah seorang mahasiswa di Universitas Teknologi Yogyakarta, saya memiliki keinginanan
			untuk meningkatkan skill yang saya miliki
		</figcaption>
	</figure>
</section>
