<template>
    <div class="main-container">

        <HeaderBlack addClass="header-transparent" />

        <OffCanvasMobileMenu />

        <SearchPopup />

        <div class="breadcrumb-area pt--260 pb--80 pt_md--200 pt_sm--150 bg_color--5 breadcrumb-title-bar">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12">
                        <div class="breadcrumb-inner text-center">
                            <h1 class="heading heading-h1">Blog</h1>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="blog-creative-area bg_color--5 pt--70 pb--100">
            <div class="container">
                <div class="row">
                    <div class="col-lg-8 mtn--70">
                        <div class="creative-blog wow move-up mt--70" v-for="blog in blogs" :key="blog.title">
                            <BlogPostFour :blog="blog" addClass="blog-standard-list" />
                        </div>

                        <div class="brook-pagination-wrapper text-center pt--80">
                            <paginate
                                :page-count="4"
                                :page-range="3"
                                :margin-pages="2"
                                :prev-text="'Prev'"
                                :next-text="'Next'"
                                :container-class="'brook-pagination'"
                                :page-class="'page-item'">
                            </paginate>
                        </div>
                    </div>

                    <div class="col-lg-4 mt_md--40 mt_sm--40">
                        <BlogSidebar />
                    </div>
                </div>
            </div>
        </div>

        <FooterTwo />

    </div>
</template>

<script>
    export default {
        components: {
            HeaderBlack: () => import('@/components/custom/HeaderBlack'),
            OffCanvasMobileMenu: () => import('@/components/OffCanvasMobileMenu'),
            SearchPopup: () => import('@/components/SearchPopup'),
            BlogPostFour: () => import('@/components/custom/BlogPostFour'),
            BlogSidebar: () => import('@/components/BlogSidebar'),
            FooterTwo: () => import('@/components/FooterTwo'),
        },
        
        data () {
            return {
                "blogs": [
                    {
                        "id": 1,
                        "title": "Creeping The Holiday Spirit Alive!",
                        "date": "OCTOBER 13, 2021",
                        "category": "CONTENT, CREATIVE",
                        "image": `${this.$router.options.base}images/blog/blog-1.jpeg`,
                        "alt": "blog image",
                        "details" : "You always know that spooky season is around the corner when the big brands start to get involved. When TV spots start to get autumnal, something wicked this way comes! Here are 5 Fangtastic ads to keep you inspired this holiday season:",
                    },
                    // {
                    //     "id": 1,
                    //     "title": "5 Chrome Extensions To Speed Up Your UX Workflow",
                    //     "date": "SEPTEMBER 29, 2021",
                    //     "category": "CREATIVE, TRENDS",
                    //     "image": `${this.$router.options.base}images/blog/blog-2.jpeg`,
                    //     "alt": "blog image",
                    //     "details" : "Our UX Design teams in Atlanta and Cleveland are always looking for ways to speed-up our workflow. Here are 5 of the Chrome extensions we’ve been putting to good use regularly at Yalo. Loom - This plugin is billed as video messaging for work and while I’m sure it fulfills that overarching goal, we primarily use it to quickly record UX and UI work that benefits from a video walkthrough. "
                    // },
                    // {
                    //     "id": 1,
                    //     "title": "Raising The Bar On Beverage Marketing",
                    //     "date": "AUGUST 4, 2021",
                    //     "category": "CONTENT, CREATIVE, CULTURE",
                    //     "image": `${this.$router.options.base}images/blog/blog-3.jpeg`,
                    //     "alt": "blog image",
                    //     "details" : "In celebration of National IPA Day we are sharing our favorite ideas for beer sales and promotions. Categories include: Contests and sweepstakes, promotions, on-site and online activities, and charitable initiatives."
                    // },
                    // {
                    //     "id": 1,
                    //     "title": "Words Make the Difference",
                    //     "date": "JULY 20, 2021",
                    //     "category": "ANALYTICS, CONTENT, TECHNOLOGY",
                    //     "image": `${this.$router.options.base}images/blog/blog-4.jpeg`,
                    //     "alt": "blog image",
                    //     "details" : "Anticipation is high for the payback on social marketing investments. The verdict is out for capturing any quantifiable results. A recent CMO poll cosponsored by Duke Business School and Deloite Touche indicates even with an average of 13% of marketing dollars being spent on social marketing only 30% of the respondents indicating that they have shown quantifiable value. "
                    // },
                    // {
                    //     "id": 1,
                    //     "title": "Dog Days Of Summer: Business Pause",
                    //     "date": "JULY 20, 2021",
                    //     "category": "CONTENT, CREATIVE, SOCIAL",
                    //     "image": `${this.$router.options.base}images/blog/blog-5.jpeg`,
                    //     "alt": "blog image",
                    //     "details" : "It’s the lazy, hazy, dog days of summer. People go on vacation, business slows down, and you take a moment to catch your breath especially after the year we’ve all had. Many businesses are doggy paddling through this seasonal lull. So we came up with a few suggestions to make the best of the pause."
                    // },
                    // {
                    //     "id": 1,
                    //     "title": "Last Call",
                    //     "date": "JULY 20, 2021",
                    //     "category": "CONTENT, CREATIVE",
                    //     "image": `${this.$router.options.base}images/blog/blog-6.jpeg`,
                    //     "alt": "blog image",
                    //     "details" : "Getting someone to take action after reading your post, ad, etc. is a true skill and a sign of a talented marketer. You can have all the right pieces in place…from a killer headline to an amazing article, but if it doesn’t result in action, is it worth it? "
                    // },
                    // {
                    //     "id": 1,
                    //     "title": "The Lead Generation",
                    //     "date": "JULY 7, 2021",
                    //     "category": "BUSINESS, CREATIVE, TECHNOLOGY",
                    //     "image": `${this.$router.options.base}images/blog/blog-7.jpeg`,
                    //     "alt": "blog image",
                    //     "details" : "When it comes to lead generation on your website, it all starts with one page; the homepage. Not only does your homepage set the tone for a good (or poor) user experience, it can also mean the difference between a lead and zilch."
                    // },
                    // {
                    //     "id": 1,
                    //     "title": "Artificial Intelligence: Fear and Promise in the Age of Change",
                    //     "date": "JULY 7, 2021",
                    //     "category": "INNOVATION, TECHNOLOGY",
                    //     "image": `${this.$router.options.base}images/blog/blog-8.jpeg`,
                    //     "alt": "blog image",
                    //     "details" : "A question often heard these days is, “What is your deepest fear?” This quote was made famous in the movie Coach Carter. Artificial intelligence has created fears on many levels. Three fears are emerging as our “deepest fears.” Since there is something magical about the number three, we will focus on these “deepest fears,” and how they can become opportunities."
                    // },
                ],
            }
        },

        mounted () {
            document.body.classList.add('template-color-5', 'template-font-1')
        },

        head() {
            return {
                title: 'Blog Standard List'
            }
        },
    };
</script>