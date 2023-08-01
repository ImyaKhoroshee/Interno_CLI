<template>
  <main class="blog-main">
    <section class="intro">
      <div class="intro__title">
        <h2 class="intro__heading">Articles & News</h2>
        <div class="intro__subhead-box">
          <router-link to="/" class="intro__subhead-box-item">Home</router-link>
          <router-link to="/blog" class="intro__subhead-box-item">Blog</router-link>
        </div>
      </div>
    </section>
    <section class="blog-post center">
      <h2 class="blog-post__title">Latest Post</h2>
      <div class="blog-post__latest-post">
        <div class="blog-post__latest-post-subbox">
          <img
            class="blog-post__latest-post-image"
            src="../assets/latest_post_image.jpg"
            alt="kitchen"
          />
          <article class="blog-post__latest-post-text">
            <h3 class="blog-post__latest-post-head">
              Low Cost Latest Invented Interior Designing Ideas
            </h3>
            <p class="blog-post__latest-post-prgth blog-post__latest-post-prgth_1">
              Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpis dignissim
              maximus.posuere in.Contrary to popular belief.
            </p>
            <p class="blog-post__latest-post-prgth blog-post__latest-post-prgth_2">
              Lorem Ipsum is not simply random text. It has roots in a piece of classica.
            </p>
            <div class="blog__data-arrow-box blog-post__data-arrow-box">
              <p class="blog__date">26 December,2022</p>
              <a href="#" class="blog__arrowbox">
                <svg
                  width="9"
                  height="16"
                  viewBox="0 0 9 16"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M1.77144 14.9527L7.71429 8.267L1.77144 1.58128"
                    stroke="#292F36"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                </svg>
              </a>
            </div>
          </article>
        </div>
      </div>
    </section>
    <section class="articles center">
      <h2 class="articles__title">Articles & News</h2>
      <div
        class="blog__cardbox-container articles__blog-cardbox-container"
        id="cardbox-container"
      >
        <div class="blog__cardbox" v-for="article in articlesData" :key="article.id">
          <img :src="article.src" :alt="article.alt" class="blog__image" />
          <h3 class="blog__head">{{ article.title }}</h3>
          <div class="blog__data-arrow-box">
            <p class="blog__date">{{ article.date }}</p>
            <router-link to="/blog-details" class="blog__arrowbox">
              <svg
                width="9"
                height="16"
                viewBox="0 0 9 16"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M1.77144 14.9527L7.71429 8.267L1.77144 1.58128"
                  stroke="#292F36"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </router-link>
          </div>
          <a href="#" class="blog__button">{{ article.button }}</a>
        </div>
      </div>
      <div class="articles__pagination">
        <span class="articles__pagination-item">01</span>
        <span class="articles__pagination-item">02</span>
        <span class="articles__pagination-item">03</span>
        <span class="articles__pagination-item"
          ><svg
            width="9"
            height="16"
            viewBox="0 0 9 16"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M1.55714 15L7.5 8.31429L1.55714 1.62857"
              stroke="#292F36"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </span>
      </div>
    </section>
  </main>
</template>
<script>
// @ is an alias to /src

// import Компонент from '@/components/Компонент.vue'

export default {
  name: "BlogView",
  components: {
    // Компонент,
  },
  data() {
    return {
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
