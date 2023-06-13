<script>
</script>



<div class="flex justify-center items-center text-white mx-3 xl:mx-10 border border-white w-full h-5/6">
    <div class="bg"></div>
    <h1 class="text-2xl xl:text-8xl font-semibold uppercase text-center"> &lt;Mukil Chittybabu/&gt;</h1>
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
        background: transparent url('http://assets.iceable.com/img/noise-transparent.png') repeat 0 0;
        background-repeat: repeat;
        animation: bg-animation .2s infinite;
        opacity: .9;
        visibility: visible;
    }

    @keyframes bg-animation {
        0% { transform: translate(0,0) }
        10% { transform: translate(-5%,-5%) }
        20% { transform: translate(-10%,5%) }
        30% { transform: translate(5%,-10%) }
        40% { transform: translate(-5%,15%) }
        50% { transform: translate(-10%,5%) }
        60% { transform: translate(15%,0) }
        70% { transform: translate(0,10%) }
        80% { transform: translate(-15%,0) }
        90% { transform: translate(10%,5%) }
        100% { transform: translate(5%,0) }
    }
</style>