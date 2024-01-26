<script>
	import { List, ListGroup, ListItem, Searchbar } from 'konsta/svelte';
</script>

<div class="grow overflow-auto w-screen flex flex-col items-start">
	<div class="w-64 ml-4 p-2 sticky top-0 bg-white z-20">
		<Searchbar disableButton disableButtonText="Cancel" value={''} />
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
