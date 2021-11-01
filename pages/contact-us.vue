<template>
    <div class="main-container">

        <HeaderElement />

        <OffCanvasMobileMenu />

        <SearchPopup />

        <ContactUsBreadcrumb />

        <ContactModern />

        <FooterTwo />

    </div>
</template>

<script>
    export default {
        components: {
            HeaderElement: () => import('@/components/custom/HeaderBlack'),
            OffCanvasMobileMenu: () => import('@/components/OffCanvasMobileMenu'),
            SearchPopup: () => import('@/components/SearchPopup'),
            ContactUsBreadcrumb: () => import('@/components/custom/ContactUsBreadcrumb'),
            ContactModern: () => import('@/components/custom/ContactModern'),
            FooterTwo: () => import('@/components/FooterTwo'),
        },

        mounted () {
            document.body.classList.add('template-color-5', 'template-font-1')
        },

        head() {
            return {
                title: 'Brook || Contact Us Modern'
            }
        },
    };
</script>