<script lang="ts">
	const options: Intl.DateTimeFormatOptions = {
		weekday: 'long',
		year: 'numeric',
		month: 'long',
		day: 'numeric'
	};

	let data = [
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		},
		{
			title: '',
			date: new Date(),
			level: 5
		}
	];
</script>

<div class="p-2 !pt-4 w-full home">
	{#each data as item}
		<div class="flex flex-col items-start rounded-xl bg-white p-4 shadow-lg mb-4">
			<h2 class="font-semibold">
				{item.date.toLocaleDateString('vi-VN', options)}
			</h2>
			<p class="mt-2 text-sm text-gray-500">Last opened 4 days ago</p>
		</div>
	{/each}
</div>

<!-- <div class="w-screen flex justify-center gap-2 items-center fixed bottom-5 right-0">
	<button
		class="text-white px-4 w-auto h-12 bg-second rounded-full touchable mouse shadow transition ease-in duration-200 focus:outline-none"
	>
		<span>Theo dõi</span>
	</button>

	<button
		class="text-white px-4 w-auto h-12 bg-primary rounded-full touchable mouse shadow transition ease-in duration-200 focus:outline-none"
	>
		<svg viewBox="0 0 20 20" enable-background="new 0 0 20 20" class="w-6 h-6 inline-block">
			<path
				fill="#FFFFFF"
				d="M16,10c0,0.553-0.048,1-0.601,1H11v4.399C11,15.951,10.553,16,10,16c-0.553,0-1-0.049-1-0.601V11H4.601
							C4.049,11,4,10.553,4,10c0-0.553,0.049-1,0.601-1H9V4.601C9,4.048,9.447,4,10,4c0.553,0,1,0.048,1,0.601V9h4.399
							C15.952,9,16,9.447,16,10z"
			/>
		</svg>
		<span>Tham gia</span>
	</button>
</div> -->

<style lang="scss">
</style>
