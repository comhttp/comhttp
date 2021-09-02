    <div class="flex-1 flex flex-col container mx-auto px-4 px-0 main-wrap">
        <amp-list layout="flex-item" src="https://enso.okno.rs/info/node" single-item items="c" reset-on-refresh
                  binding="no">
            <template type="amp-mustache">

                <button class="relative inline-flex coin" on="tap:AMP.navigateTo(url='/coin/{`{{.}}`}')">
                    <amp-img layout="fixed" width="72" height="72" alt="{`{{.}}`}"
                             src="https://img.okno.rs/coins/128/{`{{.}}`}128.png"></amp-img>
                    <div class="reflection"></div>
                </button>

            </template>
        </amp-list>
    </div>
