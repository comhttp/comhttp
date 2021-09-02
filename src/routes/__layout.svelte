<script>
    import "../styles/tailwind-output.css";

    import Sidebar from '../components/Sidebar.svelte';
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

<Sidebar />
<main class="main min-h-screen flex flex-col justify-between bg-gray-800 bg-opacity-20 font-text antialiased sm:text-md md:text-lg lg:text-lg xl:text-xl">
    <slot></slot>
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
