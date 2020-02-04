<template>
    <div class="container header-container">
        <div class="row">
            <a :href="localePath('/')" class="logo" @click.prevent="$bus.goTo('/',$router,localePath)">
                <svg-icon name="logo" style="width:126px;height:33px"/>
            </a>
            <input type="text" placeholder="Search for employee">
            <div class="header-nav">
                <nuxt-link class="header-nav-link" to="/">Работники</nuxt-link>
                <a class="header-nav-link" :href="localePath('/orders')" @click.prevent="$bus.goTo('/orders',$router,localePath)">
                    Заказы
                </a>
                <nuxt-link class="header-nav-link" v-if="!loggedIn" to="/login">Вход</nuxt-link>
                <a href="#" class="header-nav-link" v-if="loggedIn" @click.prevent="logout">Выйти</a>
                <nuxt-link class="header-nav-link" v-if="!loggedIn" to="/register">/ Регестрация</nuxt-link>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        methods: {
            logout() {
                this.$auth.logout();
            }
        }
    }
</script>

<style scoped>

</style>
