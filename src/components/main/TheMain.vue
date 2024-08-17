<template>
  <div class="text-gray-800">
    <CVBio />

    <div class="space-y-4 pr-10">
      <CVSection title="Summary">
        <CVSummary />
      </CVSection>

      <CVSection title="Experience">
        <CVExperience />
      </CVSection>

      <CVSection
        title="Education"
        :list="education"
        list-class="list-inside list-disc text-gray-700"
      >
        <template #li>
          <li>
            Kyiv Polytechnic Institute (KPI)<br />Informatics and Computer Science (FIOT)
            (bachelor's degree)<br />2008 - 2012
          </li>
        </template>
        <CVEducation />
      </CVSection>
    </div>
  </div>
</template>

<script setup>
import CVBio from './CVBio.vue'
import CVExperience from './CVExperience.vue'
import CVSummary from './CVSummary.vue'
import CVSection from '../CVSection.vue'

const education = [
  'Mastering Nuxt 3 (2022)',
  '[Udemy]: NodeJS - The Complete Guide (MVC, REST APIs, GraphQL, Deno) (2020)',
  '[Udemy]: Vue - The Complete Guide (incl. Router & Composition API) (2020)',
  '[Udemy]: The Complete Web Development Bootcamp (2020)',
  '[Udemy]: The Web Developer Bootcamp (2019)'
]
</script>
