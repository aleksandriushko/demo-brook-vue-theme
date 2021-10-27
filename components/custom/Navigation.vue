<template>
    <nav class="page_nav">
        <ul class="mainmenu">
            <li class="lavel-1">
                <n-link to="/">
                    <span>Home</span>
                </n-link>
            </li>
            <li class="lavel-1">
                <n-link to="/about-us">
                    <span>About Us</span>
                </n-link>
            </li>
            <li class="lavel-1">
                <n-link to="/services">
                    <span>Services</span>
                </n-link>
            </li>
            <li class="lavel-1">
                <n-link to="/portfolio">
                    <span>Portfolio</span>
                </n-link>
            </li>
            <li class="lavel-1">
                <n-link to="/press">
                    <span>Press</span>
                </n-link>
            </li>
            <li class="lavel-1">
                <n-link to="/blog">
                    <span>Blog</span>
                </n-link>
            </li>
            <li class="lavel-1">
                <n-link to="/contact-us">
                    <span>Contact Us</span>
                </n-link>
            </li>
        </ul>
    </nav>
</template>

<style lang="scss">
    .mega__list {
        display: flex;
        li {
            flex-basis: 25%;
        }
    }
</style>