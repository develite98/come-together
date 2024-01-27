<script lang="ts">
	import { goto } from '$app/navigation';
	import { page } from '$app/stores';
</script>

<div class="w-full h-screen">
	<div class="bg-white flex flex-col h-screen mx-auto max-w-md login text-gray-600">
		<div class="h-14 p-6 !pb-10 text-center">
			<span class="text-2xl text-sky-500 font-medium">LOGO</span>
		</div>
		<div
			class="border-b flex items-center justify-around border-gray-200 dark:bg-gray-700 dark:border-gray-600 rounded-br-2xl rounded-bl-2xl"
		>
			<button
				type="button"
				class="inline-flex grow flex-col items-center justify-center p-4 group border-b"
				class:border-primary={$page.route.id === '/app/home'}
				on:click={() => goto('/app/home')}
			>
				<svg
					class="w-5 h-5 mb-1 text-gray-500 dark:text-gray-400"
					class:text-sky-500={$page.route.id === '/app/home'}
					aria-hidden="true"
					xmlns="http://www.w3.org/2000/svg"
					fill="currentColor"
					viewBox="0 0 20 20"
				>
					<path
						d="m19.707 9.293-2-2-7-7a1 1 0 0 0-1.414 0l-7 7-2 2a1 1 0 0 0 1.414 1.414L2 10.414V18a2 2 0 0 0 2 2h3a1 1 0 0 0 1-1v-4a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v4a1 1 0 0 0 1 1h3a2 2 0 0 0 2-2v-7.586l.293.293a1 1 0 0 0 1.414-1.414Z"
					/>
				</svg>
				<span class="sr-only">Home</span>
			</button>
			<button
				type="button"
				class="inline-flex grow flex-col items-center justify-center p-4 group border-b hover:border-primary"
				class:border-primary={$page.route.id === '/app/contact'}
				on:click={() => goto('/app/contact')}
			>
				<svg
					class="w-5 h-5 mb-1 text-gray-500 dark:text-gray-400"
					class:text-sky-500={$page.route.id === '/app/contact'}
					aria-hidden="true"
					xmlns="http://www.w3.org/2000/svg"
					fill="currentColor"
					viewBox="0 0 14 20"
				>
					<path
						d="M13 20a1 1 0 0 1-.64-.231L7 15.3l-5.36 4.469A1 1 0 0 1 0 19V2a2 2 0 0 1 2-2h10a2 2 0 0 1 2 2v17a1 1 0 0 1-1 1Z"
					/>
				</svg>
				<span class="sr-only">Bookmark</span>
			</button>
			<button
				type="button"
				class="inline-flex grow flex-col items-center justify-center p-4 group border-b"
				class:border-primary={$page.route.id === '/app/profile'}
				on:click={() => goto('/app/profile')}
			>
				<svg
					class="w-5 h-5 mb-1 text-gray-500 dark:text-gray-400"
					aria-hidden="true"
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 20 20"
				>
					<path
						stroke="currentColor"
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="m19 19-4-4m0-7A7 7 0 1 1 1 8a7 7 0 0 1 14 0Z"
					/>
				</svg>
				<span class="sr-only">Search</span>
			</button>
		</div>

		<slot />
	</div>
</div>
