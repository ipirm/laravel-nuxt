<template>
    <div class="container-fluid main-swiper">
        <div class="container">
            <p v-if="loggedIn">
                Hello {{ user.name }}
            </p>
            <p v-if="!loggedIn">
                Please sign in
            </p>
        </div>
        <div class="row">
            <div v-swiper:mainSwiper="swiperOption">
                <div class="swiper-wrapper">
                    <div
                            class="swiper-slide"
                            v-for="(banner,index) in banners"
                            :key="index"
                            :style="{ backgroundImage: `url('${banner}')` }"
                    >
                    </div>
                </div>
            </div>
            <div class="main-swiper-card">
                <div class="main-swiper-card-header">
                    <span>Tviser - Найди работу своей мечты!</span>
                </div>
                <div class="main-swiper-card-body">
                    <input type="text" placeholder="Услуга или специалист">
                    <a href="#" class="main-swiper-btn">
                        <span>Приступить</span>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

    export default {
        data() {
            return {
                banners: [
                    '/images/main-page/bgMainPage.png',
                    '/images/main-page/bgMainPage.png',
                    '/images/main-page/bgMainPage.png',
                ],
                swiperOption: {
                    loop: true,
                    slidesPerView: 'auto',
                    centeredSlides: true,
                    spaceBetween: 30,
                    effect: 'fade',
                }
            }
        },
    }
</script>

