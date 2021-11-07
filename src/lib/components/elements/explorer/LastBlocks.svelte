<script>
    import PanelTitle from '$lib/helpers/PanelTitle.svelte';
    export let slug;
    export let name;
</script>

<amp-list id="coin-name" layout="fixed-height" height="390" width="auto" src="amp-state:blocks" items= "." single-item class="m1">
        <template type="amp-mustache" id="coin-name">
            <div class="flex-1 flex flex-col">
                <PanelTitle name={name} title="Last blocks" icon="network-wired" />
                <div class="flex flex-col px-4 font-mono text-sm">
            {`{{#blocks}}`}
<a href="https://{ slug }.com-http.tools/block/{`{{height}}`}" class="flex flex-row py-1 border-dotted border-dark border-t border-l-0 border-r-0 border-b-0 font-mono justify-between">
    <span class="mr-3">{`{{height}}`}</span>
    <span class="flex-1 truncate">{`{{hash}}`}</span>
    <span class="ml-2">{`{{time}}`}</span></a>
            {`{{/blocks}}`}
                </div>
            </div>
        </template>
    </amp-list>
