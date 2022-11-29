<script>
	const logo1 = '/jetorbit-astro-peace-logo.png';
</script>

<svelte:head>
	<title>About</title>
</svelte:head>

<section class="w-full bg-gray-900 flex justify-center items-center h-screen relative">
	<div class="flex justify-center items-center w-3/4">
		<div
			class="w-[569px] border-2 p-4 rounded-lg border-purple-200 shadow-lg shadow-purple-700/100"
		>
			<p class="font-roboto text-white">
				Jetorbit (PT Jetorbit Teknologi Indonesia) adalah perusahaan yang menyediakan web hosting
				indonesia terbaik dan domain murah di tahun 2020 ini. Buat web jadi lebih mudah dengan
				layanan hosting murah indonesia kami yang prima baik dari segi kualitas produk, bantuan
				teknis, data center dan juga komposisi piranti lunak yang kami gunakan.
			</p>
		</div>
		<img src={logo1} alt="" class="w-60" />
	</div>
</section>
