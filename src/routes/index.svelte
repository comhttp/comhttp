<script context="module">
    import "$lib/styles/tailwind-output.css";
    let COMponent;
</script>
<script>
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';

    import { getContext } from 'svelte';
    const tld = getContext('tld');
    const slug = getContext('slug');
    const sub = getContext('sub');
    let path = '../lib/tld/' + tld + '/' + sub + '.svelte'
    import(path.toString()).then(res => (COMponent = res.default));
</script>
<!--{tld}-->
<!--{slug}-->
<!--{sub}-->

<svelte:component this={COMponent}></svelte:component>

