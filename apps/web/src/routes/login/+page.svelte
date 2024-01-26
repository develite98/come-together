<script lang="ts">
	import { goto } from '$app/navigation';
</script>

<div class="h-screen w-full">
	<div class="bg-gray-800 h-screen mx-auto max-w-md login">
		<div class="p-10 mt-2">
			<p class="text-5xl pt-10 text-yellow-500 font-bold">
				Welcome <br />
			</p>
			<p class="text-xl py-3 text-gray-400 font-semibold">Let's come together 😍</p>
		</div>
		<div class="mx-10 p-3 rounded-xl shadow-sm bg-gray-900">
			<div class="p-1 mx-2">
				<input
					placeholder="Tell me your phone"
					class="bg-transparent text-yellow-500 w-full focus:outline-none focus:rang"
					type="tel"
				/>
			</div>
		</div>

		<div class="w-full px-10 py-4">
			<button
				class=" bg-yellow-500 font-medium p-3 rounded-3xl w-full h-full hover:bg-yellow-600 relative touchable"
				on:click={() => goto('app/home')}
			>
				Play
			</button>
		</div>
	</div>
</div>

<style>
	.login {
		background-image: url(https://e1.pxfuel.com/desktop-wallpaper/963/271/desktop-wallpaper-android-mobile-apps-flat-mountain-mobile-mountain-mobile.jpg);
		background-position: left;
		padding-top: 15%;
	}
</style>
