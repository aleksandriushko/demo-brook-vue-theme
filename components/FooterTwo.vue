<template>
    <footer class="page-footer bg_color--3 pl--150 pr--150 pl_lg--30 pr_lg--30 pl_md--30 pr_md--30 pl_sm--5 pr_sm--5">
        <!-- Start Footer Top Area -->
        <div class="bk-footer-inner pt--150 pt_sm--100">
            <div class="container">
                <div class="row">
                    <div class="col-lg-4 col-sm-6">
                        <div class="footer-widget text-var--2">
                            <div class="logo">
                                <n-link to="">
                                    <img :src="$router.options.base+'images/app/logo-white.svg'" alt="brand logo">
                                </n-link>
                            </div>
                            <div class="footer-inner">
                                <p>Yolo is a creative agency that helps businesses grow by creating brand experiences with soul. We take inspiration from film, art, music and sports and turn it into marketing that makes an impact.</p>
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-2 col-sm-6 mt_mobile--40">
                        <div class="footer-widget text-var--2 menu--about">
                            <h2 class="widgettitle">Learn more</h2>
                            <div class="footer-menu">
                                <ul class="ft-menu-list bk-hover">
                                    <li>
                                        <n-link to="/">Home</n-link>
                                    </li>
                                    <li>
                                        <n-link to="/about-u">About Us</n-link>
                                    </li>
                                    <li>
                                        <n-link to="/services">Services</n-link>
                                    </li>
                                    <li>
                                        <n-link to="/portfolio">Portfolio</n-link>
                                    </li>
                                    <li>
                                        <n-link to="/press">Press</n-link>
                                    </li>
                                    <li>
                                        <n-link to="/blog">Blog</n-link>
                                    </li>
                                    <li>
                                        <n-link to="/contact-us">Contact Us</n-link>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-3 col-sm-6 mt_md--40 mt_sm--40">
                        <div class="footer-widget text-var--2 menu--contact">
                            <h2 class="widgettitle">Contact</h2>
                            <div class="footer-address">
                                <div class="bk-hover">
                                    <p><strong>Atlanta</strong></p>
                                    <p class="fw-200">
                                        4279 Roswell Rd NE<br>
                                        STE 208-194<br>
                                        Atlanta, GA 30342<br>
                                        678.590.0834
                                    </p>
                                    <p class="mt--10"><strong>Cleveland</strong></p>
                                    <p class="fw-200">
                                        13500 Pearl Road<br>
                                        Suite 139-344<br>
                                        Strongsville, OH 44136<br>
                                        216.352.6768
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-3 col-sm-6 mt_md--40 mt_sm--40">
                        <div class="footer-widget text-var--2 menu--instagram">
                            <h2 class="widgettitle">Instagram</h2>
                            <div class="ft-instagram-list">
                                <div class="instagram-grid-wrap">
                                    <div class="item-grid grid-style--1" v-for="instagram in instagramPosts" :key="instagram.id">
                                        <div class="thumb">
                                            <n-link to="">
                                                <img :src="instagram.image" alt="instagram image">
                                            </n-link>
                                            <div class="item-info">
                                                <div class="inner">
                                                    <n-link to="">
                                                        <i class="fas fa-heart"></i>
                                                        {{ instagram.like }}
                                                    </n-link>
                                                    <n-link to="">
                                                        <i class="fas fa-comment-dots"></i>
                                                        {{ instagram.comment }}
                                                    </n-link>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="social-share social--transparent text-white mt--40">
                                <a href="https://www.facebook.com/" target="_blank">
                                    <i class="fab fa-facebook"></i>
                                </a>
                                <a href="https://twitter.com/" target="_blank">
                                    <i class="fab fa-twitter"></i>
                                </a>
                                <a href="https://www.instagram.com/" target="_blank">
                                    <i class="fab fa-instagram"></i>
                                </a>
                                <a href="https://dribbble.com/" target="_blank">
                                    <i class="fab fa-dribbble"></i>
                                </a>
                                <a href="https://www.pinterest.com/" target="_blank">
                                    <i class="fab fa-pinterest"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- Start Footer Top Area -->

        <!-- Start Copyright Area -->
        <div class="copyright ptb--50 text-var-2">
            <div class="container">
                <div class="row align-items-center">
                    <div class="col-md-6">
                        <div class="copyright-left text-md-left text-center">
                            <ul class="bk-copyright-menu d-flex bk-hover justify-content-center justify-content-md-start flex-wrap flex-sm-nowrap">
                                <li class="d-flex">
                                    <n-link to="/blog">Our Blogs</n-link>
                                </li>
                                <li class="d-flex">
                                    <n-link to="/portfolio">Latest Projects</n-link>
                                </li>
                                <li class="d-flex">
                                    <n-link to="/contact-us">Contact Us</n-link>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="copyright-right text-md-right text-center">
                            <p>@2021 Digital Yalo, All rights reserved</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- End Copyright Area -->
    </footer>
</template>

<script>
    export default {
        data () {
            return {
                instagramPosts: [
                    {
                        "id": 1,
                        "image": this.$router.options.base+"img/instagram/instagram-1.jpg",
                        "like": "1K",
                        "comment": "8"
                    },
                    {
                        "id": 2,
                        "image": this.$router.options.base+"img/instagram/instagram-2.jpg",
                        "like": "6K",
                        "comment": "9"
                    },
                    {
                        "id": 3,
                        "image": this.$router.options.base+"img/instagram/instagram-3.jpg",
                        "like": "3K",
                        "comment": "4"
                    },
                    {
                        "id": 4,
                        "image": this.$router.options.base+"img/instagram/instagram-4.jpg",
                        "like": "1K",
                        "comment": "3"
                    },
                    {
                        "id": 5,
                        "image": this.$router.options.base+"img/instagram/instagram-5.jpg",
                        "like": "2K",
                        "comment": "7"
                    },
                    {
                        "id": 6,
                        "image": this.$router.options.base+"img/instagram/instagram-6.jpg",
                        "like": "1K",
                        "comment": "8"
                    }
                ]
            }
        }
    };
</script>