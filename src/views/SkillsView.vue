<template>
  <section
    class="py-10 px-5 bg-gray-200 dark:bg-gray-900 dark:text-gray-400 container"
    id="skills"
  >
    <h3 class="subtitle dark:text-white">Skills</h3>
    <p>
      As a student, I am constantly learning and expanding my knowledge. Some of the skills I have developed include:
    </p>
    <div class="grid md:grid-cols-3 mx-auto py-5">
      <div class="flex flex-col px-4 py-4" v-for="skill in skills" :key="skill">
        <div class="flex-grow flex flex-col">
          <h4 class="mt-0 dark:text-white">{{ skill.title }}</h4>
          <p class="text-justify line-clamp-4 flex-grow">
            {{ skill.description }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="js">
export default {
    name: "SkillsView",
    data() {
        return {
            skills: [{
                    title: "Languages",
                    description: "I am proficient in JavaScript, Python, and PHP, and have experience working with various databases such as MySql, Firebase, and mongodb. Additionally, I have expertise in web development with HTML and CSS. I have also worked with other languages such as Dart, C, C++, and Ruby."
                },
                {
                    title: "Frameworks",
                    description: "I use frameworks to speed up the development process and am open to exploring different options. I have experience working with Laravel, Codeigniter, Vue, React, Electron, Jquery, TailwindCSS, AntDesign, Bootstrap, MaterializeCSS, Flask, Flutter, Selenium, and Ruby on Rails."
                },
                {
                    title: "Tools/Platform",
                    description: "I use VS-Code, Jupyter Notebook, Git, and Docker on a daily basis. My primary operating system is Windows, but I also use Ubuntu inside Windows through WSL/WSLG."
                }
            ]
        }
    }
}
</script>
