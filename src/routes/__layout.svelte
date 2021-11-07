<script context="module">

    import Sidebar from '$lib/components/Sidebar.svelte';
    import Bg from '$lib/helpers/Bg.svelte';
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';
    import "../styles/tailwind-output.css";






    let tld;
    let slug;
    let sub;
    let type;
    let vars;

    import SubDirectory from '$lib/tld/directory/directory.svelte';
    import SubDownload from '$lib/tld/download/download.svelte';
    import SubExchange from '$lib/tld/exchange/exchange.svelte';
    import SubGames from '$lib/tld/games/games.svelte';
    import SubHelp from '$lib/tld/help/help.svelte';
    import SubInfo from '$lib/tld/info/info.svelte';
    import SubLink from '$lib/tld/link/link.svelte';
    import SubLive from '$lib/tld/live/live.svelte';
    import SubNet from '$lib/tld/net/net.svelte';
    import SubNetwork from '$lib/tld/network/network.svelte';
    import SubNews from '$lib/tld/news/news.svelte';
    import SubOrg from '$lib/tld/org/org.svelte';
    import SubSocial from '$lib/tld/social/social.svelte';
    import SubSupport from '$lib/tld/support/support.svelte';
    import SubToday from '$lib/tld/today/today.svelte';
    import SubTools from '$lib/tld/tools/tools.svelte';
    import SubToolsSub from '$lib/tld/tools/sub.svelte';
    import SubToolsBlock from '$lib/tld/tools/block.svelte';
    import SubToolsTx from '$lib/tld/tools/tx.svelte';
    import SubToolsAddr from '$lib/tld/tools/addr.svelte';
    import SubTrade from '$lib/tld/trade/trade.svelte';
    import SubUndefined from '$lib/tld/undefined/undefined.svelte';
    import SubUs from '$lib/tld/us/us.svelte';
    import SubUsSub from '$lib/tld/us/sub.svelte';

    /**
     * @type {import('@sveltejs/kit').Load}
     */
    export async function load({ page, fetch, session, context }) {
        let hostPort = page.host.split(":")
        let host = hostPort[0].split(".")
        if (page.params.parts) {
            type = page.params.parts.split("/")[0];
            vars = page.params.parts.split("/")[1];
        }
        if (host.length > 2) {
            tld = host[2]
            slug =  host[0]
            sub =  'sub'
        }else{
            tld= host[1]
            slug =  host[0]
            sub =  host[1]
        }
        return {
            props: {
                tld:tld,
                slug:slug,
                sub:sub,
                type:type,
                vars:vars,
            }
        };
    }
</script>

<script>




</script>

<svelte:head>
    <script async custom-element="amp-list" src="https://cdn.ampproject.org/v0/amp-list-0.1.js"></script>
    <script async custom-element="amp-lightbox" src="https://cdn.ampproject.org/v0/amp-lightbox-1.0.js"></script>

    <script async custom-template="amp-mustache" src="https://cdn.ampproject.org/v0/amp-mustache-0.2.js"></script>
    <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
    <script async custom-element="amp-sidebar" src="https://cdn.ampproject.org/v0/amp-sidebar-0.1.js"></script>
    <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
    <script async custom-element="amp-iframe" src="https://cdn.ampproject.org/v0/amp-iframe-0.1.js"></script>
    <script async custom-element="amp-font" src="https://cdn.ampproject.org/v0/amp-font-0.1.js"></script>
    <script async custom-element="amp-selector" src="https://cdn.ampproject.org/v0/amp-selector-0.1.js"></script>

	<link rel="preload" href="https://font.okno.rs/bariol/regular.woff2" as="font" type="font/woff2" crossorigin>
    <link rel="preload" href="https://font.okno.rs/bariol/regular.woff" as="font" type="font/woff" crossorigin>
    <link rel="preload" href="https://font.okno.rs/bariol/regular.ttf" as="font" type="font/ttf" crossorigin>
    <link rel="preload" href="https://font.okno.rs/splendid/regular.woff2" as="font" type="font/woff2" crossorigin>
    <link rel="preload" href="https://font.okno.rs/splendid/regular.woff" as="font" type="font/woff" crossorigin>
    <link rel="preload" href="https://font.okno.rs/splendid/regular.ttf" as="font" type="font/ttf" crossorigin>
    <link rel="preload" href="https://font.okno.rs/lucida/console.woff2" as="font" type="font/woff2" crossorigin>
    <link rel="preload" href="https://font.okno.rs/lucida/console.woff" as="font" type="font/woff" crossorigin>
    <link rel="preload" href="https://font.okno.rs/lucida/console.ttf" as="font" type="font/ttf" crossorigin>
    
