<script>
    import ArrowKeys from "$lib/components/ArrowKeys.svelte";
    import AboutDesc from "$lib/components/AboutDesc.svelte";

</script>


<div class="flex h-full w-full flex-col items-center justify-between border rounded-md bg-gradient-to-tr from-stone-950 via-violet-950 to-stone-950 pt-24 text-white xl:flex-row xl:justify-center xl:p-2">
    <div class="bg"></div>
    <div class="flex flex-col justify-between gap-10">
        <h1 class="glitch pb-5 text-center text-xl font-semibold uppercase xl:text-6xl hoverable"
            data-text="&lt;Mukil Chittybabu/&gt;">&lt;Mukil Chittybabu/&gt;</h1>
        <div class="order-last xl:order-none hoverable">
            <AboutDesc/>
        </div>
        <p class="bottom-11 right-12 flex justify-center xl:absolute hoverable">Based in Melbourne</p>
    </div>
    <div class="bottom-10 left-10 flex justify-center xl:absolute">
        <div class="flex flex-col items-center justify-center p-2">
            <ArrowKeys/>
        </div>
    </div>
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

    h1 {
        padding: 0;
        margin: 0;
        font-family: sans-serif;
    }

    .glitch {
        position: relative;
        color: #fff;
        letter-spacing: 0.5em;
        animation: glitch-skew 5s infinite linear alternate-reverse;
    }

    .glitch::before {
        content: attr(data-text);
        position: absolute;
        top: 0;
        width: 100%;
        height: 100%;
        left: 2px;
        text-shadow: -2px 0 #3a0232;
        clip: rect(44px, 450px, 56px, 0);
        animation: glitch-anim 5s infinite linear alternate-reverse;
    }

    .glitch::after {
        content: attr(data-text);
        position: absolute;
        top: 0;
        width: 100%;
        height: 100%;
        left: -2px;
        text-shadow: -2px 0 #9d51ff, 2px 2px #7300ff;
        clip: rect(44px, 450px, 56px, 0);
        animation: glitch-anim2 5s infinite linear alternate-reverse;
    }

    @keyframes glitch-anim {
        0% {
            clip: rect(1px, 9999px, 47px, 0);
            transform: skew(0.75deg);
        }
        5% {
            clip: rect(68px, 9999px, 100px, 0);
            transform: skew(0.77deg);
        }
        10% {
            clip: rect(93px, 9999px, 38px, 0);
            transform: skew(0.79deg);
        }
        15% {
            clip: rect(53px, 9999px, 97px, 0);
            transform: skew(0.15deg);
        }
        20% {
            clip: rect(47px, 9999px, 65px, 0);
            transform: skew(0.37deg);
        }
        25% {
            clip: rect(84px, 9999px, 51px, 0);
            transform: skew(0.64deg);
        }
        30% {
            clip: rect(58px, 9999px, 38px, 0);
            transform: skew(0.14deg);
        }
        35% {
            clip: rect(36px, 9999px, 48px, 0);
            transform: skew(0.73deg);
        }
        40% {
            clip: rect(26px, 9999px, 3px, 0);
            transform: skew(0.24deg);
        }
        45% {
            clip: rect(11px, 9999px, 79px, 0);
            transform: skew(0.25deg);
        }
        50% {
            clip: rect(38px, 9999px, 9px, 0);
            transform: skew(0.95deg);
        }
        55% {
            clip: rect(6px, 9999px, 57px, 0);
            transform: skew(0.31deg);
        }
        60% {
            clip: rect(11px, 9999px, 91px, 0);
            transform: skew(0.5deg);
        }
        65% {
            clip: rect(99px, 9999px, 45px, 0);
            transform: skew(0.62deg);
        }
        70% {
            clip: rect(40px, 9999px, 28px, 0);
            transform: skew(0.14deg);
        }
        75% {
            clip: rect(77px, 9999px, 30px, 0);
            transform: skew(0.89deg);
        }
        80% {
            clip: rect(48px, 9999px, 27px, 0);
            transform: skew(0.63deg);
        }
        85% {
            clip: rect(37px, 9999px, 96px, 0);
            transform: skew(0.32deg);
        }
        90% {
            clip: rect(18px, 9999px, 47px, 0);
            transform: skew(0.47deg);
        }
        95% {
            clip: rect(1px, 9999px, 42px, 0);
            transform: skew(0.97deg);
        }
    }

    @keyframes glitch-anim2 {
        0% {
            clip: rect(23px, 9999px, 81px, 0);
            transform: skew(0.76deg);
        }
        5% {
            clip: rect(24px, 9999px, 14px, 0);
            transform: skew(0.07deg);
        }
        10% {
            clip: rect(54px, 9999px, 38px, 0);
            transform: skew(0.26deg);
        }
        15% {
            clip: rect(30px, 9999px, 61px, 0);
            transform: skew(0.7deg);
        }
        20% {
            clip: rect(24px, 9999px, 51px, 0);
            transform: skew(0.7deg);
        }
        25% {
            clip: rect(15px, 9999px, 21px, 0);
            transform: skew(0.18deg);
        }
        30% {
            clip: rect(60px, 9999px, 50px, 0);
            transform: skew(0.01deg);
        }
        35% {
            clip: rect(82px, 9999px, 96px, 0);
            transform: skew(0.47deg);
        }
        40% {
            clip: rect(41px, 9999px, 32px, 0);
            transform: skew(0.49deg);
        }
        45% {
            clip: rect(22px, 9999px, 61px, 0);
            transform: skew(0.78deg);
        }
        50% {
            clip: rect(87px, 9999px, 91px, 0);
            transform: skew(0.25deg);
        }
        55% {
            clip: rect(60px, 9999px, 48px, 0);
            transform: skew(0.27deg);
        }
        60% {
            clip: rect(19px, 9999px, 90px, 0);
            transform: skew(0.92deg);
        }
        65% {
            clip: rect(72px, 9999px, 72px, 0);
            transform: skew(0.24deg);
        }
        70% {
            clip: rect(95px, 9999px, 67px, 0);
            transform: skew(0.89deg);
        }
        75% {
            clip: rect(66px, 9999px, 15px, 0);
            transform: skew(0.3deg);
        }
        80% {
            clip: rect(83px, 9999px, 10px, 0);
            transform: skew(0.34deg);
        }
        85% {
            clip: rect(19px, 9999px, 78px, 0);
            transform: skew(0.18deg);
        }
        90% {
            clip: rect(89px, 9999px, 76px, 0);
            transform: skew(0.23deg);
        }
        95% {
            clip: rect(32px, 9999px, 28px, 0);
            transform: skew(0.77deg);
        }
    }

    @keyframes glitch-skew {
        0% {
            transform: skew(-4deg);
        }
        10% {
            transform: skew(1deg);
        }
        20% {
            transform: skew(3deg);
        }
        30% {
            transform: skew(-1deg);
        }
        40% {
            transform: skew(-4deg);
        }
        50% {
            transform: skew(2deg);
        }
        60% {
            transform: skew(1deg);
        }
        70% {
            transform: skew(0deg);
        }
        80% {
            transform: skew(-4deg);
        }
        90% {
            transform: skew(0deg);
        }
    }


</style>