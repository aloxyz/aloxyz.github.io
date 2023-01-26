<template>
    <MainSmall v-if="isSmallScreen"/>
    <MainMid v-else-if="isMidScreen"/>
    <Main v-else/>
</template>

<script>

import Main from './components/Main.vue';
import MainMid from './components/MainMid.vue';
import MainSmall from './components/MainSmall.vue';

export default {
    name: 'App',
    components: {
        Main,
        MainMid,
        MainSmall
    },

    data() {
        return {
            isSmallScreen: false,
            isMidScreen: false,

            colors: {
                azure: "#7BCCEE",
                orange: "#FFA500",
                green: "#20BF55",
                red: "#E71D36",
                blue: "#0B4F6C"
            },

            biography: "I am Gabriele, also known as alo. My current focus is studying Computer Science at the University of Messina, while also exploring my interests in graphic design, music, sports, and engineering. I am also a dedicated Calisthenics athlete, having been training for about a year. My passions include sciences and arts, and I am also an advocate for FOSS.",

            skills: {
                tech: [
                    "C",
                    "Java",
                    "Python",
                    "Vue.js",
                    "Docker",
                ],

                graphics: [
                    "Blender3D",
                    "Photoshop",
                    "Illustrator",
                    "Gimp",
                    "Ink/Stitch"
                ],

                audio: [
                    "Bitwig",
                    "FL Studio",
                    "Reaper",
                    "Sound synthesis"
                ]

            },

            links: [
                {
                    name: "GitHub",
                    url: "https://github.com/aloxyz",
                },
                {
                    name: "GitLab",
                    url: "https://gitlab.com/aloxyz",
                },
                {
                    name: "Twitter",
                    url: "https://twitter.com/alodesu",
                },
                {
                    name: "Instagram",
                    url: "https://instagram.com/alo.xyz",
                },
                {
                    name: "Soundcloud",
                    url: "https://soundcloud.com/aloxyz",

                },
                {
                    name: "Bandcamp",
                    url: "https://aloxyz.bandcamp.com/",
                },


            ],

            sections: {
                projects: {
                    title: "Projects",
                    color: "#7bccee",
                    cards: [
                        {
                            title: "Platea",
                            content: "Open source Docker container orchestration tool",
                            buttons: [
                                {
                                    url: "https://gitlab.com/aloxyz/platea",
                                    content: '<i class="fa-brands fa-gitlab"></i>',
                                    color: "#FFA500"
                                },
                            ]

                        },
                        {
                            title: "Private Room - CoDeRTD",
                            content: "Proof-gathering tool for illegal online content publishing",
                            buttons: [
                                {
                                    url: "https://www.codertd.com/it/privateroom",
                                    content: '<i class="fa-solid fa-link"></i>',
                                    color: "#7bccee"
                                },
                            ]
                        }
                    ]
                },

                music: {
                    title: "Music",
                    color: "#FFA500",
                    cards: [
                        {
                            title: "Verdant - Colorful World",
                            content: "GBA-inspired instrumental music for the Verdant (former H+ME) videogame",
                            buttons: [
                                {
                                    url: "https://www.youtube.com/playlist?list=PLkbHFHowIf5U7N8W45BGumo-1fE5C8wcT",
                                    content: '<i class="fa-brands fa-youtube"></i>',
                                    color: "#FFA500"
                                },
                                {
                                    url: "hme.plus",
                                    content: '<i class="fa-solid fa-link"></i>',
                                    color: "#7bccee"
                                },
                            ]
                        }
                    ]
                }

            }
        }
    },

    computed: {

    },

    methods: {
        randomColor() {
            var colorKeys = Object.keys(this.colors)
            var randomKey = colorKeys[Math.floor(Math.random() * colorKeys.length)];

            return this.colors[randomKey];
        },

        midViewHandler() {
            this.isMidScreen = window.innerWidth <= 1200;
        },

        smallViewHandler() {
            this.isSmallScreen = window.innerWidth <= 768;
        },
    },

    created() {
        this.midViewHandler();

        this.smallViewHandler();
        window.addEventListener('resize', this.midViewHandler);
        window.addEventListener('resize', this.smallViewHandler);

    }

}


</script>

<style>

* {
    color: #333333;
    font-family: Helvetica;
    list-style: none;
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    scroll-behavior: smooth;
}

body {margin: 0em;}
h1 {font-size: 38px;}
h2 {font-size: 28px;}
h3 {font-size: 20px;}
p {font-size: 18px;}

/* large screens */
@media screen and (min-width: 768px) {
    body {margin: 3em 10vw 3em 10vh;}
    h1 {font-size: 72px;}
    h2 {font-size: 32px;}
    h3 {font-size: 22px;}
    p {font-size: 18px;}
}





a:hover {
    transition: .3s;
    color: #7bccee;
}

/* footer */


/* dot background animation */
.dotBg {
    background-image: radial-gradient(#7bccee 2px, transparent 0);
    background-size: 40px 40px;

    animation:
        moveBg 20s infinite linear;
}

@keyframes moveBg {
    100% {
        background-position: 100%;
    }
}


/* typewriter animation */
.typewriter>* {
    white-space: nowrap;
    font-family: monaco, monospace;
    font-weight: 600;
    overflow: hidden;
    border-right: .75em solid orange;
    width: 0;
    animation:
        typing 2s steps(23, end) forwards,
        blink 1s infinite;
}

.typewriter {
    display: inline-block;
}

@keyframes typing {
    from {
        width: 0
    }

    to {
        width: 100%
    }

    from {
        padding-right: 0
    }

    to {
        padding-right: .75em
    }
}

@keyframes blink {
    from {
        border-color: transparent
    }

    to {
        border-color: orange;
    }
}
</style>

