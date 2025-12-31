<script>
    import Step from "./Step.svelte";

    function scrollToProjects() {
        const projectsSection = document.getElementById('projects');
        if (projectsSection) {
            projectsSection.scrollIntoView({ behavior: 'smooth' });
        }
    }

    let steps = [
        {
            name: "HTML",
            icon: "fa-brands fa-html5",
            description:
                "HTML (HyperText Markup Language) adalah bahasa markup standar untuk membuat struktur dan konten halaman web, berfungsi sebagai kerangka dasar yang memberitahu browser bagaimana menampilkan teks, gambar, video, dan elemen lain menggunakan tag seperti <p> untuk paragraf atau <img> untuk gambar, dan bekerja bersama CSS (untuk gaya) dan JavaScript (untuk interaktivitas) untuk membangun website yang kaya dan interaktif. ",
        },
        {
            name: "CSS",
            icon: "fa-brands fa-css3-alt",
            description:
                "CSS (Cascading Style Sheets) adalah bahasa stylesheet untuk mendesain tampilan website, mengatur warna, font, tata letak, dan elemen visual lainnya agar lebih menarik, serta memisahkan konten (HTML) dari presentasinya, menjadikannya lebih praktis, konsisten, dan responsif di berbagai perangkat.",
        },
        {
            name: "JavaScript",
            icon: "fa-brands fa-js",
            description:
                "JavaScript (JS) adalah bahasa pemrograman ringan dan dinamis yang menjadi salah satu pilar utama web bersama HTML dan CSS, digunakan untuk membuat halaman web menjadi interaktif, dinamis, dan fungsional, seperti menampilkan animasi, peta interaktif, menu dropdown, atau memperbarui konten secara real-time tanpa perlu me-reload halaman.",
        },
    ];

    let benefits = [
        {
            metric: "10x",
            name: "a self taught developer",
            description:
                "I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, backend programming, design, cloud services and much much more.",
        },
        {
            name: "a product design & UX finatic",
            description:
                "Carefully crafting and designing amazing user experiences allows me to express and experiment with every morsel of creativity I have. I love the challenge of learning new design concepts and enabling users with amazing online experiences.",
        },
        {
            name: "an excellent communicator",
            description:
                "Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.",
        },
    ];

    let certifications = [
    {
        name: "AI",
        icon: "fa-solid fa-brain",  
        image: "images/belajar_ai.png",
    },
    {
        name: "Pemograman Web",
        icon: "fa-solid fa-code",  
        image: "images/pemograman_web.png",
    },
    {
        name: "JavaScript",
        icon: "fa-brands fa-js",  
        image: "images/java_script.png",
    },
    {
        name: "Front-End Web",
        icon: "fa-solid fa-desktop",  
        image: "images/front_end.png",
    },
];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
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
                I'am an <span class="text-violet-400"> informatics engineering student at Yudharta University, Pasuruan. </span> 
                I love creating beautiful, functional websites and web applications
            </p>
            <button
                on:click={scrollToProjects}
                class="blueShadow mx-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-4 py-2 sm:px-6 sm:py-3 group rounded-full bg-white text-slate-950"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </button>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/profile.png"}
                alt="M Muzacky Riswanda"
                class="object-cover z-[2] max-h-[70vh]"
            />
        </div>
        <!-- <div  class="flex p-0.5 relative max-w-[700px] w-full mx-auto">
            <div
                class="absolute inset-0 overflow-hidden rounded-md flex items-center justify-center"
            >
                <div
                    class="bg-gradient-to-r absolute inset-[-20px]  from-violet-800 to-indigo-800 specialSpin"
                />
            </div>

            <img
                src={"images/zetane-engine.jpeg"}
                alt="Zetane Engine"
                class="w-full h-full object-cover z-[2]"
            />
        </div> -->
        
    </section>
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>
        <a
            href="https://github.com/Zacky171"
            target="_blank"
            class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
        >
            <i class="fa-regular fa-circle-play" />
            <p>see my work here</p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p> <strong
                        class="text-violet-400"
                        >HTML (HyperText Markup Language) adalah</strong
                    > berfungsi sebagai kerangka dasar yang memberitahu browser bagaimana menampilkan teks, gambar, video, dan elemen lain dan bekerja bersama CSS (untuk gaya) dan JavaScript (untuk interaktivitas) untuk membangun website yang kaya dan interaktif. 

                </p>
            </Step>
            <Step step={steps[1]}>
                <p><strong
                        class="text-violet-400">CSS (Cascading Style Sheets) adalah</strong
                    >,
                    
                    
                     bahasa stylesheet untuk mendesain tampilan website, mengatur warna, font, tata letak, dan elemen visual lainnya agar lebih menarik, serta memisahkan konten (HTML) dari presentasinya, menjadikannya lebih praktis, konsisten, dan responsif di berbagai perangkat.
                </p>
            </Step>
            <Step step={steps[2]}>
                <p><strong class="text-violet-400"
                        >JavaScript (JS) adalah</strong
                    >  
                    bahasa pemrograman yang digunakan untuk membuat website interaktif dan dinamis, memungkinkan pengguna untuk berinteraksi dengan elemen-elemen halaman web secara langsung, seperti mengubah tampilan, menangani input pengguna, dan memanipulasi konten secara real-time.
                </p>
            </Step>
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
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}

                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
        <h5 class={" text-2xl sm:text-3xl font-semibold text-center poppins "}>
            My <span class="text-violet-400">Certification</span> Course
        </h5>
        <div class="flex flex-col gap-10 max-w-[800px] mx-auto w-full">
            <div class="overflow-hidden relative">
                <div class="flex animate-slide-continuous">
                    {#each certifications as cert}
                        <div class="flex-shrink-0 flex flex-col items-center gap-4 p-4 bg-white text-slate-700 rounded-lg shadow-md mx-2 min-w-[200px]">
                            <i class="{cert.icon} text-4xl text-violet-400"></i>
                            <h4 class="text-lg font-semibold text-center">{cert.name}</h4>
                        </div>
                    {/each}
                    {#each certifications as cert}
                        <div class="flex-shrink-0 flex flex-col items-center gap-4 p-4 bg-white text-slate-700 rounded-lg shadow-md mx-2 min-w-[200px]">
                            <i class="{cert.icon} text-4xl text-violet-400"></i>
                            <h4 class="text-lg font-semibold text-center">{cert.name}</h4>
                        </div>
                    {/each}
                </div>
            </div>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        <p class="mx-auto">So why not invest?</p>
    </section>
</main>

<style>
    @keyframes slide-continuous {
        0% {
            transform: translateX(100%);
        }
        100% {
            transform: translateX(-100%);
        }
    }

    .animate-slide-continuous {
        animation: slide-continuous 10s linear infinite;
    }
</style>
