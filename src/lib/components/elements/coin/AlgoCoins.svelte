

<svelte:head>
  <link rel="preload" href="https://enso.okno.rs/json/algo" as="fetch">

</svelte:head>




{@html `<amp-state id="algocoins" src="https://enso.okno.rs/json/algo"></amp-state>`}

<div class="flex-1 flex flex-col container mx-auto px-4 px-0 main-wrap">





{@html `<amp-state id="allCoins" src="https://enso.okno.rs/json/algo"></amp-state>

<amp-list src="amp-state:algocoins" height="60" single-item items=".">
  <template type="amp-mustache">
    <select on="change:AMP.setState({
    filteredCoins: allCoins.c.filter(a => event.value == 'all' ? true : a.a == event.value)
  })">
  <option value="all" selected>All</option>
    {{#a}}     
  <option value="{{.}}">{{.}}</option>
        {{/a}}
      </select>
  </template>
</amp-list>`}



        

        {@html `<amp-list layout="flex-item" src="amp-state:algocoins" [src]="filteredCoins"  items="c"  binding="no">
            
            <template type="amp-mustache">
                <button class="relative inline-flex coin" on="tap:AMP.navigateTo(url='https://{{s}}.com-http.us')">
                  <svg width="16" height="16" xmlns="http://www.w3.org/2000/svg"><image href="{{l}}" height="16" width="16" /></svg>
                </button>



            </template>
        </amp-list>`}
    </div>
