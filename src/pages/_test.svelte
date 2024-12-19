<script lang="ts">
	import { setContext } from "svelte";
	// import Nested from "./_nested.svelte";

	type Props = {
		children: any;
	};
	let count = $state(0);
	let { children }: Props = $props();

	// setContext("count", {
	//   increment: () => count++,
	//   decrement: () => count--,
	// });
</script>

<!-- <Nested /> -->
<div>
	{@render children?.()}
</div>

<button onclick={() => count++}>Increment</button>
<div class="count">
	{count}
</div>

<button onclick={() => count--}>Decrement</button>
