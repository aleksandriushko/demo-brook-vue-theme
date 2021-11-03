<template>
    <div class="main-container">

        <HeaderBlack />

        <OffCanvasMobileMenu />

        <SearchPopup />

        <div class="breadcaump-area pt--260 pt_md--200 pt_sm--150 pb--160 pb_sm--100 bg_color--18 breadcaump-title-bar breadcaump-title-white">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12">
                        <div class="breadcaump-inner text-center">
                            <div class="breadcrumb-insite">
                                <div class="header mb--40 text-center">
                                    <h3 class="heading heading-h3 font-32 text-white">{{ data.title }}</h3>
                                    <div class="post-meta mt--20 text-white bk-hover align-items-center d-flex justify-content-center">
                                        <div class="post-date">{{ data.date }}</div>
                                        <div class="post-category">
                                            <n-link to="/">{{ data.category }}</n-link>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Start Blog Details -->
        <div class="brook-blog-details-area space_dec--100 pt_md--80 pt_sm--80">
            <div class="container">
                <div class="row mb--85">

                    <div class="col-lg-12">
                        <div class="blog-modern-layout">
                            <div class="thumbnail mb--60">
                                <img class="w-100" :src="data.image" alt="Multipurpose">
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-2 order-2 order-lg-1 mt_md--40 mt_sm--40">
                        <div class="blog-post-return-button">
                            <button><i class="fa fa-arrow-left"></i> Back</button>
                        </div>
                    </div>
                    <div class="col-lg-8 order-1 order-lg-2">
                        <div class="blog-details-wrapper">
                            <article class="blog-post blog-modern-layout">
                                <!-- Start Content -->
                                <div class="content basic-dark2-line-1px pb--50 mb--35">
                                    <div class="inner">
                                        <h5 class="heading heading-h5 line-height-1-95 wow move-up">
                                            Social Media Returns</h5>
                                        <div class="desc mt--45 mb--50">
                                            <p class="bk_pra wow move-up">Anticipation is high for the payback on social marketing investments. The verdict is out for capturing any quantifiable results. A recent CMO poll cosponsored by Duke Business School and Deloite Touche indicates even with an average of 13% of marketing dollars being spent on social marketing only 30% of the respondents indicating that they have shown quantifiable value. Pressure will increase significantly to show value with social marketing estimated to grow to 21.5 % of the marketing budget over the next five years.</p>
                                        </div>
                                    </div>
                                    <div class="thumbnail wow move-up">
                                        <img class="w-100" :src="data.image3" alt="Multipurpose">
                                    </div>
                                    <div class="desc mt--45">
                                        <h5 class="heading heading-h5 line-height-1-95 wow move-up">
                                            Social Media Value – Lagging Indicators
                                        </h5>
                                    </div>
                                    <div class="mt--20">
                                        <p class="bk_pra wow move-up">To achieve quantifiable benefit, social media must deliver outcomes with business value. Social media must facilitate the journey through the marketing funnel, for users, customers, and clients. For eCommerce, the outcome is a loaded shopping cart and commitment to buy. For concerns, offering services and/or building brand image, it is attracting eyeballs “from the wild,” and migrating from reach/impressions to followers. Using tools like, Google Analytics, progress is tracked using lagging indicators. The intent is to determine what was an effective post, but resorts instead, to just comparing summary statistics for a given time period. This can show that the process is directionally correct but:</p>
                                    </div>
                                    <div class="bk-list--2 mt--20 move-up wow">
                                        <div class="list-header">
                                            <div class="marker with-dot"></div>
                                            <div class="title-wrap">
                                                <h6 class="heading heading-h5">No detailed data exists on how the how the post-performance was attained</h6>
                                            </div>
                                        </div>
                                        <div class="list-header">
                                            <div class="marker with-dot"></div>
                                            <div class="title-wrap">
                                                <h6 class="heading heading-h5">No clear direction on how to maintain or change or change course for the future</h6>
                                            </div>
                                        </div>
                                    </div>

                                    <p class="bk_pra wow move-up mt--20">Even sentiment analysis has focused on what has happened. It is used to sense public opinion from social media posts or internal customer issue tracking or product feature feedback.  Companies use sentiment analysis to gain insights so they can provide differentiated services, valued product designs, frictionless user experiences and refined business processes. Sentiment analysis is used to determine the predilection or opinions of the author. But again, this is something that has already happen, which is like, “trying to drive a car by looking in the rear-view mirror.”</p>

                                    <div class="thumbnail wow move-up mt--45">
                                        <img class="w-100" :src="data.image4" alt="Multipurpose">
                                    </div>
                                    <div class="desc mt--45">
                                        <h5 class="heading heading-h5 line-height-1-95 wow move-up">
                                            Sentiment Analysis – Influencing Outcomes
                                        </h5>
                                    </div>
                                    <p class="bk_pra wow move-up mt--20">Sentiment analysis can be performed using several approaches. They tend to fall either in the supervised learning or lexicon (bag of words) approaches. Supervised learning, large amount of unlabeled text is fed into algorithms. These algorithms use embedded words learn based on the coming text and develop a model which establishes the sentiment (positive, negative, or neutral) analyzing text sources including social media. Getting large amounts of text and defining the parameters for embedding terms for teaching the model are two of the challenges using this approach. </p>
                                    <p class="bk_pra wow move-up mt--20">Bag of Words uses a pre-defined lexicon. There is significant effort to build a lexicon, especially if a crowd sourcing (sending out surveys, online tools) is used. This builds a lexicon with each word being assigned a positive or negative score. The scored words with rules for addressing context and syntax define a sentiment score at the sentence and paragraph levels. This gives an overall score plus insights how the chosen words effected the sentence and or paragraph sentiment score. </p>
                                    <p class="bk_pra wow move-up mt--20">Using tools when creating all content influences the reader to continue reading, become a follower, or act. Applying sentimental analysis cannot address all the variability for social media outcomes, it is a part of the variability that you can control. Using a lexicon and consistent approach to content development will influence the audience because, the words make a difference. They make a difference because research has shown that social media with higher positive content</p>
                                    <div class="bk-list--2 mt--20 move-up wow">
                                        <div class="list-header">
                                            <div class="marker with-dot"></div>
                                            <div class="title-wrap">
                                                <h6 class="heading heading-h5">Increase the quantity of social media traffic and its speed through social media channels</h6>
                                            </div>
                                        </div>
                                        <div class="list-header">
                                            <div class="marker with-dot"></div>
                                            <div class="title-wrap">
                                                <h6 class="heading heading-h5">Used with environmental factors improves the predictability of social media diffusion</h6>
                                            </div>
                                        </div>
                                        <div class="list-header">
                                            <div class="marker with-dot"></div>
                                            <div class="title-wrap">
                                                <h6 class="heading heading-h5">Increased positive content increases social media acceptance and diffusion</h6>
                                            </div>
                                        </div>
                                        <div class="list-header">
                                            <div class="marker with-dot"></div>
                                            <div class="title-wrap">
                                                <h6 class="heading heading-h5">The Lexicon Challenge</h6>
                                            </div>
                                        </div>
                                    </div>
                                    
                                    <p class="bk_pra wow move-up mt--20">Having the “right” lexicon is the challenge when taking the supervised approach using a lexicon. How do you manage the effort of creating the “right lexicon,” by audience but not introduce bias? How do you get unbiased word scoring? How often should it be updated? Is a general one-size fits all lexicon the answer or something specific needed for each audience? What choices exist in developing or collecting public domain lexicons and developing audience specific lexicons?</p>

                                </div>
                                <!-- Start Footer -->
                                <div class="blog-footer wow move-up">
                                    <div class="row">
                                        <div class="col-lg-12 col-12">
                                            <div class="post-tag d-flex align-items-center justify-content-center">
                                                <h6 class="heading heading-h6">TAGS:</h6>
                                                <div class="blog-tag-list pl--5">
                                                    <n-link to="/blog/blog-creative">business</n-link>
                                                    <n-link to="/blog/blog-creative">format</n-link>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </article>
                        </div>
                    </div>

                </div>
            </div>
        </div>
        <!-- End Blog Details -->

        <!-- Start Pagination Area -->
        <div class="blog-modern-pagination bg_color--18 ptb--110 ptb-md--80 ptb-sm--60">
            <div class="container">
                <div class="row">
                    <div class="col-lg-8 offset-lg-2">
                        <div class="modern-pagination text-center">
                            <n-link to="/">
                                <p class="bk_pra body-color">Next</p>
                                <div class="title mt--25 mb--40">
                                    <h4 class="heading heading-h4 text-white">4 Best Ways to Keep Inspired</h4>
                                </div>
                                <span class="nav-icon fa fa-arrow-right"></span>
                            </n-link>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- End Pagination Area -->

        <!-- Start Post Comment Area -->
        <div class="blog-post-review-area bg_color--5 pt--100 pt_sm--60 pt_md--80 pb--100 pb_sm--60 pb_lg--100 pb_md--80">
            <div class="container">
                <div class="row">
                    <div class="col-lg-8 offset-lg-2">
                        <!-- Start Comment Area -->
                        <div class="comments-wrapper bg_color--1">
                            <div class="inner">
                                <h4 class="heading heading-h4">3 Comments</h4>
                                <div class="commnent-list-wrap mt--25">

                                    <!-- Start Single Comment -->
                                    <div class="comment wow move-up">
                                        <div class="thumb">
                                            <img :src="$router.options.base+'img/blog/client/client-1.jpg'" alt="Multipurpose">
                                        </div>
                                        <div class="content">
                                            <h6 class="heading heading-h6">SCOTT JAMES</h6>
                                            <div class="text mt--10 pr--50 pr_sm--5">
                                                <p class="bk_pra">To link your Facebook and Twitter accounts, open the Instagram app on your phone or tablet, and select the Profile tab in the bottom-right corner of the screen.</p>
                                            </div>
                                            <div class="comment-footer mt--10">
                                                <span>May 17, 2018 at 1:59 am</span>
                                                <span class="reply-btn">
                                                    <button>Reply</button>
                                                </span>
                                            </div>
                                        </div>
                                    </div>
                                    <!-- End Single Comment -->

                                    <!-- Start Single Comment -->
                                    <div class="comment comment-reply wow move-up">
                                        <div class="thumb">
                                            <img :src="$router.options.base+'img/blog/client/client-2.jpg'" alt="Multipurpose">
                                        </div>
                                        <div class="content">
                                            <h6 class="heading heading-h6">OWEN CHRIST</h6>
                                            <div class="text mt--10 pr--50 pr_sm--5">
                                                <p class="bk_pra">To link your Facebook and Twitter accounts, open the Instagram app on your phone or tablet, and select the Profile tab in the bottom-right corner of the screen.</p>
                                            </div>
                                            <div class="comment-footer mt--10">
                                                <span>May 17, 2018 at 1:59 am</span>
                                                <span class="reply-btn">
                                                    <button>Reply</button>
                                                </span>
                                            </div>
                                        </div>
                                    </div>
                                    <!-- End Single Comment -->

                                    <!-- Start Single Comment -->
                                    <div class="comment wow move-up">
                                        <div class="thumb">
                                            <img :src="$router.options.base+'img/blog/client/client-3.jpg'" alt="Multipurpose">
                                        </div>
                                        <div class="content">
                                            <h6 class="heading heading-h6">EDNA WATSON</h6>
                                            <div class="text mt--10 pr--50 pr_sm--5">
                                                <p class="bk_pra">To link your Facebook and Twitter accounts, open the Instagram app on your phone or tablet, and select the Profile tab in the bottom-right corner of the screen.</p>
                                            </div>
                                            <div class="comment-footer mt--10">
                                                <span>May 17, 2018 at 1:59 am</span>
                                                <span class="reply-btn">
                                                    <button>Reply</button>
                                                </span>
                                            </div>
                                        </div>
                                    </div>
                                    <!-- End Single Comment -->

                                </div>
                            </div>
                        </div>
                        <!-- End Comment Area -->

                        <!-- Start Comment Form -->
                        <div class="comment-form-wrapper">
                            <div class="header wow move-up">
                                <h4 class="heading heading-h4">Leave A Comment</h4>
                                <div class="coppent-note mt--20 mb--30">
                                    <p class="bk_pra">Your email address will not be published. Required fields are marked</p>
                                </div>
                            </div>
                            <!-- Start Contact Area -->
                            <div class="contact-form wow move-up">
                                <form>
                                    <div class="row">
                                        <div class="col-lg-12">
                                            <input type="text" placeholder="Name *">
                                        </div>

                                        <div class="col-lg-12 mt--30">
                                            <input type="text" placeholder="Email *">
                                        </div>

                                        <div class="col-lg-12 mt--30">
                                            <input type="text" placeholder="Website">
                                        </div>

                                        <div class="col-lg-12 mt--30">
                                            <textarea placeholder="Your Comment"></textarea>
                                        </div>

                                        <div class="col-lg-12 mt--30">
                                            <div class="blog-btn">
                                                <button class="brook-btn bk-btn-theme btn-sd-size btn-rounded space-between">Post Comment</button>
                                            </div>
                                        </div>
                                    </div>
                                </form>
                            </div>
                            <!-- End Contact Area -->

                        </div>
                        <!-- End Comment Form -->
                    </div>
                </div>
            </div>
        </div>
        <!-- End Post Comment Area -->

        <FooterTwo />

    </div>