</svelte:head>

{tld} -1- 
{slug} -2- 
{sub} -3- 
{type} -4- 
{vars} -5- 

<Sidebar></Sidebar>
<main class="main min-h-screen flex flex-col justify-between bg-gray-800 bg-opacity-20 font-text antialiased sm:text-md md:text-lg lg:text-lg xl:text-xl">
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
    <Bg slug={slug} name="name"></Bg>
    <Header slug={slug} name={slug}></Header>
    
    

<!-- 
{#if tld === "undefined"}
<SubUndefined></SubUndefined>
{/if}
 -->

{#if tld === "directory"}
<SubDirectory></SubDirectory>
{/if}
{#if tld === "download"}
<SubDownload></SubDownload>
{/if}
{#if tld === "exchange"}
<SubExchange></SubExchange>
{/if}
{#if tld === "games"}
<SubGames></SubGames>
{/if}
{#if tld === "help"}
<SubHelp></SubHelp>
{/if}
{#if tld === "info"}
<SubInfo></SubInfo>
{/if}
{#if tld === "link"}
<SubLink></SubLink>
{/if}
{#if tld === "live"}
<SubLive></SubLive>
{/if}
{#if tld === "net"}
<SubNet></SubNet>
{/if}
{#if tld === "network"}
<SubNetwork></SubNetwork>
{/if}
{#if tld === "news"}
<SubNews></SubNews>
{/if}
{#if tld === "org"}
<SubOrg></SubOrg>
{/if}
{#if tld === "social"}
<SubSocial></SubSocial>
{/if}
{#if tld === "support"}
<SubSupport></SubSupport>
{/if}
{#if tld === "today"}
<SubToday></SubToday>
{/if}
{#if tld === "tools"}
    {#if sub === "sub"}
        {#if type === "block"}
        <SubToolsBlock slug={slug} vars={vars}></SubToolsBlock>
        {:else if type === "tx"}
        <SubToolsTx slug={slug} vars={vars}></SubToolsTx>
        {:else if type === "addr"}
        <SubToolsAddr slug={slug} vars={vars}></SubToolsAddr>
        {:else}
        <SubToolsSub slug={slug}></SubToolsSub>
        {/if}
    {:else}
    <SubTools></SubTools>
    {/if}
{/if}
{#if tld === "trade"}
<SubTrade></SubTrade>
{/if}
{#if tld === "us"}
    {#if sub === "sub"}
    <SubUsSub slug={slug}></SubUsSub>
    {:else}
    <SubUs></SubUs>
    {/if}
{/if}


    <Footer></Footer>
</main>




<style>
    :global(.light){

    }
    :global(.dark) {

    }
    @font-face {
        font-family: 'bariolregular';
        src: local('bariolregular'), url('https://font.okno.rs/bariol/regular.woff2') format('woff2'), url('https://font.okno.rs/bariol/regular.woff') format('woff'), url('https://font.okno.rs/bariol/regular.ttf') format('truetype');

        font-weight: normal;
        font-style: normal;
    }
    @font-face {
        font-family: 'splendid';
        font-style: normal;
        font-display: swap;
        font-weight: 400;
        src: local('splendid'), url('https://font.okno.rs/splendid/regular.woff2') format('woff2'),url('https://font.okno.rs/splendid/regular.woff') format('woff'),url('https://font.okno.rs/splendid/regular.ttf') format('truetype');

    }
    @font-face {
        font-family: 'lucidaconsole';
        font-style: normal;
        font-display: swap;
        font-weight: 400;
        src: local('lucidaconsole'), url('https://font.okno.rs/lucida/console.woff2') format('woff2'),url('https://font.okno.rs/lucida/console.woff') format('woff'),url('https://font.okno.rs/lucida/console.ttf') format('truetype');

    }

</style>
