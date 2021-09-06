<script>
    import Icon from '$lib/helpers/Icon.svelte';
    import BigScreenOnly from '$lib/helpers/BigScreenOnly.svelte';
    import Aria from '$lib/helpers/Aria.svelte';

    let currentTheme = "light";

    export let slug;
    export let name;
</script>

<header class="header bg-gray-800 text-gray-50">
        <div class="flex justify-between m-1 menu-wrap">
            <button class="p-1 cursor-pointer menulogo sidelogo" on="tap:drawermenu.toggle">


                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 64 64" width="24" height="24">
                    <g><g><g><g>
                        <path class="alogo svgpa logocolors" d="M0 36.35L0 25.75L57.11 25.75C59.08 25.75 60.72 26.45 62.03 27.85C63.35 29.24 64 30.92 64 32.89L64 36.35L0 36.35L0 36.35Z" /></g><g>
                        <path class="alogo svgpa logocolors" d="M0 15.45L0 4.84L57.11 4.84C59.08 4.84 60.72 5.54 62.03 6.93C63.35 8.33 64 10.02 64 11.99L64 15.44L0 15.44L0 15.45Z" /></g><g>
                        <path class="alogo svgpa logocolors" d="M0 57.24L0 46.63L57.11 46.63C59.08 46.63 60.72 47.33 62.03 48.73C63.35 50.13 64 51.81 64 53.79L64 57.24L0 57.24L0 57.24Z" />
                    </g></g></g></g></svg>


            </button>

            <div class="container mx-auto px-0 flex flex-1 justify-between">
                <a href="http://com-http.us" class="flex items-center menulogo">
                    <amp-img layout="fixed" width="32" height="32" src="https://img.okno.rs/coins/32/{slug}32.png" alt="navigation"></amp-img>
                    <span class="text-2xl ml-2">{name}</span>
                </a>
                <div>
                    <input name="search" type="search" placeholder="Search" value>
                    <input type="submit" value></div>
            </div>
            <div class="suggest">

            </div>


            <label class="theme">
                <Aria>{currentTheme} mode</Aria>
                <BigScreenOnly ariaHidden="true">DARK</BigScreenOnly>
                <input type="checkbox" checked={currentTheme !== "DARK"} on:click={toggleTheme} />
                <span class="toggle">
    <span class="toggleIcons">
      <Icon name="moon" />
      <Icon name="sun" />
    </span>
  </span>
                <BigScreenOnly ariaHidden="true">LIGHT</BigScreenOnly>
            </label>


        </div>
    </header>

<style>
    label {
        display: flex;
        align-items: center;
        padding: 0;

        background: transparent;
        border: none;
        box-sizing: border-box;

        font-family: var(--monospace);
        font-size: 0.75rem;
        letter-spacing: 0.05em;
        text-transform: uppercase;
        color: var(--dark_blue);

        --toggle-height: 20px;
    }

    @media all and (min-width: 900px) {
        label {
            margin: 0;
            --toggle-height: 15px;
        }
    }

    input {
        position: absolute;
        width: 0;
        height: 0;
        opacity: 0;
        overflow: hidden;
    }

    .toggle {
        position: relative;
        display: inline-block;
        width: calc(var(--toggle-height) * 2);
        height: var(--toggle-height);
        margin: 0 0.5em;

        background: var(--green_blue_light);
        color: var(--green_blue_light);

        border-radius: var(--toggle-height);
        cursor: pointer;
    }

    .toggle::after {
        position: absolute;
        top: 1px;
        left: 1px;
        width: calc(var(--toggle-height) - 2px);
        height: calc(var(--toggle-height) - 2px);

        background: var(--light_gray);
        box-shadow: 1px 2px 3px 0 rgba(0, 0, 0, 0.2);

        border-radius: var(--toggle-height);
        content: '';
        transition: all 0.25s cubic-bezier(0.19, 1, 0.22, 1);
    }

    input:checked ~ .toggle:after {
        left: calc(var(--toggle-height) + 1px);
        background: var(--gray);
    }

    .toggleIcons {
        position: absolute;
        top: 2px;
        left: 4px;
        width: calc(100% - 7px);
        height: calc(100% - 6px);
        z-index: 1;

        display: flex;
        justify-content: space-between;

        font-size: 14px;
        pointer-events: none;
    }

    @media all and (min-width: 900px) {
        .toggleIcons {
            display: none;
        }

        label:focus-within .toggle {
            background: var(--light_blue);
        }
    }
</style>