</template>

<script>
    
    export default {
        components: {
            HeaderBlack: () => import('@/components/custom/HeaderBlack'),
            OffCanvasMobileMenu: () => import('@/components/OffCanvasMobileMenu'),
            SearchPopup: () => import('@/components/SearchPopup'),
            BlogSidebar: () => import('@/components/BlogSidebar'),
            FooterTwo: () => import('@/components/FooterTwo'),
        },
        
        data () {
            return {
                data: {
                    "id": 1,
                    "title": "Words Make the Difference",
                    "date": "JULY 20, 2021",
                    "category": "ANALYTICS, CONTENT, TECHNOLOGY",
                    "image": `${this.$router.options.base}images/blog/blog-4.jpeg`,
                    "image2": `${this.$router.options.base}images/blog/blog-4-2.jpeg`,
                    "image3": `${this.$router.options.base}images/blog/blog-4-3.jpeg`,
                    "image4": `${this.$router.options.base}images/blog/blog-4-4.jpeg`,
                    "image5": `${this.$router.options.base}images/blog/blog-4-5.jpeg`,
                    "alt": "blog image",
                    "details" : "Anticipation is high for the payback on social marketing investments. The verdict is out for capturing any quantifiable results. A recent CMO poll cosponsored by Duke Business School and Deloite Touche indicates even with an average of 13% of marketing dollars being spent on social marketing only 30% of the respondents indicating that they have shown quantifiable value. "
                },
            }
        },

        mounted () {
            document.body.classList.add('template-color-5', 'template-font-1')
        },

        head() {
            return {
                title: 'Blog Details'
            }
        },
    };
</script>