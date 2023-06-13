<script>
    import {browser} from "$app/environment";
    // function to check if the user is on a mobile device
    let isMobileDevice = false;

    function checkIfMobileDevice() {
        if (browser) {
            // check if the user is on a mobile device
            const width = window.screen.width;
            const height = window.screen.height;
            // check if the screen size is less than 1024px
             return width < 1024 || height < 1024;
        }
    }

    $: isMobileDevice = checkIfMobileDevice();

</script>

{#if isMobileDevice}
    <svg fill="#000000" viewBox="0 0 24 24" class="animate-bounce"
         xmlns="http://www.w3.org/2000/svg">
        <g>
            <circle id="primary" class="fill-violet-700" cx="12" cy="12" r="10"></circle>
            <path id="secondary" class="fill-white"
                  d="M14.14,13H13V7a1,1,0,0,0-2,0v6H9.86a1,1,0,0,0-.69,1.5l2.14,3.12a.82.82,0,0,0,1.38,0l2.14-3.12A1,1,0,0,0,14.14,13Z"></path>
        </g>
    </svg>
{:else}
    <div class="flex flex-col items-center">
        <svg class="hoverable w-16 xl:w-24" xmlns="http://www.w3.org/2000/svg" viewBox="210 474.208 122.76 79.794">
            <g transform="matrix(0.05115, 0, 0, -0.05115, 156.292099, 783.665161)" stroke="none" style="">
                <path id="up" class="fill-white"
                      d="M1920 6030 c-19 -19 -20 -33 -20 -335 0 -302 1 -316 20 -335 19 -19 33 -20 330 -20 297 0 311 1 330 20 19 19 20 33 20 335 0 302 -1 316 -20 335 -19 19 -33 20 -330 20 -297 0 -311 -1 -330 -20z m540 -335 l0 -215 -210 0 -210 0 0 215 0 215 210 0 210 0 0 -215z"/>
                <path id="left" class="fill-white"
                      d="M1070 5180 c-19 -19 -20 -33 -20 -335 0 -302 1 -316 20 -335 19 -19 33 -20 330 -20 297 0 311 1 330 20 19 19 20 33 20 335 0 302 -1 316 -20 335 -19 19 -33 20 -330 20 -297 0 -311 -1 -330 -20z m540 -335 l0 -215 -210 0 -210 0 0 215 0 215 210 0 210 0 0 -215z"/>
                <path id="down" class="fill-violet-400 animate-pulse"
                      d="M1920 5180 c-19 -19 -20 -33 -20 -335 0 -302 1 -316 20 -335 19 -19 33 -20 330 -20 297 0 311 1 330 20 19 19 20 33 20 335 0 302 -1 316 -20 335 -19 19 -33 20 -330 20 -297 0 -311 -1 -330 -20z m540 -335 l0 -215 -210 0 -210 0 0 215 0 215 210 0 210 0 0 -215z"/>
                <path id="right" class="fill-white"
                      d="M2770 5180 c-19 -19 -20 -33 -20 -335 0 -302 1 -316 20 -335 19 -19 33 -20 330 -20 297 0 311 1 330 20 19 19 20 33 20 335 0 302 -1 316 -20 335 -19 19 -33 20 -330 20 -297 0 -311 -1 -330 -20z m540 -335 l0 -215 -210 0 -210 0 0 215 0 215 210 0 210 0 0 -215z"/>
            </g>
        </svg>

        <p class="animate-pulse pt-2 text-sm font-semibold text-violet-400">Use arrow keys to navigate</p>
    </div>
{/if}