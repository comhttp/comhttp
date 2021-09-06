<script context="module">
	/**
	 * @type {import('@sveltejs/kit').Load}
	 */
	import Main from '$lib/components/Main.svelte';
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Panel from '$lib/helpers/Panel.svelte';
	import CoinButtons from '$lib/components/elements/coin/CoinButtons.svelte';
	import Name from '$lib/components/elements/coin/Name.svelte';
	import Basics from '$lib/components/elements/coin/Basics.svelte';
	import Description from '$lib/components/elements/coin/Description.svelte';
	import Info from '$lib/components/elements/coin/Info.svelte';
	import LastBlocks from '$lib/components/elements/coin/LastBlocks.svelte';
	import Exchange from '$lib/components/elements/coin/Exchange.svelte';
	import News from '$lib/components/elements/coin/News.svelte';
	import Tools from '$lib/components/elements/coin/Tools.svelte';
	import Specifications from '$lib/components/elements/coin/Specifications.svelte';




	export async function load({ page, fetch, session, context }) {
		const url = 'https://enso.okno.rs/coins/' + slug;
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
    import { getContext } from 'svelte';
    const tld = getContext('tld');
    const slug = getContext('slug');
    const sub = getContext('sub');

	export let coin;


</script>





<Main slug={slug}>



<svelte:fragment slot="header"><Header slug={slug} name={slug}></Header></svelte:fragment>

<!--{coin.slug}-->

<!--{slug}-->

<amp-state id="coin" src="https://enso.okno.rs/coins/{ slug }"></amp-state>




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
			<Panel class="col-span-2"><Basics name={slug} /></Panel>
			<Panel class="col-span-1"><Specifications name={slug}/></Panel>
			<Panel class="col-span-3"><Description name={slug}/></Panel>
			<Panel class="col-span-3"><Info /></Panel>
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


<svelte:fragment slot="footer"><Footer></Footer></svelte:fragment>
</Main>
