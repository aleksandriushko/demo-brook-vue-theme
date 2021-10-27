<template>
    <div class="hero-essential-area swiper-arrow-hover">
        <swiper :options="swiperOption">
            <div class="swiper-slide" v-for="slider in sliders" :key="slider.id">
                <div class="hero-essential-slide bg-cover slider-right-bg" :style="{backgroundImage: `url(${slider.bgImage})`}">
                    <div class="container">
                        <div class="row">
                            <div class="col-6 slider-right-bg">
                                <div class="hero-content">
                                    <h2 class="hero-title" v-html="slider.heading">{{ slider.heading }}</h2>
                                    <h5>{{ slider.subHeading }}</h5>
                                    <n-link v-if="slider.id !== 1" to="/" class="btn-essential">Learn More</n-link>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </swiper>
        <!-- slider arrow navigation -->
        <div class="ht-swiper-button ht-swiper-button-prev">
            <i class="ion ion-ios-arrow-back"></i>
        </div>
        <div class="ht-swiper-button ht-swiper-button-next">
            <i class="ion ion-ios-arrow-forward"></i>
        </div>
    </div>
</template>

<script>
    export default {
        data () {
            return {
                swiperOption: {
                    loop: true,
                    speed: 1000,
                    navigation: {
                        nextEl: '.ht-swiper-button-next',
                        prevEl: '.ht-swiper-button-prev'
                    },
                },
                sliders: [
                    {
                        id: 1,
                        // heading: "A platform migration across 50 sites.",
                        // subHeading: "B&G Foods",
                        bgImage: `${this.$router.options.base}images/slider/hero-slide-5.jpeg`
                    },
                    {
                        id: 2,
                        heading: "The virtual show must go on",
                        subHeading: "Imperial Distributors",
                        bgImage: `${this.$router.options.base}images/slider/hero-slide-6.jpeg`
                    },
                    {
                        id: 3,
                        heading: "Creating vital spaces",
                        subHeading: "Sodexo",
                        bgImage: `${this.$router.options.base}images/slider/hero-slide-7.jpeg`
                    },
                ]
            }
        }
    };
</script>

<style lang="scss" scoped>
    .hero-essential-slide {
        background-size: cover;
        // background-position: right;

        height: 650px;
        display: flex;
        align-items: center;
        position: relative;
        // res
        @media #{$md-layout}{
            height: 600px;
        }
        @media #{$sm-layout}{
            height: 550px;
        }
        @media #{$small-mobile}{
            height: 450px;
        }
        .hero-content {
            max-width: 500px;
            .hero-title {
                font-size: 48px;
                font-weight: 300;
                // res
                @media #{$sm-layout}{
                    font-size: 40px;
                }
                @media #{$small-mobile}{
                    font-size: 32px;
                }
            }
            h5 {
                color: #777;
                font-size: 20px;
                font-weight: 300;
                line-height: 1.2;
                margin-bottom: 40px;
                // res
                @media #{$sm-layout}{
                    color: #444;
                }
                @media #{$small-mobile}{
                    margin-top: 15px;
                    line-height: 1.5;
                }
            }
        }
    }
    .hero-essential-area {
        .ht-swiper-button {
            color: $black;
            font-size: 30px;
            left: 70px;
            width: 68px;
            height: 68px;
            line-height: 68px;
            border-radius: 50%;
            text-align: center;
            background-color: $white;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.01);
            &-next {
                right: 70px;
                left: auto;
            }
        }
    }
    .slider-right-bg:after {
        content: '';
        height: 140vh;
        max-height: 1060px;
        margin-top: -25px;
        width: 22vh;
        max-width: 180px;
        background-image: url(/demo-brook-vue-theme/images/app/slider-right-bg.svg);
        background-size: cover;
        background-repeat: no-repeat;
        left: 47%;
        position: absolute;
        z-index: 2;
    }
</style>