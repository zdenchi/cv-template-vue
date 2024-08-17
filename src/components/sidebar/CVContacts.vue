<template>
  <ul class="mt-3 flex flex-col gap-2 text-xs font-medium">
    <li v-for="contact in contacts" :key="contact.label">
      <a
        :href="contact.href"
        class="print-data flex items-center gap-2 print:after:content-[attr(data-print)]"
        :data-print="contact.print || contact.label"
      >
        <span class="rounded-full bg-white p-1 text-slate-800">
          <component :is="contact.icon" class="size-4" />
        </span>
        <span class="print:hidden">{{ contact.label }}</span>
      </a>
    </li>
  </ul>
</template>

<script setup>
import IconEmail from '../icons/IconEmail.vue'
import IconPhone from '../icons/IconPhone.vue'
import IconGithub from '../icons/IconGithub.vue'
import IconTelegram from '../icons/IconTelegram.vue'
import IconLinkedin from '../icons/IconLinkedin.vue'
import IconLocation from '../icons/IconLocation.vue'

const { VITE_PHONE, VITE_EMAIL, VITE_USERNAME } = import.meta.env

const contacts = [
  {
    icon: IconPhone,
    href: `tel:${VITE_PHONE.replace(/\s/g, '')}`,
    label: `${VITE_PHONE}`
  },
  {
    icon: IconEmail,
    href: `mailto:${VITE_EMAIL}`,
    label: `${VITE_EMAIL}`
  },
  {
    icon: IconLinkedin,
    href: `https://linkedin.com/in/${VITE_USERNAME}`,
    label: `LinkedIn`,
    print: `linkedin.com/in/${VITE_USERNAME}`
  },
  {
    icon: IconGithub,
    href: `https://github.com/${VITE_USERNAME}`,
    label: `GitHub`,
    print: `github.com/${VITE_USERNAME}`
  },
  {
    icon: IconTelegram,
    href: `https://t.me/${VITE_USERNAME}`,
    label: `@${VITE_USERNAME}`,
    print: `t.me/${VITE_USERNAME}`
  },
  {
    icon: IconLocation,
    href: 'https://maps.app.goo.gl/dyEMT5gMWCpJDMpx5',
    label: 'Kyiv, Ukraine'
  }
]
</script>
