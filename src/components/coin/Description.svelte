<script>
    import PanelTitle from '../../components/helpers/PanelTitle.svelte';
    export let name;
</script>
<amp-list id="coin-desc" layout="responsive" height="80" width="320" src="amp-state:coin" items= "." single-item class="m1">
    <template type="amp-mustache"  id="coin-desc">
        <div class="flex flex-col">
            <PanelTitle name={name} title="Description" icon="scroll" />
            <div class="flex flex-col flex-1 p-6 text-xl">
                {`{{{description}}}`}</div>
        </div>
</template></amp-list>
