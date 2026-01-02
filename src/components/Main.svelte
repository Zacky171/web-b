<script>
    function scrollToContact() {
        const contactSection = document.getElementById('contact');
        if (contactSection) {
            contactSection.scrollIntoView({ behavior: 'smooth' });
        }
    }

    function scrollToJourney() {
        const journeySection = document.getElementById('journey');
        if (journeySection) {
            journeySection.scrollIntoView({ behavior: 'smooth' });
        }
    }

    function scrollToProjects() {
        const projectsSection = document.getElementById('projects');
        if (projectsSection) {
            projectsSection.scrollIntoView({ behavior: 'smooth' });
        }
    }

    let certifications = [
        {
            name: "AI",
            icon: "fa-solid fa-brain",  
            image: "/images/belajar_ai.png",
            link: "https://www.dicoding.com/certificates/6RPNG4VR8Z2M",  
        },
        {
            name: "Pemograman Web",
            icon: "fa-solid fa-code",  
            image: "/images/pemograman_web.png",
            link: "https://www.dicoding.com/certificates/2VX3545JJPYQ",
        },
        {
            name: "JavaScript",
            icon: "fa-brands fa-js",  
            image: "/images/java_script.png",
            link: "https://www.dicoding.com/certificates/98XWOOMY9ZM3",
        },
        {
            name: "Front-End Web",
            icon: "fa-solid fa-desktop",  
            image: "/images/front_end.png",
            link: "https://www.dicoding.com/certificates/EYX4KMV86PDL",
        },
    ];

    let education = [
        {
            title: "Smk Negeri Prigen",
            subtitle: "Multimedia",
            date: "July 2021 - May 2024",
        },
        {
            title: "Mocci Academy",
            subtitle: "3D Modeller, Lrc, Render Wrangler",
            date: "July 2022 - December 2022",
        },
        {
            title: "Mocca Studio",
            subtitle: "Render Wrangler",
            date: "January 2023 - December 2023",
        },
        {
            title: "Universitas Yudharta Pasuruan",
            subtitle: "Informatics Engineering",
            date: "September 2024 - Now",
        },
        {
            title: "ID Camp x Dicoding",
            subtitle: "Front-end",
            date: "September 2025 - November 2025",  
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4 bg-slate-950 text-white">

    <section
        id="home"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">M Muzacky</span> Riswanda
                <br />web
                <span class="poppins text-violet-400">developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                I'm an <span class="text-violet-400">informatics engineering student at Yudharta University, Pasuruan.</span> 
                I love creating beautiful, functional websites and web applications.
            </p>

            <button
                on:click={() => { scrollToContact(); }}
                class="blueShadow mx-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-4 py-2 sm:px-6 sm:py-3 group rounded-full bg-white text-slate-950"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Contact</h4>
            </button>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src="/images/profile.png"
                alt="M Muzacky Riswanda"
                class="object-cover z-[2] max-h-[70vh] rounded-lg"
            />
        </div>
    </section>

    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
            <h6 class="text-large sm:text-xl md:text-2xl">
                Want to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <div class="max-w-4xl mx-auto text-center">
            <p class="text-base sm:text-lg md:text-xl leading-relaxed">
                Hi am an Informatics Engineering student with a strong interest in technology, especially in web development. 
                I actively study various web technologies, including user interface design, data management, and performance 
                optimization to ensure applications run efficiently and provide a smooth user experience.

                I regularly work on website development projects for academic purposes, personal learning, and portfolio building. 
                My current focus is on improving my ability to create responsive, well structured, and scalable websites.

                As part of my commitment to continuous growth, I have completed several training programs and earned certifications 
                related to web development and programming. You can find these certifications in the section below as proof of my dedication to developing strong technical skills.

                I am always open to learning new things, collaborating with others, and taking on challenges that expand my 
                knowledge and experience. My goal is to become a web developer who not only has strong technical skills, but also delivers practical and impactful solutions.
            </p>
        </div>
    </section>

    <section id="certification" class="py-20 lg:py-32 flex flex-col gap-16">
        <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">
            My <span class="text-violet-400">Certification</span> Course
        </h5>
        <div class="flex flex-col gap-10 max-w-[800px] mx-auto w-full -mt-2 sm:-mt-4 md:-mt-6"> 
            <div class="overflow-hidden relative">
                <div class="flex animate-slide-continuous gap-4 sm:gap-6 md:gap-8"> 
                    {#each certifications as cert}
                        <a href={cert.link} target="_blank" rel="noopener noreferrer" class="flex-shrink-0 flex flex-col items-center gap-4 p-4 text-white rounded-lg mx-2 min-w-[200px] sm:min-w-[250px] md:min-w-[300px] hover:bg-slate-700 transition-colors duration-200 cursor-pointer">
                            <img src={cert.image} alt={cert.name} class="w-full h-32 sm:h-40 md:h-48 object-cover rounded-lg" />
                            <h4 class="text-lg sm:text-xl font-semibold text-center">{cert.name}</h4>
                        </a>
                    {/each}
                    {#each certifications as cert}
                        <a href={cert.link} target="_blank" rel="noopener noreferrer" class="flex-shrink-0 flex flex-col items-center gap-4 p-4 text-white rounded-lg mx-2 min-w-[200px] sm:min-w-[250px] md:min-w-[300px] hover:bg-slate-700 transition-colors duration-200 cursor-pointer">
                            <img src={cert.image} alt={cert.name} class="w-full h-32 sm:h-40 md:h-48 object-cover rounded-lg" />
                            <h4 class="text-lg sm:text-xl font-semibold text-center">{cert.name}</h4>
                        </a>
                    {/each}
                </div>
            </div>
        </div>
        <div class="mx-auto -mt-8 sm:-mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
    </section>

    <section id="journey" class="py-20 lg:py-32 flex flex-col gap-16">
        <div class="text-center">
            <h1 class="font-semibold text-3xl sm:text-4xl md:text-5xl mb-4">Journey</h1>
            <div class="text-lg sm:text-xl text-violet-400">My Education & Experience</div>
        </div>
        <div class="max-w-4xl mx-auto">
            <h2 class="text-2xl sm:text-3xl font-semibold mb-8">Education & Training</h2>
            <div class="relative">
                <div class="absolute left-4 top-0 bottom-0 w-1 bg-violet-400"></div>
                {#each education as item, index}
                    <div class="flex items-start gap-6 mb-8 relative">
                        <div class="w-8 h-8 bg-violet-400 rounded-full flex-shrink-0 mt-1"></div>
                        <div class="flex-1">
                            <h3 class="text-xl sm:text-2xl font-semibold">{item.title}</h3>
                            <p class="text-violet-300 mb-2">{item.subtitle}</p>
                            <div class="text-sm text-slate-400">{item.date}</div>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>
</main>

<style>
    @keyframes slide-continuous {
        0% { transform: translateX(0); }
        100% { transform: translateX(-50%); }
    }
    .animate-slide-continuous {
        animation: slide-continuous 20s linear infinite;
    }
</style>