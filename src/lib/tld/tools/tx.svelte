<script context="module">

import Panel from '$lib/helpers/Panel.svelte';
	import Tx from '$lib/components/elements/explorer/Tx.svelte';

</script>
<script>
	export let slug;
	export let vars;
</script>

<svelte:head>
    <script async custom-element="amp-render" src="https://cdn.ampproject.org/v0/amp-render-1.0.js"></script>
	<link rel="preload" href="https://enso.okno.rs/explorer/parallelcoin/tx/{vars}" as="fetch">
</svelte:head>



<div class="container mx-auto mb-8 px-4 px-0 flex flex-col flex-1 content main-wrap">
	<div class="flex flex-col py-12">Transaction </div>
	<div class="grid grid-cols-6 gap-5">
			<Panel class="col-span-5"><Tx vars={vars} slug={slug}></Tx></Panel>
	</div>
</div>

