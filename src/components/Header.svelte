<script>
    export let y;
    export let tabs = [
        { name: "Home", link: "#home" },
        { name: "About me", link: "#about" },
        { name: "Certification", link: "#Certification" }, 
        { name: "Journey", link: "#journey" },
    ];

    let isMenuOpen = false;

    function scrollToContact() {
        const contactSection = document.getElementById('contact');
        if (contactSection) {
            contactSection.scrollIntoView({ behavior: 'smooth' });
        }
    }

    function scrollToCertification() {
        const certificationSection = document.getElementById('certification');
        if (certificationSection) {
            certificationSection.scrollIntoView({ behavior: 'smooth' });
        }
    }

    function toggleMenu() {
        isMenuOpen = !isMenuOpen;
    }

    function closeMenu() {
        isMenuOpen = false;
    }
</script>

<header
    class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid " +
        (y > 0
            ? " py-4 bg-slate-950 border-violet-950"
            : " py-6 bg-transparent border-transparent")}
>
    <h1 class="font-medium">
        <b class="font-bold poppins">Muzacky</b>
    </h1>
    <!-- Desktop Navigation -->
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            {#if index === 2}  
                <button
                    on:click={scrollToCertification}
                    class="duration-200 hover:text-violet-400"
                >
                    <p>{tab.name}</p>
                </button>
            {:else}
                <a
                    href={tab.link}
                    class="duration-200 hover:text-violet-400"
                >
                    <p>{tab.name}</p>
                </a>
            {/if}
        {/each}

        <button
            on:click={scrollToContact}
            class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950"
        >
            <div
                class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9">Contact</h4>
        </button>
    </div>
    <button
        class="sm:hidden text-white"
        on:click={toggleMenu}
    >
        <i class="fa-solid fa-bars"></i>
    </button>
</header>

{#if isMenuOpen}
    <div class="sm:hidden fixed top-0 left-0 w-full h-full bg-slate-950 bg-opacity-95 z-50 flex flex-col items-center justify-center gap-8">
        {#each tabs as tab, index}
            {#if index === 2}  
                <button
                    on:click={() => { scrollToCertification(); closeMenu(); }}
                    class="text-white text-xl duration-200 hover:text-violet-400"
                >
                    {tab.name}
                </button>
            {:else}
                <a
                    href={tab.link}
                    class="text-white text-xl duration-200 hover:text-violet-400"
                    on:click={closeMenu}
                >
                    {tab.name}
                </a>
            {/if}
        {/each}
        <button
            on:click={() => { scrollToContact(); closeMenu(); }}
            class="blueShadow relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
        >
            <div
                class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9">Contact</h4>
        </button>
        <button
            class="text-white text-2xl mt-8"
            on:click={closeMenu}
        >
            <i class="fa-solid fa-times"></i>
        </button>
    </div>
{/if}