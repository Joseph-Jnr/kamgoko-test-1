<script setup>
import { ref } from 'vue'

const navLinks = ref([
  {
    url: '#',
    icon: '/assets/icons/Icon.svg',
    alt: 'dashboard icon',
    text: 'Dashboard',
    active: false,
  },
  {
    url: '#',
    icon: '/assets/icons/accounts.svg',
    alt: 'accounts icon',
    text: 'Accounts',
    active: true,
  },
  {
    url: '#',
    icon: '/assets/icons/cards.svg',
    alt: 'card icon',
    text: 'Cards',
    active: false,
  },
  {
    url: '#',
    icon: '/assets/icons/transactions.svg',
    alt: 'transactions icon',
    text: 'Transactions',
    active: false,
  },
  {
    url: '#',
    icon: '/assets/icons/payment.svg',
    alt: 'payment icon',
    text: 'Payment',
    active: false,
  },
  {
    url: '#',
    icon: '/assets/icons/invoice.svg',
    alt: 'invoice icon',
    text: 'Invoicing',
    active: false,
  },
  {
    url: '#',
    icon: '/assets/icons/trade.svg',
    alt: 'trade icon',
    text: 'Trading',
    active: false,
  },
  {
    url: '#',
    icon: '/assets/icons/report.svg',
    alt: 'report icon',
    text: 'Reports',
    active: false,
  },
])

const balances = ref([
  {
    url: '#',
    icon: '/assets/img/usa.png',
    alt: 'usa flag',
    text: '100,050.75 USD',
    active: false,
  },
  {
    url: '#',
    icon: '/assets/img/eur.png',
    alt: 'europe flag',
    text: '2310.40 EUR',
    active: false,
  },
  {
    url: '#',
    icon: '/assets/img/gbp.png',
    alt: 'british flag',
    text: '9455.50 GBP',
    active: false,
  },
  {
    url: '#',
    icon: '/assets/icons/plus.svg',
    alt: 'plus icon',
    text: 'Open a balance',
    active: false,
  },
])
</script>

<template>
  <aside class="sidenav">
    <div class="logo">
      <img src="/assets/img/logo.png" height="50" alt="logo" />
    </div>

    <div class="nav-group-wrap hide-scrollbar">
      <div class="nav-group">
        <div class="group-title">
          <p>Navigation</p>
        </div>
        <div class="group-links">
          <ul>
            <li
              v-for="(link, index) in navLinks"
              :key="index"
              :class="{ active: link.active }"
            >
              <a :href="link.url">
                <img :src="link.icon" :alt="link.alt" />
                <span>{{ link.text }}</span>
              </a>
            </li>
          </ul>
        </div>
      </div>

      <div class="nav-group">
        <div class="group-title">
          <p>Balances</p>
        </div>
        <div class="group-links">
          <ul>
            <li
              v-for="(link, index) in balances"
              :key="index"
              :class="{ active: link.active }"
            >
              <a :href="link.url">
                <img :src="link.icon" width="22" :alt="link.alt" />
                <span>{{ link.text }}</span>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>

    <div class="nav-group">
      <div class="group-links">
        <ul>
          <li>
            <a href="#">
              <img
                src="/assets/icons/settings.svg"
                width="22"
                alt="settings icon"
              />
              <span>Profile Settings</span>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </aside>
</template>
