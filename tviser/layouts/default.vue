<template>
    <div>
        <div v-if="!active">
            <div class="preloader">
                <div class="logo">
                    <svg-icon name="logo" style="width:126px;height:33px"/>
                </div>
            </div>
        </div>
        <div v-if="active">
            <PageTransitioner/>
            <nuxt-link :to="switchLocalePath('en')">English</nuxt-link>
            <nuxt-link :to="switchLocalePath('ru')">Russian</nuxt-link>
            <Header/>
            <nuxt/>
            <Footer/>
        </div>
    </div>
</template>

<script>
    import Header from "../components/global/Header";
    import Footer from "../components/global/Footer";
    import PageTransitioner from '../components/PageTransitioner'

    export default {
        components: {Footer, Header, PageTransitioner},
        data() {
            return {
                active: false
            }
        },
        mounted() {
            if (process.browser) {
                window.onNuxtReady((app) => {
                    this.active = !this.active;
                })
            }
        }
    }
</script>


