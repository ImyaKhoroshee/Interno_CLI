<template>
  <main class="blog-main">
    <IntroBackground class="intro">
      <IntroText class="intro-blog__text" :text="text" v-for="text in blogTexts" />
    </IntroBackground>

    <section class="blog-post center">
      <h2 class="blog-post__title">Latest Post</h2>
      <div class="blog-post__latest-post">
        <ArticleCard
          class="blog-post__latest-post-subbox"
          :article="article"
          v-for="article in blogpostArticles"
        >
          <template #paragraphs>
            <p class="blog-post__latest-post-prgth blog-post__latest-post-prgth_1">
              {{ article.paragraphOne }}
            </p>
            <p class="blog-post__latest-post-prgth blog-post__latest-post-prgth_2">
              {{ article.paragraphTwo }}
            </p></template
          >
        </ArticleCard>
      </div>
    </section>
    <section class="articles center">
      <h2 class="articles__title">Articles & News</h2>
      <div
        class="blog__cardbox-container articles__blog-cardbox-container"
        id="cardbox-container"
      >
        <ArticleCard :article="article" v-for="article in cardArticles">
          <template #button>
            <router-link to="/blog-details" class="blog__button">{{
              article.buttonText
            }}</router-link></template
          >
        </ArticleCard>
      </div>
      <div class="articles__pagination">
        <Pagination />
      </div>
    </section>
  </main>
</template>
<script>
// @ is an alias to /src

import IntroBackground from "@/components/IntroBackground.vue";
import IntroText from "@/components/IntroText.vue";
import ArticleCard from "@/components/ArticleCard.vue";
import Pagination from "@/components/Pagination.vue";

export default {
  name: "BlogView",
  components: {
    IntroBackground,
    IntroText,
    ArticleCard,
    Pagination,
  },
  data() {
    return {
      cardArticles: [
        {
          id: "article-card-1",
          src: require("../assets/blog_1.png"),
          alt: "interior",
          heading: "Let’s Get Solution For Building Construction Work",
          date: "26 December,2022",
          buttonText: "Kitchen Design",
        },
        {
          id: "article-card-2",
          src: require("../assets/blog_2.png"),
          alt: "interior",
          heading: "Low Cost Latest Invented Interior Designing Ideas",
          date: "22 December,2022",
          buttonText: "Living Design",
        },
        {
          id: "article-card-2",
          src: require("../assets/blog_3.png"),
          alt: "interior",
          heading: "Best For Any Office & Business Interior Solution",
          date: "25 December,2022",
          buttonText: "Interior Design",
        },
      ],
      blogTexts: [
        {
          id: "blogText",
          title: "Articles & News",
          subheadOne: "Home",
          subheadTwo: "Blog",
          routerlink: "/blog",
        },
      ],
      blogpostArticles: [
        {
          id: "blopost-card-1",
          src: require("../assets/latest_post_image.png"),
          alt: "kitchen",
          heading: "Low Cost Latest Invented Interior Designing Ideas",
          paragraphOne:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpis dignissim maximus.posuere in.Contrary to popular belief.",
          paragraphTwo:
            "Lorem Ipsum is not simply random text. It has roots in a piece of classica.",
          date: "26 December,2022",
          class: "blog-post__latest-post-text",
          head: "blog-post__latest-post-head",
        },
      ],
      articlesData: [
        {
          id: 1,
          src: require("../assets/blog_1.png"),
          alt: "interior",
          title: "Let’s Get Solution For Building Construction Work",
          date: "26 December,2022",
          button: "Kitchan Design",
        },
        {
          id: 2,
          src: require("../assets/blog_2.png"),
          alt: "interior",
          title: "Low Cost Latest Invented Interior Designing Ideas.",
          date: "22 December,2022",
          button: "Living Design",
        },
        {
          id: 3,
          src: require("../assets/blog_3.png"),
          alt: "interior",
          title: "Best For Any Office & Business Interior Solution",
          date: "25 December,2022",
          button: "Interior Design",
        },
        {
          id: 4,
          src: require("../assets/blog_4.png"),
          alt: "interior",
          title: "Let’s Get Solution For Building Construction Work",
          date: "26 December,2022",
          button: "Kitchan Design",
        },
        {
          id: 5,
          src: require("../assets/blog_5.png"),
          alt: "interior",
          title: "Low Cost Latest Invented Interior Designing Ideas.",
          date: "22 December,2022",
          button: "Living Design",
        },
        {
          id: 6,
          src: require("../assets/blog_6.png"),
          alt: "interior",
          title: "Best For Any Office & Business Interior Solution",
          date: "25 December,2022",
          button: "Interior Design",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.blog-post__latest-post-subbox :deep(.blog-post__latest-post-head) {
  width: 490px;
}
.articles__blog-cardbox-container :deep(.blog-post__latest-post-head) {
  width: 342px;
  margin-bottom: 52px;
}
</style>
