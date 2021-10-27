<template>
    <fixed-header>
        <header class="br_header header-default header-bar position-from--top black-logo--version haeder-fixed-width haeder-fixed-150 headroom--sticky header-mega-menu clearfix" :class="addClass">
            <div class="container-fluid">
                <div class="row">
                    <div class="col-12">
                        <div class="header__wrapper">
                            <!-- Header Left -->
                            <div class="header-left">
                                <div class="logo">
                                    <n-link to="">
                                        <img :src="$router.options.base+'images/app/logo-orange.svg'" alt="Brook Logo">
                                    </n-link>
                                </div>
                            </div>

                            <!-- Header Right -->
                            <div class="header-right">
                                <!-- Start Popup Search Wrap -->
                                <div class="popup-search-wrap">
                                    <a class="btn-search-click" href="javascript:void(0)" @click="toggleClass('addClass', 'search-popup-open')">
                                        <i class="fa fa-search"></i>
                                    </a>
                                </div>
                                <!-- End Popup Search Wrap -->

                                <!-- Start Hamberger -->
                                <div class="manu-hamber hamberger-trigger black-version d-none d-xl-block" @click="togglePopupMenu('addClass', 'is-visiable')">
                                    <div>
                                        <i></i>
                                    </div>
                                </div>
                                <!-- End Hamberger -->

                                 <!-- Start Hamberger -->
                                 <div class="manu-hamber popup-mobile-click d-block black-version d-block d-xl-none" @click="mobiletoggleClass('addClass', 'show-mobile-menu')">
                                    <div>
                                        <i></i>
                                    </div>
                                </div>
                                <!-- End Hamberger -->

                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </header>
    </fixed-header>
</template>

<script>
    import FixedHeader from 'vue-fixed-header'
    import Navigation from '@/components/Navigation';

    export default {
        components: {
            FixedHeader,
            Navigation
        },

        props: ['addClass'],

        methods: {
            //offcanvas search 
            toggleClass(addRemoveClass, className) {
                const el = document.querySelector('#search-popup');
                if (addRemoveClass === 'addClass') {
                    el.classList.add(className);
                } else {
                    el.classList.remove(className);
                }
            },

            // popup fullscreen menu
            togglePopupMenu(addRemoveClass, className) {
                const el = document.querySelector('#popup-fullscreen-menu');
                if (addRemoveClass === 'addClass') {
                    el.classList.add(className);
                } else {
                    el.classList.remove(className);
                }
            },

            // offcanvas mobilemenu open
            mobiletoggleClass(addRemoveClass, className) {
                const el = document.querySelector('#offcanvas-menu');
                if (addRemoveClass === 'addClass') {
                    el.classList.add(className);
                } else {
                    el.classList.remove(className);
                }
            },
        },
    };
</script>

<style lang="scss" scoped>
    .vue-fixed-header--isFixed {
        top: 0;
        left: 0;
        width: 100%;
        z-index: 999;
        position: fixed !important;
        background-color: rgba($white, 0.9);
        box-shadow: 0 0 8px 1px rgba(0, 0, 0, 0.2);
        animation: 900ms cubic-bezier(0.2, 1, 0.22, 1) 0s normal none 1 running fadeInDown;
        padding-top: 0 !important;
    }
</style>