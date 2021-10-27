<template>
    <div class="blog-grid" :class="addClass">
        <div class="post-thumb">
            <n-link :to="`/blog/${blog.id}`">
                <img :src="blog.image" :alt="blog.alt">
            </n-link>
        </div>
        <div class="post-content">
            <div class="post-inner">
                <h4 class="heading heading-h4">
                    <n-link :to="`/blog/${blog.id}`">
                        {{ blog.title }}
                    </n-link>
                </h4>
                <div class="post-meta">
                    <div class="post-date">{{ blog.date }}</div>
                    <div class="post-category">
                        <n-link :to="`/blog/${blog.id}`">
                            {{ blog.category }}
                        </n-link>
                    </div>
                </div>
                <div class="desc mt--20">
                    <p class="bk_pra">{{ blog.details }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ["blog", "addClass"]
    };
</script>