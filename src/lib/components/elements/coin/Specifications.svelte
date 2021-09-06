<script>
    import PanelTitle from '$lib/helpers/PanelTitle.svelte';
    export let name;
</script>
<amp-list id="coin-spec" layout="fixed-height" height="200" width="auto" src="amp-state:coin" items= "." single-item class="m1">
<template type="amp-mustache" id="coin-spec">
    <PanelTitle name={name} title="Specifications" icon="network-wired"/>

    <div class="grid grid-cols-3 gap-1 p-4">
{`{{#algo}}`}<span>Algorithm</span><span class="col-span-2">{`{{algo}}`}</span>{`{{/algo}}`}
{`{{#total}}`}<span>Total Coin Supply</span><span class="col-span-2">{`{{total}}`}</span>{`{{/total}}`}
{`{{#diff}}`}<span>Difficulty Adjustment</span><span class="col-span-2">{`{{diff}}`}</span>{`{{/diff}}`}
{`{{#rew}}`}<span>Block Reward Reduction</span><span class="col-span-2">{`{{rew}}`}</span>{`{{/rew}}`}
{`{{#proof}}`}<span>Proof Type</span><span class="col-span-2">{`{{proof}}`}</span>{`{{/proof}}`}
</div>
</template>
</amp-list>
