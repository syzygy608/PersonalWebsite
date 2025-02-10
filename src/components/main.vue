<template>
    <div class = "flex min-h-[calc(100dvh-6rem)]">
        <div class = "flex w-[min(90%,50rem)] mx-auto my-3">
            <div class = "flex flex-col justify-center">
                <div class = "flex flex-col md:flex-row items-center bg-amber-50 py-3" id = "about">
                    <div class = "w-3/12 flex justify-center">
                        <img src = "/avatar.jpg" alt = "avatar" class = "w-[15rem] px-3 rounded-lg md:rounded-none" />
                    </div>
                    <div class = "text-md font-light w-9/12">
                        Hello, My name is <span class = "font-medium">Han-Ping Wu</span>. 
                        I am a undergraduate student at National Chung Cheng University, Taiwan.
                        I am interested in <span class = "font-medium">Web Development</span> and <span class = "font-medium">Algorithm</span>.
                        I am currently working on research about <span class = "font-medium">Pairwise Comparison</span> and <span class = "font-medium">Ranking</span>
                        in <span class = "font-medium">Digital Society and Security Lab (DIGI-SSL)</span> at CCU.
                        I will graduate in <span class = "font-medium">June 2025</span> and join the <span class = "font-medium">Master's Program</span> at NCKU.
                        In NCKU I will join the <span class = "font-medium">Supercomputing and Intelligent Visual System Laboratory (SIVSL)</span> and continue studying
                        <span class = "font-medium">Algorithm</span> specially in graph theory.
                    </div>
                </div>
                <div class = "flex flex-col items-center p-3">
                    <h1 class = "text-2xl font-bold py-2 underline">
                        Education
                    </h1>
                    <div>
                        <ul>
                            <li v-for = "edu in educationList" :key = "edu.year" class = "py-1">
                                <span class = "font-bold">{{edu.year}}</span> - {{edu.school}} - {{edu.degree}}
                            </li>
                        </ul>
                    </div>
                </div>
                <div class = "flex flex-col items-center p-3">
                    <h1 class = "text-2xl font-bold py-2 underline">
                        Experience
                    </h1>
                    <div>
                        <ul>
                            <li v-for = "exp in experienceList" :key = "exp.year" class = "py-1">
                                <span class = "font-bold">{{exp.year}}</span> - {{exp.organization}} - {{exp.position}}
                            </li>
                        </ul>
                    </div>
                </div>
                <div class = "flex flex-col items-center p-3">
                    <h1 class = "text-2xl font-bold py-2 underline">
                        Research Interest
                    </h1>
                    <div>
                        <ul class = "text-center flex space-x-2">
                            <li class = "py-1">
                                Pairwise Comparison,
                            </li>
                            <li class = "py-1">
                                Algorithm,
                            </li>
                            <li class = "py-1">
                                Graph Theory
                            </li>
                        </ul>
                    </div>
                </div>
                <div class = "flex flex-col items-center p-3">
                    <h1 class = "text-2xl font-bold py-2 underline">
                        Achievement
                    </h1>
                    <div>
                        <ul>
                            <li v-for = "ach in achievementList" :key = "ach.year" class = "py-1">
                                <span class = "font-bold">{{ach.year}}</span>
                                <ul>
                                    <li v-for = "item in ach.items" :key = "item" class = "py-1">
                                        {{item}}
                                    </li>
                                </ul>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class = "flex flex-col items-center p-3" id = "contact">
                    <h1 class = "text-2xl font-bold py-2 underline">
                        Contact
                    </h1>
                    <div>
                        <ul class = "text-center flex space-x-2">
                            <li class = "py-1">
                                Email: <span class = "font-bold">
                                    <a href = "mailto:bey0nd@csie.io" class = "hover:text-blue-500 duration-500 underline">
                                        bey0nd [at] csie [dot] io
                                    </a>
                                </span>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
            
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const educationList = ref([
    {
        year: "2021~2025",
        school: "National Chung Cheng University",
        degree: "B.S. in Computer Science"
    },
    {
        year: "2025~",
        school: "National Cheng Kung University",
        degree: "M.S. in Computer Science"
    }
])

const experienceList = ref([
    {
        year: "2024~2025",
        organization: "Digital Society and Security Lab (DIGI-SSL)",
        position: "Capstone Project Researcher"
    },
    {
        year: "2023~2025",
        organization: "CCU Programming Contest Team",
        position: "Leader"
    }
])

const achievementList = ref([
    {
        year: "2024",
        items: [
            "ICPC Taiwan Online Programming Contest - Bronze Medal",
            "National Collegiate Programming Contest - Honorable Mention",
            "ICPC Taichung Regional Contest - Bronze Medal"
        ]
    },
    {
        year: "2023",
        items: [
            "ICPC Taiwan Online Programming Contest - Silver Medal",
            "National Collegiate Programming Contest - Honorable Mention",
            "ICPC Taoyuan Regional Contest - Honorable Mention"
        ]
    }
])

</script>