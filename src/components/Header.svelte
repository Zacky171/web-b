<script>
    export let y;

    let isMenuOpen = false;

    function scrollToProjects() {
        const projectsSection = document.getElementById('projects');
        if (projectsSection) {
            projectsSection.scrollIntoView({ behavior: 'smooth' });
        }
    }

    export let tabs = [
        { name: "Projects ", link: "#projects" },
        { name: "About me", link: "#about" },
        { name: "Blog", link: "https://github.com/Zacky171" },
        // { name: "Contact", link: "" },
        // {name: '', link: ''},

    ];
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
            <a
                href={tab.link}
                class="duration-200 hover:text-violet-400"
                target={index === 2 ? "_blank" : ""}
            >
                <p>{tab.name}</p>
            </a>
        {/each}

        <button
            on:click={scrollToProjects}
            class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950"
        >
            <div
                class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9">Get in touch</h4>
        </button>
    </div>
    <!-- Mobile Menu Button -->
    <button
        class="sm:hidden text-white"
        on:click={() => isMenuOpen = !isMenuOpen}
    >
        <i class="fa-solid fa-bars"></i>
    </button>
</header>

<!-- Mobile Menu -->
{#if isMenuOpen}
    <div class="sm:hidden fixed top-0 left-0 w-full h-full bg-slate-950 bg-opacity-95 z-50 flex flex-col items-center justify-center gap-8">
        {#each tabs as tab, index}
            <a
                href={tab.link}
                class="text-white text-xl duration-200 hover:text-violet-400"
                target={index === 2 ? "_blank" : ""}
                on:click={() => isMenuOpen = false}
            >
                {tab.name}
            </a>
        {/each}
        <button
            on:click={() => { scrollToProjects(); isMenuOpen = false; }}
            class="blueShadow relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
        >
            <div
                class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9">Get in touch</h4>
        </button>
        <button
            class="text-white text-2xl mt-8"
            on:click={() => isMenuOpen = false}
        >
            <i class="fa-solid fa-times"></i>
        </button>
    </div>
{/if}
