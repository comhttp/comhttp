<script context="module">
    let topLevelDomain;
    let slug;
    let sub;

    import "$lib/styles/tailwind-output.css";
    import Sidebar from '$lib/components/Sidebar.svelte';
    import Bg from '$lib/helpers/Bg.svelte';


    /**
     * @type {import('@sveltejs/kit').Load}
     */
    export async function load({ page, fetch, session, context }) {
        let slugs = ""
        let hostPort = page.host.split(":")
        let host = hostPort[0].split(".")
        if (page.params.parts) {
            slugs = page.params.parts.split("/");
        }
        if (host.length > 2) {
            topLevelDomain= host[2]
            slug =  host[0]
            sub =  'sub'
        }else{
            topLevelDomain= host[1]
            slug =  host[0]
            sub =  host[1]
        }


        // let path = '../lib/tld/us/us.svelte'
// let path = '../lib/tld/' + tld + '/' + sub + '.svelte'
//         import(path.toString()).then(res => (COMponent = res.default));
        return {
            // props: {
            //     tld:topLevelDomain,
            //     slug:slug,
            //     sub:sub,
            // }
        };
    }
</script>

<script>

import {setContext} from "svelte";

setContext('tld', topLevelDomain);
setContext('slug', slug);
setContext('sub', sub);




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
</svelte:head>

    <slot></slot>

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
