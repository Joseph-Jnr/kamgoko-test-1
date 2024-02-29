<script setup>
import Header from './components/Header.vue'
import Sidenav from './components/Sidenav.vue'
import Tabs from './components/Tabs.vue'
import Transactions from './components/Transactions.vue'
import AccountDetails from './components/AccountDetails.vue'
import Footer from './components/Footer.vue'
import MobileNav from './components/MobileNav.vue'
</script>

<template>
  <main class="app">
    <Sidenav />
    <div class="main-body">
      <Header />
      <div class="main-body-content">
        <!-- Account balance -->
        <div class="container">
          <div class="account_balance">
            <h1>$120,420.50</h1>
            <span>Account **** 4567</span>
          </div>
        </div>

        <!-- Tabs -->
        <Tabs />

        <div class="container">
          <div class="section-grid">
            <div class="section_wrapper order-1 hide-scrollbar">
              <Transactions />
              <div class="fade-effect"></div>
            </div>
            <div class="section_wrapper order-2 hide-scrollbar">
              <AccountDetails />
            </div>
          </div>
        </div>
      </div>
      <footer>
        <div class="container">
          <Footer />
          <MobileNav />
        </div>
      </footer>
    </div>
  </main>
</template>
