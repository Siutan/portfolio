<script>
    import "../app.css";
    import "$lib/components/Navbar.svelte";
    import Navbar from "$lib/components/Navbar.svelte";

    import {onMount} from 'svelte';
    import gsap from 'gsap';
    import {
        Fullpage,
        FullpageSection,
        FullpageSlide
    } from 'svelte-fullpage'


    onMount(() => {
        gsap.set(".ball", {xPercent: -50, yPercent: -50});
        gsap.set(".follow-ball", {xPercent: -50, yPercent: -50});

        let fxTo = gsap.quickTo(".follow-ball", "x", {duration: 0.4, ease: "power3"}),
            fyTo = gsap.quickTo(".follow-ball", "y", {duration: 0.4, ease: "power3"});

        let xTo = gsap.quickTo(".ball", "x", {duration: 0.01, ease: "power3"}),
            yTo = gsap.quickTo(".ball", "y", {duration: 0.01, ease: "power3"});

        window.addEventListener("mousemove", e => {
            // if not mobile
            if (window.innerWidth > 768) {
                // for the follow ball
                fxTo(e.clientX);
                fyTo(e.clientY);
                // for the ball
                xTo(e.clientX);
                yTo(e.clientY);
            }
        });

        document.documentElement.addEventListener("mouseleave", (event) => {
            if (event.clientY <= 0 || event.clientX <= 0 || (event.clientX >= window.innerWidth || event.clientY >= window.innerHeight)) {
                console.log("mouse left window")
                gsap.to(".follow-ball", {opacity: 0, duration: 0.3, ease: "power1.inOut"})
                gsap.to(".ball", {opacity: 0, duration: 0.3, ease: "power1.inOut"})
            }
        });

        document.documentElement.addEventListener("mouseenter", (event) => {
            console.log("mouse entered window")
            gsap.to(".follow-ball", {opacity: 1, duration: 0.3, ease: "power1.inOut"})
            gsap.to(".ball", {opacity: 1, duration: 0.3, ease: "power1.inOut"})
        });

        // if mouse over elements with the class of .hoverable, increase the size of the follow-ball and hide the ball
        let hover = gsap.to(".follow-ball", {scale: 2.6, duration: 0.3, paused: true, ease: "power1.inOut"})
        let hide = gsap.to(".ball", {opacity: 0, duration: 0.3, paused: true, ease: "power1.inOut"})

        document.querySelectorAll(".hoverable").forEach(hoverable => {
            hoverable.addEventListener("mouseenter", () => {
                hide.play()
                hover.play()
            });
            hoverable.addEventListener("mouseleave", () => {
                hide.reverse()
                hover.reverse()
            });
        });
    });

</script>

<body class="h-screen bg-black">
<Navbar/>
<!--<div class="main-div">-->
<!--    <slot/>-->
<div class="ball"></div>
<div class="follow-ball"></div>
<!--</div>-->

<div class="w-full h-full">
    <Fullpage>
        <FullpageSection title="Home">
            <slot/>
        </FullpageSection>
        <FullpageSection title="About">
            <FullpageSlide title="1982-1993">
                ...Your markup here
            </FullpageSlide>
            <FullpageSlide title="1993-2006">
                ...Your markup here
            </FullpageSlide>
            <FullpageSlide title="2006-present">
                ...Your markup here
            </FullpageSlide>
        </FullpageSection>
        <FullpageSection title="Projects">
            ...Your markup here
        </FullpageSection>
        <FullpageSection title="Review">
            ...Your markup here
        </FullpageSection>
        <FullpageSection title="Contact">
            ...Your markup here
        </FullpageSection>
    </Fullpage>
</div>
</body>

<style>
    body {
        overflow: hidden;
        cursor: none;
    }

    .follow-ball {
        width: 30px;
        height: 30px;
        position: fixed;
        top: 0;
        left: 0;
        z-index: 49;
        background: #ffffff;
        mix-blend-mode: difference;
        border-radius: 50%;
        pointer-events: none;
    }

    .ball {
        width: 10px;
        height: 10px;
        position: fixed;
        top: 0;
        left: 0;
        z-index: 50;
        background: #ffffff;
        mix-blend-mode: difference;
        border-radius: 50%;
        pointer-events: none;
    }


    /* if mobile, hide follow-ball and ball */

    @media (max-width: 768px) {
        .follow-ball {
            display: none;
        }

        .ball {
            display: none;
        }
    }

</style>