<script>
    export const ssr = false;
    import { onMount } from 'svelte';
    import Scrambler from "$lib/helpers/scrambler.ts";
    const phrases = [
        "Developer",
        "Freelancer",
        "Musician",
        "Gamer",
    ]

    onMount(() => {
        const scrambler = new Scrambler();

        // for each phrase, every 3 seconds, scramble the phrase, if all phrases have been scrambled, start again
        let i = 0;
        setInterval(() => {
            if (i >= phrases.length) {
                i = 0;
            }
            scrambler.scramble(phrases[i], handlePhrase);
            i++;
        }, 3000);

        const handlePhrase = (phrase) => {
            // set the phrase to the span with the id of phrase
            console.log(phrase);
            document.querySelector("#phrase").innerHTML = phrase;
        }
    })

</script>

<p class="text-center text-lg font-semibold uppercase pt-5">I am a <span id="phrase" class="text-violet-400">Designer</span> </p>