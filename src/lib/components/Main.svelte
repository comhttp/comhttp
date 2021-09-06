<script>
    import Sidebar from '$lib/components/Sidebar.svelte';
    import Bg from '$lib/helpers/Bg.svelte';

    export let slug;

</script>




<Sidebar />
<main class="main min-h-screen flex flex-col justify-between bg-gray-800 bg-opacity-20 font-text antialiased sm:text-md md:text-lg lg:text-lg xl:text-xl">
    <Bg slug={slug} name=name />
    <slot name="header"></slot>
    <slot></slot>
    <slot name="footer"></slot>
</main>
