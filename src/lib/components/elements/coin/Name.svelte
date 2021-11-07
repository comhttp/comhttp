<amp-list id="coin-name" layout="fixed-height" height="128" width="auto" src="amp-state:coin" items= "." single-item class="m1">
<template type="amp-mustache" id="coin-name">
            <div class="flex items-center">
            <amp-img src="https://enso.okno.rs/logo/{`{{slug}}`}/128" alt="{`{{name}}`}"  width="128px" height="128px" layout="fixed"  class="nic"><noscript><img src="https://enso.okno.rs/coins/{`{{slug}}`}/128" width="128" height="128" alt="{`{{name}}`}"></noscript></amp-img>
            <h1 class="sm:text-5xl md:text-6xl lg:text-8xl xl:text-9xl text-primary heading-shadow-invert whitespace-nowrap overflow-ellipsis overflow-hidden truncate flex-1 ml-8">{`{{name}}`}</h1></div>
</template>
</amp-list>
