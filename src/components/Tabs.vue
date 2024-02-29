<script setup>
import { ref } from 'vue'

const tabLinks = ref([
  {
    url: '#',
    icon: '/assets/icons/transfer.svg',
    alt: 'icon',
    text: 'Transfer',
  },
  {
    url: '#',
    icon: '/assets/icons/make_payment.svg',
    alt: 'icon',
    text: 'Make a payment',
  },
  {
    url: '#',
    icon: '/assets/icons/convert.svg',
    alt: 'icon',
    text: 'Convert',
  },
  {
    url: '#',
    icon: '/assets/icons/request.svg',
    alt: 'icon',
    text: 'Request',
  },
])
</script>

<template>
  <div class="tabs">
    <div class="container">
      <div class="tabs-flex">
        <div class="links">
          <a v-for="(link, index) in tabLinks" :key="index" :href="link.url">
            <div class="single-link">
              <img :src="link.icon" :alt="link.text" />
              <p>{{ link.text }}</p>
            </div>
          </a>
        </div>
        <div class="filter">
          <div class="single-link">
            <img src="/assets/icons/search.svg" alt="icon" />
            <p>Search</p>
          </div>
          <div class="single-link">
            <img src="/assets/icons/calendar.svg" alt="icon" />
            <p>August 2022</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
