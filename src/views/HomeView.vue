<template>
  <main class="main">
    <section class="banner center">
      <Banner
        :banner="banner"
        v-for="banner in homeBanner"
        :buttonText="buttonText"
        :link="link"
      />
    </section>
    <section class="projects center" id="projects">
      <h2 class="projects__heading">Follow Our Projects</h2>
      <p class="projects__text">
        It is a long established fact that a reader will be distracted by the of readable
        content of page lookings at its layouts points.
      </p>
      <div class="projects__images">
        <ProjectCard :project="project" v-for="project in projects" />
      </div>
    </section>
    <div class="counter">
      <div class="counter-wrapper center">
        <div class="counter__content-box counter__content-box_1">
          <p class="counter__content-digit">12</p>
          <p class="counter__content-text">Years Of Experiance</p>
        </div>
        <div class="counter__line counter__line_1"></div>
        <div class="counter__content-box counter__content-box_2">
          <p class="counter__content-digit">85</p>
          <p class="counter__content-text">Success Project</p>
        </div>
        <div class="counter__line counter__line_2"></div>
        <div class="counter__content-box counter__content-box_3">
          <p class="counter__content-digit">15</p>
          <p class="counter__content-text">Active Project</p>
        </div>
        <div class="counter__line counter__line_3"></div>
        <div class="counter__content-box">
          <p class="counter__content-digit">95</p>
          <p class="counter__content-text">Happy CUstomers</p>
        </div>
      </div>
    </div>
    <section class="blog center" id="blog">
      <h2 class="blog__heading">Articles & News</h2>
      <p class="blog__paragraph">
        It is a long established fact that a reader will be distracted by the of readable
        content of a page when lookings at its layouts the points of using.
      </p>
      <div class="blog__cardbox-container">
        <ArticleCard :article="article" v-for="article in cardArticles">
          <template #button>
            <router-link to="/blog-details" class="blog__button">{{
              article.buttonText
            }}</router-link></template
          >
        </ArticleCard>
      </div>
    </section>
  </main>
</template>

<script>
// @ is an alias to /src

import Banner from "@/components/Banner.vue";
import ProjectCard from "@/components/ProjectCard.vue";
import ArticleCard from "@/components/ArticleCard.vue";

export default {
  name: "HomeView",
  components: {
    Banner,
    ProjectCard,
    ArticleCard,
  },
  data() {
    return {
      link: "/:CatchAll(.*)",
      buttonText: "Get Started",
      homeBanner: [
        {
          id: "homebanner",
          src: require("../assets/intro-image.png"),
          alt: "living-room",
          heading: "Let Your Home Be Unique",
          paragraph:
            "There are many variations of the passages of lorem Ipsum fromavailable, majority.",
        },
      ],
      projects: [
        {
          id: "productcard1",
          src: require("../assets/project-1.png"),
          alt: "interio",
          title: "Modern Kitchen",
          subject: "Decor",
          field: "Architecture",
          class: "projects__card-image_1",
        },
        {
          id: "productcard2",
          src: require("../assets/project-2.png"),
          alt: "interio",
          title: "Modern Kitchen",
          subject: "Decor",
          field: "Architecture",
          class: "projects__card-image_2",
        },
        {
          id: "productcard3",
          src: require("../assets/project-3.png"),
          alt: "interio",
          title: "Modern Kitchen",
          subject: "Decor",
          field: "Architecture",
          class: "projects__card-image_3",
          classbottom: "projects__card-textbox_bottom",
        },
        {
          id: "productcard4",
          src: require("../assets/project-4.png"),
          alt: "interio",
          title: "Modern Kitchen",
          subject: "Decor",
          field: "Architecture",
          class: "projects__card-image_4",
          classbottom: "projects__card-textbox_bottom",
        },
      ],
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
    };
  },
};
</script>
<style scoped lang="scss">
.banner :deep(.banner-box) {
  position: relative;
}
.banner :deep(.banner__text) {
  position: absolute;
  max-width: 434px;
  top: 208px;
  left: 52px;
}

.banner :deep(.banner__heading) {
  margin-bottom: 18px;
  color: #292f36;
  font-family: DM Serif Display;
  font-size: 65px;
  font-style: normal;
  font-weight: 400;
  line-height: 125%;
}

.banner :deep(.banner__paragraph) {
  margin-bottom: 21px;
  color: #4d5053;
  font-family: Jost;
  font-size: 22px;
  font-style: normal;
  font-weight: 400;
  line-height: 150%;
  letter-spacing: 0.22px;
}

.blog__cardbox-container :deep(.blog-post__latest-post-head) {
  width: 341px;
  margin-bottom: 50px;
}
</style>
