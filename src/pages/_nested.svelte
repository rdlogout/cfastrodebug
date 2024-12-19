<script lang="ts">
  import { getContext } from "svelte";

  let count = getContext("count");
</script>

<div>
  Nested: {count}
</div>

<button onclick={() => count.increment()}>Increment</button>
<button onclick={() => count.decrement()}>Decrement</button>
