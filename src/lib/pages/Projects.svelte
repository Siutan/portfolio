<script>

</script>


<div class="flex h-full w-full flex-col items-center justify-between border rounded-md bg-gradient-to-tr from-stone-950 via-rose-950 to-stone-950 pt-24 text-white xl:flex-row xl:justify-center xl:p-2">
    <div class="bg"></div>

</div>

<style>

    .bg {
        position: absolute;
        top: -50%;
        left: -50%;
        right: -50%;
        bottom: -50%;
        width: 200%;
        height: 200vh;
        background: transparent url('noise-transparent.png') repeat 0 0;
        animation: bg-animation .2s infinite;
        opacity: 100%;
        filter: brightness(1.2);
        visibility: visible;
    }

    @keyframes bg-animation {
        0% {
            transform: translate(0, 0)
        }
        10% {
            transform: translate(-5%, -5%)
        }
        20% {
            transform: translate(-10%, 5%)
        }
        30% {
            transform: translate(5%, -10%)
        }
        40% {
            transform: translate(-5%, 15%)
        }
        50% {
            transform: translate(-10%, 5%)
        }
        60% {
            transform: translate(15%, 0)
        }
        70% {
            transform: translate(0, 10%)
        }
        80% {
            transform: translate(-15%, 0)
        }
        90% {
            transform: translate(10%, 5%)
        }
        100% {
            transform: translate(5%, 0)
        }
    }


</style>