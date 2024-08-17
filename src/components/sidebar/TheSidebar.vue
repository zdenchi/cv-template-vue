<template>
  <aside class="space-y-4 bg-slate-800 py-12 text-white">
    <CVPhoto />

    <CVSection title="Contacts">
      <CVContacts />
    </CVSection>

    <CVSection
      v-for="skill in skills"
      :key="skill.title"
      :title="skill.title"
      :list="skill.children"
      :list-class="skill.class"
    />
  </aside>
</template>

<script setup>
import CVPhoto from './CVPhoto.vue'
import CVContacts from './CVContacts.vue'
import CVSection from '../CVSection.vue'

const skills = {
  tech: {
    title: 'Tech skills',
    children: [
      'HTML5',
      'CSS3 (SCSS), Tailwind CSS',
      'JavaScript (ES5, ES6)',
      'TypeScript',
      'Vue/Nuxt/Nitro (Vuex, Vue Router, Pinia)',
      'Node.js, Express.js, REST API',
      'PostgreSQL, MongoDB, Firebase, Prisma ORM',
      'Figma',
      'Git'
    ],
    class: 'list-inside list-disc'
  },
  soft: {
    title: 'Soft Skills',
    children: ['Problem-solving', 'Teamwork', 'Communication', 'Stress resistance'],
    class: 'list-inside list-disc'
  },
  languages: {
    title: 'Languages',
    children: ['Ukrainian - native', 'English - intermediate'],
    class: ''
  }
}
</script>
