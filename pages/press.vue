<template>
    <div class="main-container">

        <HeaderAbout />

        <OffCanvasMobileMenu />

        <SearchPopup />

        <div class="brook-breadcrumb-area pt--130 pb--170 bg_color--1 breadcrumb-title-bar">
            <div class="container-fluid plr--150 plr_md--50 plr_sm--50">
                <div class="row">
                    <div class="col-lg-12">
                        <div class="breadcrumb-inner text-center">
                            <h1 class="heading heading-h1 line-height-1-5">Press<span class="theme-color">.</span></h1>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="brook-service-list-area">
            <div class="bk-service-list d-block d-md-flex mb--70 align-items-center wow move-up" v-for="service in serviceList" :key="service.i">
                <div class="thumb">
                    <img class="w--100" :src="service.image" :alt="service.alt">
                </div>
                <div class="content plr--130 plr_md--50 plr_sm--40">
                    <h3 class="heading heading-h3">{{ service.title }}</h3>
                    <div class="bkseparator--35"></div>
                    <p class="bk_pra">{{ service.desc }}</p>
                </div>
            </div>
        </div>

        <WhatNext />

        <FooterTwo />

    </div>
</template>

<script>
    export default {
        components: {
            HeaderAbout: () => import('@/components/custom/HeaderAbout'),
            OffCanvasMobileMenu: () => import('@/components/OffCanvasMobileMenu'),
            SearchPopup: () => import('@/components/SearchPopup'),
            WhatNext: () => import('@/components/custom/WhatNext'),
            FooterTwo: () => import('@/components/FooterTwo'),
        },

        data () {
            return {
                "serviceList": [
                    {
                        "image": `${this.$router.options.base}img/service/modern/service-list-1.jpg`,
                        "alt": "service image",
                        "title": "Atlanta Marketing Agency Yalo! Acquires Creative Brand Agency My Friend’s Nephew",
                        "desc": "ATLANTA — August 31, 2021 — Award-winning, full-service marketing agency Yalo! announces its acquisition of creative brand agency, My Friend’s Nephew. This is the second acquisition in Yalo!’s growth strategy to gain new services and skills, building on the existing capabilities for the agency, over the next 24 to 36 months.  Since 2015, Atlanta-based, My Friend’s Nephew has delivered successful marketing..."
                    },
                    {
                        "image": `${this.$router.options.base}img/service/modern/service-list-2.jpg`,
                        "alt": "service image",
                        "title": "Digital Yalo Announced as a Top Atlanta Creative Agency by UpCity!",
                        "desc": "ATLANTA — June 23, 2021 — Digital Yalo announces that it has been recognized as one of the top creative agencies in Atlanta and nationally by UpCity. Yalo prides itself on being different from the average creative agency by leveraging its unique creative approach to elevate clients’ brands. Yalo’s “Soul Song” creative process helps clients grab attention and..."
                    },
                    {
                        "image": `${this.$router.options.base}img/service/modern/service-list-3.jpg`,
                        "alt": "service image",
                        "title": "Yalo Scores Gold at 19th Annual Horizon Interactive Media Awards",
                        "desc": "ATLANTA, Georgia – June 8, 2021 — The Horizon Interactive Awards, a leading international interactive media awards competition, has announced the 2020 award winners showcasing this year’s “best of the best” in interactive media production. This year, Yalo was recognized for its excellence with 7 awards.  The 2020 competition saw over 600 entries from around..."
                    },
                    {
                        "image": `${this.$router.options.base}img/service/modern/service-list-3.jpg`,
                        "alt": "service image",
                        "title": "Yalo Named A Cobb Chamber 2021 Top 30 Small Business of the Year",
                        "desc": "ATLANTA — April 27, 2021  FOR IMMEDIATE RELEASE Award-winning, creative agency Digital Yalo named a Top 30 Small Business of The Year by The Cobb Chamber of Commerce for the 3rd consecutive year. Yalo is the only marketing firm named in the Top 30 and will compete for Small Business of the Year. “In these unprecedented..."
                    },
                    {
                        "image": `${this.$router.options.base}img/service/modern/service-list-3.jpg`,
                        "alt": "service image",
                        "title": "Digital Yalo Adds 100th Client",
                        "desc": "ATLANTA, Georgia – December 8, 2020. Beginning as a one-man shop just eight years ago, creative marketing & design agency Yalo continues to grow during a very challenging time for many in the marketing & advertising industries. Signing its 100th client in November, the digital & analog agency has also added to its internal roster..."
                    },
                    {
                        "image": `${this.$router.options.base}img/service/modern/service-list-3.jpg`,
                        "alt": "service image",
                        "title": "Digital Yalo and FullStory Partner to Deliver Best-in-Class Digital Experiences",
                        "desc": "ATLANTA, Georgia – October 27, 2020 Award-winning, creative agency Digital Yalo announces a new partnership with digital experience analytics platform FullStory.  This strategic partnership employs FullStory’s powerful digital experience platform to deliver exceptional customer experiences. Through Fullstory’s measurement and conversion rate optimization tools, Yalo can help their clients grasp the “why” and the “what” to..."
                    },
                    {
                        "image": `${this.$router.options.base}img/service/modern/service-list-3.jpg`,
                        "alt": "service image",
                        "title": "Digital Yalo’s Virtual Trade Shows Platform Gains Online Ground",
                        "desc": "FOR IMMEDIATE RELEASE What began as a pivot is now a solid stance for many companies. As more businesses look for ways to connect with and sell to consumers in this time of social distancing, Yalo’s Virtual Events platform continues to gain ground.  Yalo’s Virtual Events platform began as clients found themselves facing canceled trade..."
                    },
                    {
                        "image": `${this.$router.options.base}img/service/modern/service-list-3.jpg`,
                        "alt": "service image",
                        "title": "Digital Yalo and InVision Partner to Create Design System Managers",
                        "desc": "Living, Scalable Solutions for Corporate Brand Elevation FOR IMMEDIATE RELEASE ATLANTA, Georgia—August 12, 2020 Award-winning, creative agency Digital Yalo announces a new partnership with digital product design platform company InVision. This robust union formalizes Yalo’s support for InVision’s new Design System Manager (DSM) solution to clients.   The InVision DSM platform enables designers anywhere in..."
                    },
                    {
                        "image": `${this.$router.options.base}img/service/modern/service-list-3.jpg`,
                        "alt": "service image",
                        "title": "Yalo Wins Top 25 Small Business Award",
                        "desc": "FOR IMMEDIATE RELEASE ATLANTA, Georgia—July 6, 2020   Award-winning, creative agency Digital Yalo named a Top 25 Small Business by The Cobb Chamber of Commerce for the 2nd year in a row. Cobb County is a growth county in Atlanta, where Yalo is a Chairman’s Circle member of the Chamber of Commerce. Established in 1982, the Small Business..."
                    },
                    {
                        "image": `${this.$router.options.base}img/service/modern/service-list-3.jpg`,
                        "alt": "service image",
                        "title": "Yalo Activates Its Growth Strategy",
                        "desc": "ATLANTA, Georgia—June 8, 2020  Award-winning, creative marketing agency Digital Yalo announces acquisition of Ninja Multimedia. The Ninja acquisition signals the activation of Yalo’s growth strategy through acquisitions and new technology partnerships over the next 24 to 36 months. Based in Atlanta, Ninja has worked with clients such as Georgia Lottery, Arby’s, and brings an arsenal..."
                    }
                ]
            }
        },

        mounted () {
            document.body.classList.add('template-color-5', 'template-font-1')
        },

        head() {
            return {
                title: 'Brook || Service List'
            }
        },
    };
</script>