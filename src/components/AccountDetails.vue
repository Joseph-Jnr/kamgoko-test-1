<script setup>
import DetailsCard from './DetailsCard.vue'
import DetailsTray from './DetailsTray.vue'

import { ref } from 'vue'
// Use a ref to track the visibility of the DetailsTray
const isTrayVisible = ref(false)

// Function to toggle the visibility of the DetailsTray
const toggleTray = () => {
  isTrayVisible.value = !isTrayVisible.value
}
</script>

<template>
  <div class="account-details">
    <div class="ad_header">
      <p>Linked Card</p>
    </div>

    <div class="card">
      <div class="card-wrap">
        <div class="image">
          <img src="/assets/img/mesh-gradient.png" width="100" alt="img" />
        </div>
        <div class="text_area">
          <h3>Visa Gold Paywave</h3>
          <div class="card_details">
            <p>**** 8790</p>
            <p>03/22</p>
          </div>
        </div>
      </div>
      <div class="card-mobile-footer">
        <div class="text" @click="toggleTray">
          <img src="/assets/icons/make_payment.svg" alt="icon" />
          <h4>See account details</h4>
        </div>
      </div>
    </div>

    <DetailsCard />

    <DetailsTray :isTrayVisible="isTrayVisible" />
  </div>
</template>
