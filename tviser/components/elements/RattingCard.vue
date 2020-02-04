<template>
    <div class="ratting-card">
        <div class="ratting-card-header">
            <img src="/images/main-page/ilham.png">
            <div class="ratting-card-header-right">
                <span>Ilham Pirmammadov</span>
                <span class="ratting-card-job">Front-end разработчик</span>
                <div class="ratting-card-crown">
                    <img src="/images/icons/crown.svg">
                    <span>Top rated</span>
                </div>
            </div>
        </div>
        <div class="ratting-card-body">
            <span class="ratting-card-left">Baku, Azerbaijan</span>
            <span class="ratting-card-right">$15 / hr</span>
        </div>
        <div class="ratting-card-work">
            <div class="ratting-card-work-item" v-for="index in 6" :key="index">
                <div class="ratting-card-work-item-exp">
                    <span>Javascript</span>
                </div>
            </div>
        </div>
        <div class="ratting-card-show">
            <a href="#" @click.prevent>Смотреть все</a>
        </div>
        <div class="ratting-card-footer">
            <a class="ratting-card-btn" :href='localePath(`/profile/${id}`)'
               @click.prevent="$bus.goTo(`/profile/${id}`,$router,localePath)">
                <span>Показать профиль</span>
            </a>
        </div>
    </div>

</template>

<script>
    export default {
        props: {
            id: Number,
        },
        data() {
            return {}
        },
        mounted() {
        }
    }
</script>

