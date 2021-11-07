<script>
    import PanelTitle from '$lib/helpers/PanelTitle.svelte';
    export let slug;
    export let vars;
</script>

<svelte:head>
    <script async custom-element="amp-render" src="https://cdn.ampproject.org/v0/amp-render-1.0.js"></script>
	<link rel="preload" href="https://enso.okno.rs/explorer/parallelcoin/block/{vars}" as="fetch">
</svelte:head>




<amp-state id="block" src="https://enso.okno.rs/explorer/parallelcoin/block/{vars}"></amp-state>





<amp-render src="amp-state:block" layout="flex-item" class="cgl">
    <template type="amp-mustache">
            <section class="flex-1 flex flex-col mx-auto px-4 px-0 main-wrap">
                    <header class="flex flex-col">
                            <h1 class="my-8 flex flex-col xl:flex-row justify-between items-center heading-shadow-invert text-light whitespace-nowrap overflow-ellipsis overflow-hidden" title="ParallelCoin Block">
                            <strong class="text-4xl sm:text-5xl md:text-6xl xl:text-7xl xl:text-8xl"> Block</strong><span class="text-xl md:text-2xl xl:text-3xl xl:text-5xl">` + {slug} + `</span></h1>
                        </header>
                    <article class="w-full flex flex-col rounded md:rounded-lg bg-dark text-xl text-light mx-auto p-8 main-wrap">
                               <div class="grid grid-cols-5 gap-0 divide-y-2 divide-black divide-dotted divide-opacity-20">
                                        {`{{#blockhash}}`}<div class="font-bold tracking-wide py-2">Block hash</div><div class="col-span-4 value py-2 whitespace-nowrap overflow-ellipsis overflow-hidden"><a class="no-underline hover:no-underline text-green_blue hover:text-orange" href="/block/{`{{blockhash}}`}">{`{{blockhash}}`}</a></div>{`{{/blockhash}}`}
                                        {`{{#hash}}`}<div class="font-bold tracking-wide py-2">Hash</div><div class="col-span-4 value py-2 whitespace-nowrap overflow-ellipsis overflow-hidden">{`{{hash}}`}</div>{`{{/hash}}`}
                                            {`{{#previousblockhash}}`}<div class="font-bold py-2">Previous block Hash</div><div  class="col-span-4 value py-2 whitespace-nowrap overflow-ellipsis overflow-hidden"><a class="no-underline hover:no-underline text-green_blue hover:text-orange" href="/block/{`{{ previousblockhash }}`}">{`{{ previousblockhash }}`}</a></div>{`{{/previousblockhash}}`}
                                            {`{{#nextblockhash}}`}<div class="font-bold py-2">Next block Hash</div><div  class="col-span-4 value py-2 whitespace-nowrap overflow-ellipsis overflow-hidden"><a class="no-underline hover:no-underline text-green_blue hover:text-orange" href="/block/{`{{ nextblockhash }}`}">{`{{ nextblockhash }}`}</a></div>{`{{/nextblockhash}}`}
                                            {`{{#bits}}`}<div class="font-bold py-2">Bits</div><div  class="col-span-4 value py-2">{`{{bits}}`}</div>{`{{/bits}}`}
                                            {`{{#confirmations}}`}<div class="font-bold py-2">Confirmations</div><div  class="col-span-4 value py-2">{`{{confirmations}}`}</div>{`{{/confirmations}}`}
                                            {`{{#difficulty}}`}<div class="font-bold py-2">Difficulty</div><div class="col-span-4 value py-2">{`{{difficulty}}`}</div>{`{{/difficulty}}`}
                                            {`{{#merkleroot}}`}<div class="font-bold py-2">Merkle root</div><div class="col-span-4 value py-2 whitespace-nowrap overflow-ellipsis overflow-hidden">{`{{merkleroot}}`}</div>{`{{/merkleroot}}`}
                                            {`{{#nonce}}`}<div class="font-bold py-2">Nonce</div><div class="col-span-4 value py-2">{`{{nonce}}`}</div>{`{{/nonce}}`}
                                            {`{{#size}}`}<div class="font-bold py-2">Size</div><div  class="col-span-4 value py-2">{`{{size}}`}</div>{`{{/size}}`}
                                            {`{{#pow_algo}}`}<div class="font-bold py-2">POW algo</div><div  class="col-span-4 value py-2">{`{{pow_algo}}`}</div>{`{{/pow_algo}}`}
                                            {`{{#pow_hash}}`}<div class="font-bold py-2">Hash</div><div  class="col-span-4 value py-2 whitespace-nowrap overflow-ellipsis overflow-hidden">{`{{pow_hash}}`}</div>{`{{/pow_hash}}`}
                                            {`{{#pow_algo_id}}`}<div class="font-bold py-2">Hash</div><div  class="col-span-4 value py-2">{`{{pow_algo_id}}`}</div>{`{{/pow_algo_id}}`}
                                            {`{{#time}}`}<div class="font-bold py-2">Time</div><div class="col-span-4 value py-2">{`{{time}}`}</div>{`{{/time}}`}
                                            {`{{#timeutc}}`}<div class="font-bold py-2">Time UTC</div><div  class="col-span-4 value py-2">{`{{timeutc}}`}</div>{`{{/timeutc}}`}
                                            {`{{#version}}`}<div class="font-bold py-2">Version</div><div  class="col-span-4 value py-2">{`{{version}}`}</div>{`{{/version}}`}
                                            {`{{#tx}}`}<div class="font-bold py-2">Number of transactions</div><div class="col-span-4 value py-2">{`{{tx.length}}`}</div>{`{{/tx}}`}
                                            {`{{#tx}}`}<div class="font-bold py-2">Transactions</div>{`{{/tx}}`}
                                            <div class="col-span-4 value py-2">
                                            <div class="value flex flex-col my-4 p-6 bg-black bg-opacity-25 rounded-lg">
                                                {`{{#tx}}`}<a class="whitespace-nowrap overflow-ellipsis overflow-hidden no-underline hover:no-underline text-green_blue hover:text-orange" href="/tx/{`{{.}}`}">{`{{.}}`}</a>{`{{/tx}}`}
                                            </div>
                                        </div>
                               </div>
                                </article>
                    <footer class="flex space-between">
                            {`{{#previousblockhash}}`}<a class="flex-1 justify-center p-6 button blue text-2xl no-underline hover:no-underline title text-green_blue hover:text-orange" href="/block/{`{{previousblockhash}}`}"><i class="fas fa-angle-left mr-2"></i>Previous block</a>{`{{/previousblockhash}}`}
                            {`{{#nextblockhash}}`}<a class="flex-1 justify-center p-6 button blue text-2xl no-underline hover:no-underline text-green_blue hover:text-orange" href="/block/{`{{nextblockhash}}`}">Next block<i class="fas fa-angle-right mr-2"></i></a>{`{{/nextblockhash}}`}
                        </footer>
                </section>
        </template>
</amp-render>