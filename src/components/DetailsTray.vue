<script setup>
import { ref } from 'vue'

// Create a ref to track the visibility of the DetailsTray
const isTrayVisible = ref(false)

// Function to toggle the visibility of the DetailsTray
const toggleTray = () => {
  isTrayVisible.value = !isTrayVisible.value
}
</script>

<template>
  <div class="details-tray" v-if="isTrayVisible">
    <div class="backdrop">
      <div class="user-account-details mobile">
        <div class="header">
          <p>Account Details</p>
        </div>

        <div class="uad_wrap">
          <div class="single_detail">
            <p>Account name</p>
            <h3>Premium Account</h3>
          </div>
          <div class="single_detail">
            <p>Account number</p>
            <h3>UK64CT0000010034567</h3>
          </div>
          <div class="single_detail">
            <p>Account type</p>
            <h3>Single Currency</h3>
          </div>
          <div class="single_detail">
            <p>Bonus program</p>
            <h3>Premium</h3>
          </div>
          <div class="single_detail">
            <p>Insurance</p>
            <h3>Enabled</h3>
          </div>
        </div>

        <div class="button-wrap">
          <div class="button">
            <img src="/assets/icons/convert.svg" alt="icon" />
            <h4>Update your details</h4>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
