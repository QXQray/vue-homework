<template>
  <div class="w-full max-w-[600px]">
    <div class="bg-surface-container-lowest p-8 rounded-xl shadow-[0_32px_64px_-12px_rgba(0,0,0,0.04)] border border-outline-variant/20">
      
      <form @submit.prevent="handleLogin" class="space-y-4">
        <div class="space-y-1">
          <span class="text-lg font-body text-on-surface font-semibold">系統登入</span>
        </div>

        <div class="space-y-1">
          <input 
            v-model="account"
            class="w-full px-4 py-4 border-b-2 border-outline rounded-full focus:border-primary outline-none" 
            placeholder="電子郵件或手機號碼" 
            type="text"
          />
        </div>
        
        <div class="space-y-1">
          <input 
            v-model="password"
            class="w-full px-4 py-4 border-b-2 border-outline rounded-full focus:border-primary outline-none" 
            placeholder="密碼" 
            type="password"
          />
        </div>
        
        <button class="w-full py-4 bg-blue-600 text-white font-bold rounded-full" type="submit">
          登入
        </button>
      </form>

    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

// 宣告響應式變數來儲存使用者輸入的資料
const account = ref('')
const password = ref('')

// 處理登入邏輯的方法
const handleLogin = () => {
  console.log('嘗試登入的帳號:', account.value)
  console.log('嘗試登入的密碼:', password.value)
  // 這裡未來可以串接後端 API
}
</script>