<script setup lang="js">
import { Logo } from '@/assets/logo'
import { ButtonPrimary } from '@/components/buttons'
import { Navigation } from '@/components'

const navigations = [
  {
    loc: '#landing',
    name: 'Product',
  },
  {
    loc: '#steps',
    name: 'Steps',
  },
  {
    loc: '#features',
    name: 'Features',
  },
  {
    loc: '#statistics',
    name: 'Achievement',
  },
]
</script>

<template>
  <header>
    <nav class="flex py-2 px-10 md:px-36 m-auto justify-between w-full bg-white fixed right-0 top-0">    
      <div class="flex m-1">
        <a href="#">
          <img :src="Logo" width="160" alt="logo">
        </a>
      </div>
      <div class="flex justify-between">
        <Navigation
          v-for="navigate in navigations"
          :loc="navigate.loc"
          :name="navigate.name"
        />
      </div>
      <div>
        <ButtonPrimary text="Login" type="outline" />
        <ButtonPrimary text="Sign Up" />

        <!-- 
        <RouterLink to="/login" class="p-1 m-2 font-medium text-gray-700">Login</RouterLink>
        <RouterLink to="/register" class="py-2 px-4 bg-teal-500 text-white rounded-xl font-medium hover:bg-teal-700 transition-colors">Sign Up</RouterLink> 
        -->
      </div>
    </nav>
  </header>
</template>