    <div class="flex-1 flex flex-col container mx-auto px-4 px-0 main-wrap">
        <amp-list layout="fixed-height" width="auto" height="300" src="https://enso.okno.rs/info/node" items="c" reset-on-refresh
                  binding="no">
            <template type="amp-mustache">
                <button class="relative inline-flex coin" on="tap:AMP.navigateTo(url='https://{`{{.}}`}.com-http.us')">
                    <amp-img layout="fixed" width="72" height="72" alt="{`{{.}}`}"
                             src="https://enso.okno.rs/logo/{`{{.}}`}/128"></amp-img>
                    <div class="reflection"></div>
                </button>

            </template>
        </amp-list>
    </div>
