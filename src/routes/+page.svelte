<script lang="ts">
	import { Dropdown } from '$lib';
	let options = ['First Item', 'Second Item', 'Third Item', 'Fourth Item', 'Fifth Item'];
</script>

<h1 class="text-center text-2xl font-bold m-5">Dropdown Component</h1>

<div class="flex gap-5 justify-center">
	<Dropdown options={options} />
	<Dropdown options={options} status={true} />
	<Dropdown options={options} status={true} defaultSelectedOption={options[2]} />
	<Dropdown options={options} status={false} defaultSelectedOption={options[2]} />
</div>
