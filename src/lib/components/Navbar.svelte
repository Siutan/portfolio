<script>
    import "./Links.svelte";
    import Links from "$lib/components/Links.svelte";
</script>

<nav class="flex justify-between bg-black text-white ">
    <div class="px-5 xl:px-12 p-2 flex w-full items-center">
        <!-- Nav Links -->
        <ul class="hidden md:flex px-4 mx-auto font-semibold font-heading space-x-10">
            <Links linkText="About" linkUrl="About" />
            <Links linkText="Projects" linkUrl="Projects" />
            <Links linkText="Reviews" linkUrl="Reviews" />
            <Links linkText="Contact" linkUrl="Contact" />
        </ul>
        <!-- Theme Switcher -->
<!--        <div class="hidden xl:flex items-center space-x-5 items-center">-->
<!--            <a class="hover:text-gray-200" href="#">-->
<!--                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">-->
<!--                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" />-->
<!--                </svg>-->
<!--            </a>-->
<!--        </div>-->
    </div>
    <!-- Responsive navbar -->
    <a class="navbar-burger self-center mr-12 xl:hidden" href="#">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 hover:text-gray-200" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
    </a>
</nav>