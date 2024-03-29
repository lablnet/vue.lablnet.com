<template>
  <div>
    <section class="flex-none md:flex py-10 px-5 container">
      <div class="flex-none md:flex-1">
        <h1 class="title">Muhammad Umer Farooq</h1>
        <CollaboratorComp
          text="lablent"
          :picture="require('../assets/images/umer-removebg.png')"
          link="https://github.com/lablnet"
          :contributionsStatus="true"
        />

        <div class="flex md:hidden">
          <div class="sm:px-0 mx-auto">
            <img
              class="w-32 h-32 mx-auto rounded-full pointer-events-none"
              :src="require('../assets/images/umer2023.jpg')"
              alt="Muhammad Umer Farooq"
            />
          </div>
        </div>
        <p class="text-justify dark:text-gray-300">
          Hello, I am a Professional Software Developer with a passion for
          working on open-source products.
        </p>

        <p class="text-justify dark:text-gray-300">
          I have extensive experience in Full Stack development, including web,
          mobile, and desktop applications. I have also worked with web
          scraping, web crawling, and web API integrations. I have worked on a
          wide range of projects and have interest in deep learning, computer
          vision, deterministic algorithms, kernel development, compilers, and
          cryptography.
        </p>
        <p class="text-justify mb-6 dark:text-gray-300">
          I am highly motivated to work on open-source projects and contribute
          to the community. I am always looking for opportunities to collaborate
          and learn from others.
        </p>

        <br />
        <ButtonComp text="Contact Me" link="#contact" />
      </div>

      <div class="hidden md:flex">
        <div class="sm:px-0 md:px-20">
          <div class="rounded-full mt-12 overflow-hidden">
          <img
            class="
              w-64
              h-64
              ml-4
              rounded-full
              object-cover
              pointer-events-none
              mt-12
            "
            :src="require('../assets/images/umer2023.jpg')"
            alt="Muhammad Umer Farooq"
            style="margin-top: 16px;"
          />
        </div>
        </div>
      </div>
    </section>

    <hr class="mt-2 mb-2" v-if="theme === 'dark'" />
    <!--   Skills -->
    <SkillsView />

    <hr class="mt-2 mb-2" v-if="theme === 'dark'" />
    <!--   Projects -->
    <ProjectsView />

    <hr class="mt-2 mb-2" v-if="theme === 'dark'" />
    <!--   Education -->
    <EducationView />

    <hr class="mt-2 mb-2" v-if="theme === 'dark'" />

    <section class="py-10 px-5 container" id="showcase">
      <div class="grid grid-cols-1 gap-5 md:gap-8 xl:grid-cols-3 xl:gap-5">
        <div
          class="
            flex flex-col
            items-center
            justify-center
            text-center
            md:flex-row md:text-left
          "
        ></div>
      </div>
    </section>

    <hr class="mt-2 mb-2" v-if="theme === 'dark'" />

    <!--   Certificates -->
    <CertificatesView />

    <hr class="mt-2 mb-2" v-if="theme === 'dark'" />
    <!--   Contact -->
    <ContactView />
  </div>
</template>

<script lang="js">
import ButtonComp from "@/components/ButtonComp"
import SkillsView from "./SkillsView"
import EducationView from "./EducationView"
import ProjectsView from "./ProjectsView"
import CertificatesView from "./CertificatesView"
import CollaboratorComp from "@/components/CollaboratorComp"
import ContactView from "./ContactView"
import {
    useThemeStore
} from '@/store/ThemeStore';

export default {
    name: 'HomeView',
    components: {
        CollaboratorComp,
        ButtonComp,
        EducationView,
        ProjectsView,
        CertificatesView,
        ContactView,
        SkillsView,
    },
    computed: {
        theme() {
            return useThemeStore().theme;
        },
    }
}
</script>
