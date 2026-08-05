<template>
  <div class="fixed inset-0 z-50 flex items-center justify-center p-4 sm:p-0">
    <!-- Modal Container -->
    <div class="w-full max-w-[380px] bg-white border border-[#e5e5e5] rounded-2xl overflow-hidden shadow-lg max-h-[90vh] flex flex-col">
      <!-- Modal Header -->
      <div class="flex justify-between items-center px-6 py-5 pb-4 border-b border-[#e5e5e5]">
        <h1 class="text-sm font-medium text-[#171717] leading-6">Bagikan Link Checkout</h1>
        <button class="bg-transparent border-0 p-0 cursor-pointer flex items-center justify-center w-6 h-6 text-[#171717] transition-opacity hover:opacity-60" @click="onClose">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M18 6L6 18M6 6L18 18" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>
      </div>

      <!-- Modal Body -->
      <div class="px-6 py-5 flex flex-col gap-4 overflow-y-auto flex-1">
        <!-- URL Input Container -->
        <div class="flex items-center bg-[#f9fafb] border border-[#e5e5e5] rounded-xl p-3 sm:p-4">
          <input
            type="text"
            :value="checkoutUrl"
            readonly
            class="flex-1 bg-transparent text-sm font-normal text-[#171717] focus:outline-none truncate"
          />
          <button class="ml-auto flex-shrink-0 px-4 py-2 bg-[#1f1f54] text-white text-sm font-medium rounded-md transition-all hover:bg-[#171645] active:bg-[#0f0e32]">
            {{ copied ? 'Disalin' : 'Salin' }}
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const emit = defineEmits<{
  close: []
}>();

const copied = ref(false)
const checkoutUrl = ref('api.dev.useflik.com/shortener/3WLh6H')

const onClose = () => {
  emit('close');
};

const copyLink = async () => {
  try {
    await navigator.clipboard.writeText(checkoutUrl.value)
    copied.value = true
    setTimeout(() => {
      copied.value = false
    }, 2000)
  } catch (err) {
    console.error('Failed to copy:', err)
  }
}
</script>
