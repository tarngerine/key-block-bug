<script>
	import Header from './Header.svelte';
	import KeyBlock from './KeyBlock.svelte';
</script>

<Header />
<h1>Home page</h1>
<p>To see the bug, click back and forth between Test and Index a few times</p>
<p>Expected: going to test removes all index content immediately, and vice versa</p>
<p>
	Actual: If going from Index -> Test, Index will remain at the bottom of the page for a bit, there
	are some ghost keys insert at the top, invisible, too. It's non deterministic
</p>
<p>
	This effect is more pronounced the more KeyBlock components you have. This repro starts with just
	one on index, but you can add more to both index and test to see the effect compounded.
</p>

<KeyBlock />
<!-- <KeyBlock />
<KeyBlock />
<KeyBlock />
<KeyBlock /> -->
