<script>
    import PanelTitle from '$lib/helpers/PanelTitle.svelte';
    export let name;
</script>

<svelte:head>
    <script async custom-element="amp-render" src="https://cdn.ampproject.org/v0/amp-render-1.0.js"></script>
</svelte:head>

<amp-render id="coin-desc" layout="flex-item" src="amp-state:coin" class="m1">
    <template type="amp-mustache"  id="coin-desc">
        <div class="flex flex-col">
            <PanelTitle name={name} title="Description" icon="scroll" />
            <div class="flex flex-col flex-1 p-6 text-xl">
                {`{{{description}}}`}</div>
        </div>
</template>
  </amp-render>