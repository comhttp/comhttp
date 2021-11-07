<script context="module">

	import Panel from '$lib/helpers/Panel.svelte';
	import CoinButtons from '$lib/components/elements/coin/CoinButtons.svelte';
	import Name from '$lib/components/elements/coin/Name.svelte';
	import Basics from '$lib/components/elements/coin/Basics.svelte';
	import Description from '$lib/components/elements/coin/Description.svelte';
	import Info from '$lib/components/elements/coin/Info.svelte';
	import LastBlocks from '$lib/components/elements/explorer/LastBlocks.svelte';
	import Exchange from '$lib/components/elements/coin/Exchange.svelte';
	import News from '$lib/components/elements/coin/News.svelte';
	import Tools from '$lib/components/elements/coin/Tools.svelte';
	import Specifications from '$lib/components/elements/coin/Specifications.svelte';


	// /**
	//  * @type {import('@sveltejs/kit').Load}
	//  */
	// export async function load({ page, fetch, session, context }) {
	// 	const url = 'https://enso.okno.rs/coins/' + { slug };
	// 	const res = await fetch(url);
	// 	if (res.ok) {
	// 		return {
	// 			props: {
	// 				coin: await res.json(),
	// 				// slug:slug,
	// 			}
	// 		};
	// 	}
	// 	return {
	// 		// slug:slug,
	// 		status: res.status,
	// 		error: new Error(`Could not load ${url}`)
	// 	};
	// }
</script>

<!--{coin.slug}-->
<script>
	export let slug;
</script>
{slug}

<amp-state id="blocks" src="https://enso.okno.rs/explorer/{slug}/blocks/10/1"></amp-state>

<div class="container mx-auto mb-8 px-4 px-0 flex flex-col flex-1 content main-wrap">
	<div class="flex flex-col py-12"><Name /></div>
	<div class="grid grid-cols-6 gap-5">
		<div class="col-span-full md:col-span-4 lg:col-span-4 grid grid-cols-3 gap-5">
			<Panel class="col-span-2"><Basics name={slug} /></Panel>
			<Panel class="col-span-1"><Specifications name={slug}/></Panel>
			<Panel class="col-span-3"><Description name={slug}/></Panel>
			<Panel class="col-span-3"><Info slug={slug} /></Panel>
			<Panel class="col-span-3"><LastBlocks name={slug} slug={slug}/></Panel>
			<Panel class="col-span-1"><Exchange /></Panel>
			<Panel class="col-span-1"><News /></Panel>
			<Panel class="col-span-1"><Tools /></Panel>



		</div>
		<div class="col-span-full md:col-span-2 flex flex-col">
			<div class="grid grid-cols-2 gap-3">
				<CoinButtons />
			</div>
		</div>
	</div>
</div>



