<script>
	import { List, ListGroup, ListItem } from 'konsta/svelte';
</script>

<div class="w-screen flex flex-col items-start">
	<div class="w-full p-4 sticky z-20 top-11">
		<div
			class="relative flex items-center w-full h-12 rounded-lg shadow-lg bg-white overflow-hidden"
		>
			<div class="grid place-items-center h-full w-12 text-gray-300">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-6 w-6"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
					/>
				</svg>
			</div>

			<input
				class="peer h-full w-full outline-none text-lg text-gray-700 pr-2"
				type="text"
				id="search"
				placeholder="Type name, phone number.."
			/>
		</div>
	</div>

	<div class="w-full p-2 -mt-10">
		<List strongIos>
			<ListGroup>
				<ListItem title="A" groupTitle contacts />
				<ListItem title="Aaron" contacts />
				<ListItem title="Abbie" contacts />
				<ListItem title="Adam" contacts />
				<ListItem title="Adele" contacts />
				<ListItem title="Agatha" contacts />
				<ListItem title="Agnes" contacts />
				<ListItem title="Albert" contacts />
				<ListItem title="Alexander" contacts />
			</ListGroup>
			<ListGroup>
				<ListItem title="B" groupTitle contacts />
				<ListItem title="Bailey" contacts />
				<ListItem title="Barclay" contacts />
				<ListItem title="Bartolo" contacts />
				<ListItem title="Bellamy" contacts />
				<ListItem title="Belle" contacts />
				<ListItem title="Benjamin" contacts />
			</ListGroup>
			<ListGroup>
				<ListItem title="C" groupTitle contacts />
				<ListItem title="Caiden" contacts />
				<ListItem title="Calvin" contacts />
				<ListItem title="Candy" contacts />
				<ListItem title="Carl" contacts />
				<ListItem title="Cherilyn" contacts />
				<ListItem title="Chester" contacts />
				<ListItem title="Chloe" contacts />
			</ListGroup>
			<ListGroup>
				<ListItem title="V" groupTitle contacts />
				<ListItem title="Vladimir" contacts />
			</ListGroup>
		</List>
	</div>
</div>
