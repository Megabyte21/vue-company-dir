<script setup>
import { ref } from "vue";
<<<<<<< HEAD
import { useAuth } from '@/composables/useAuth'

const { isAuthenticated, logout, user } = useAuth()
const brand = ref(import.meta.env.VITE_APP_NAME)
=======
const brand = ref('🏢 Fake Company Directory')
>>>>>>> parent of a829e77 (Added more funcitons to the main and added login)
</script>


<template>
    <nav>
        <div class="wrapper">
            <div class="brand">
                <span class="brand-title">{{ brand }}</span>
            </div>
            <div class="menu">
<<<<<<< HEAD
                <p v-show="isAuthenticated" class="px-2 py-4 mx-2">Welcome back <strong><i>{{ user?.email }}</i></strong></p>
                <div v-if="isAuthenticated">
                <RouterLink :to="{ name: 'Settings' }" class="menu-item">Settings</RouterLink>
                <RouterLink :to="{ name: 'Login'}" @click="logout" class="menu-logout">Logout</RouterLink>
                </div>
                <div v-else>
                <RouterLink :to="{ name: 'Login'}" class="menu-login">Login</RouterLink>
                </div>
=======
                <a href="#" class="menu-item">Departments</a>
                <a href="#" class="menu-item">Settings</a>
                <a href="#" class="menu-login">Logout</a>
>>>>>>> parent of a829e77 (Added more funcitons to the main and added login)
            </div>
        </div>
    </nav>
</template>

<style scoped lang="postcss">
    nav {
    @apply h-20 bg-slate-900 text-slate-200 flex items-center justify-between;
    }
    .wrapper {
        @apply container flex items-center justify-between mx-auto w-full;
    }
    .brand {
        &-title {
            @apply text-2xl font-bold text-yellow-500;
        }
    }
    .menu{
        @apply flex gap-2;
        &-item {
            @apply rounded-md px-4 py-2 hover:bg-yellow-500 hover:text-slate-900;
        }
        &-login {
            @apply rounded-md bg-red-500 px-4 py-2 text-red-100 hover:bg-red-700;
        }
    }
</style>