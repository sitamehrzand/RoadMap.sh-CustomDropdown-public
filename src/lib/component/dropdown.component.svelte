<script lang="ts">
	let { status = false, options = ['1', '2', '3'], defaultSelectedOption = 'Select Item' } = $props();
	let isOpen = $state(status);
	let selectedOption = $state(defaultSelectedOption);

	function selectOption(option: string) {
		selectedOption = option;
		isOpen = false;
	}
</script>

<div class="relative">
	<button
		type="button"
		class="m-5 cursor-pointer rounded-md border border-black px-2 py-1"
		onclick={() => {
			isOpen = !isOpen;
		}}
	>
		<div class="flex items-center gap-2">
			<p>{selectedOption}</p>
			<img
				src="https://img.icons8.com/ios/50/000000/chevron-down.png"
				alt="chevron-down"
				class="h-4 w-4"
			/>
		</div>
	</button>
	<div class:hidden={!isOpen} class="absolute">
		<ul class="mx-5 flex w-fit flex-col rounded-md border border-black">
			{#each options as option}
				<button
					type="button"
					class="cursor-pointer border-b border-black p-1 last:border-b-0 hover:bg-gray-200 hover:first:rounded-t-md hover:last:rounded-b-md"
					class:bg-gray-200={selectedOption === option}
					class:rounded-t-md={selectedOption === option && options.indexOf(option) === 0}
					class:rounded-b-md={selectedOption === option &&
						options.indexOf(option) === options.length - 1}
					onclick={() => {
						selectOption(option);
					}}>{option}</button
				>
			{/each}
		</ul>
	</div>
</div>
