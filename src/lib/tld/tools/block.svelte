<script context="module">
	import Panel from '$lib/helpers/Panel.svelte';
	import Block from '$lib/components/elements/explorer/Block.svelte';
</script>
<script>
	export let slug;
	export let vars;
</script>





<div class="container mx-auto mb-8 px-4 px-0 flex flex-col flex-1 content main-wrap">
	<div class="flex flex-col py-12">Block </div>
	<div class="grid grid-cols-6 gap-5">
			<Panel class="col-span-6"><Block vars={vars} slug={slug}></Block></Panel>
	</div>
</div>

