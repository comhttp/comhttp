<script context="module">
	/**
	 * @type {import('@sveltejs/kit').Load}
	 */
	import Bg from '../../components/helpers/Bg.svelte';
	import Header from '../../components/Header.svelte';
	import Footer from '../../components/Footer.svelte';
	import Panel from '../../components/helpers/Panel.svelte';
	import CoinButtons from '../../components/coin/CoinButtons.svelte';
	import Name from '../../components/coin/Name.svelte';
	import Basics from '../../components/coin/Basics.svelte';
	import Description from '../../components/coin/Description.svelte';
	import Info from '../../components/coin/Info.svelte';
	import LastBlocks from '../../components/coin/LastBlocks.svelte';
	import Exchange from '../../components/coin/Exchange.svelte';
	import News from '../../components/coin/News.svelte';
	import Tools from '../../components/coin/Tools.svelte';
	import Specifications from '../../components/coin/Specifications.svelte';
	export async function load({ page, fetch, session, context }) {
		const url = `https://enso.okno.rs/coins/${page.params.slug}`;
		const res = await fetch(url);

		if (res.ok) {
			return {
				props: {
					coin: await res.json()
				}
			};
		}

		return {
			status: res.status,
			error: new Error(`Could not load ${url}`)
		};
	}
</script>
<script>
	export let coin;
	export let page;

</script>



<Header slug={coin.slug} name={coin.name} />


<amp-state id="coin" src="https://enso.okno.rs/coins/{ coin.slug }"></amp-state>




<amp-font layout="nodisplay"
		  font-family="bariolregular"
		  timeout="2000"
		  on-error-remove-class="bariolregular-loading"
		  on-error-add-class="plan9regular-missing"
		  on-load-remove-class="bariolregular-loading"
		  on-load-add-class="bariolregular-loaded">
</amp-font>
<amp-font layout="nodisplay"
		  font-family="plan9regular"
		  timeout="2000"
		  on-error-remove-class="plan9regular-loading"
		  on-error-add-class="plan9regular-missing"
		  on-load-remove-class="plan9regular-loading"
		  on-load-add-class="plan9regular-loaded">
</amp-font>

<div class="container mx-auto mb-8 px-4 px-0 flex flex-col flex-1 content main-wrap">
	<div class="flex flex-col py-12"><Name /></div>
	<div class="grid grid-cols-6 gap-5">
		<div class="col-span-full md:col-span-4 lg:col-span-4 grid grid-cols-3 gap-5">
			<Panel class="col-span-2"><Basics name={coin.name} /></Panel>
			<Panel class="col-span-1"><Specifications name={coin.name}/></Panel>
			<Panel class="col-span-3"><Description name={coin.name}/></Panel>
			<Panel class="col-span-3"><Info /></Panel>
			<Panel class="col-span-3"><LastBlocks name={coin.name} slug={coin.slug}/></Panel>
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

<Footer />
