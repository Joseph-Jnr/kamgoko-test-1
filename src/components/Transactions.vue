<script setup>
import { ref } from 'vue'

const trxList1 = ref([
  {
    title: 'Online purchase',
    amount: '- $10.480,00',
    date: '28 Aug, 3:00 PM',
  },
  {
    title: 'ATM Cash withdrawal',
    amount: '- $201.50',
    date: '28 Aug, 2:15 AM',
  },
  {
    title: 'Online purchase',
    amount: '- $184.00',
    date: '28 Aug, 5:40 PM',
  },
  {
    title: 'Monthly home rent',
    amount: '- $400.00',
    date: '24 Aug, 1:00 AM',
  },
])

const trxList2 = ref([
  {
    title: 'Income payment',
    amount: '+ $3.000,00',
    date: '24 Aug, 6:20 PM',
  },
  {
    title: 'Groceries store',
    amount: '- $400.00',
    date: '24 Aug, 1:00 AM',
  },
  {
    title: 'Monthly home rent',
    amount: '- $400.00',
    date: '24 Aug, 1:00 AM',
  },
  {
    title: 'Online purchase',
    amount: '- $396,00',
    date: '28 Aug, 2:00 PM',
  },
])
</script>

<template>
  <div class="transactions">
    <div class="trx_mobile_header">
      <h2>Latest transactions</h2>
    </div>
    <div class="trx_group">
      <div class="trx_date">
        <p>28 August</p>
      </div>
      <div class="trx_list">
        <div class="single_trx" v-for="(item, index) in trxList1" :key="index">
          <div class="details">
            <div class="image">
              <img src="/assets/img/bw_grid.png" width="32" alt="placeholder" />
            </div>
            <div class="text">
              <h4>{{ item.title }}</h4>
              <p>{{ item.date }}</p>
            </div>
          </div>
          <div class="amount">
            <h4>{{ item.amount }}</h4>
          </div>
        </div>
      </div>
    </div>

    <div class="trx_group mt-5">
      <div class="trx_date">
        <p>24 August</p>
      </div>
      <div class="trx_list">
        <div class="single_trx" v-for="(item, index) in trxList2" :key="index">
          <div class="details">
            <div class="image">
              <img src="/assets/img/bw_grid.png" width="32" alt="placeholder" />
            </div>
            <div class="text">
              <h4>{{ item.title }}</h4>
              <p>{{ item.date }}</p>
            </div>
          </div>
          <div class="amount">
            <h4>{{ item.amount }}</h4>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
