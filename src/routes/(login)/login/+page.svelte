<script>
	import { goto } from '$app/navigation';
	import axios from 'axios';

	let username = '';
	let password = '';

	$: submit = async () => {
		const response = await axios({
			method: 'post',
			url: 'https://dummyjson.com/auth/login',
			headers: {},
			data: {
				username,
				password
			}
		});

		if (response.status === 200) {
			goto('/');
		}
		console.log(response);
	};
</script>

<section class="w-screen h-screen flex justify-center items-center bg-blue-600 font-roboto">
	<form
		on:submit|preventDefault={submit}
		action=""
		class="flex flex-col w-[500px] h-[300px] shadow-lg justify-evenly p-4 rounded-md bg-blue-800 text-white"
	>
		<h1 class="text-center text-3xl font-bold">Login Dulu !</h1>
		<div class="flex flex-col my-2">
			<label for="username">Username</label>
			<input bind:value={username} type="text" name="username" class="p-2 rounded-lg text-black" />
		</div>

		<div class="flex flex-col my-2">
			<label for="password">Password</label>
			<input
				bind:value={password}
				type="password"
				name="password"
				class="p-2 rounded-lg text-black"
			/>
		</div>
		<button type="submit" class="bg-blue-500 w-fit mx-auto py-2 px-6 rounded-lg">Login</button>
	</form>
</section>
