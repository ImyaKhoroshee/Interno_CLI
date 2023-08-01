<template>
  <main class="main-blog-details">
    <section class="blog-details__intro">
      <div class="blog-details__intro-image"></div>
    </section>

    <div id="blogdetails" class="blog-details__box center">
      <div class="blog-details">
        <BlogDetailsArticle
          :article="article"
          v-for="article in sortedArray"
          :key="article.id"
          :id="article.id"
        />
      </div>

      <div class="blog-details__aside">
        <h3 class="blog-details__aside-title">{{ title }}</h3>
        <div class="blog-details__buttons">
          <BlogDetailsButton
            :button="button"
            v-for="button in buttons"
            @change="sortArticles"
            @click="filters"
          />
        </div>
      </div>
    </div>
  </main>
</template>
<script>
import BlogDetailsArticle from "@/components/BlogDetailsArticle.vue";
import BlogDetailsButton from "@/components/BlogDetailsButton.vue";

export default {
  name: "BlogDetailsView",
  components: {
    BlogDetailsArticle,
    BlogDetailsButton,
  },
  data() {
    return {
      title: "Tag",
      sortedArray: [
        {
          id: "kitchen",
          title: "Let’s Get Solution for Building Construction Work",
          date: "26 December,2022",
          link: "Interior / Home / Decore",
          firstpargth:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don’t look even slightly believable.",
          secondpargth:
            "Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          src: require("../assets/blog_kitchen.png"),
          alt: "photo",
          quote: "The details are not the details. They make the design.",
          subtitle: "Design sprints are great",
          thirdpargth:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          firstnumber: "1",
          secondnumber: "2",
          thirdnumber: "3",
          fourthpargth:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          secondsrc: require("../assets/blog_kitchen_bottom.jpg"),
        },
      ],
      articles: [
        {
          id: "kitchen",
          title: "Let’s Get Solution for Building Construction Work",
          date: "26 December,2022",
          link: "Interior / Home / Decore",
          firstpargth:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don’t look even slightly believable.",
          secondpargth:
            "Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          src: require("../assets/blog_kitchen.png"),
          alt: "photo",
          quote: "The details are not the details. They make the design.",
          subtitle: "Design sprints are great",
          thirdpargth:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          firstnumber: "1",
          secondnumber: "2",
          thirdnumber: "3",
          fourthpargth:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          secondsrc: require("../assets/blog_kitchen_bottom.jpg"),
        },
        {
          id: "bedroom",
          title: "Low Cost Latest Invented Interior Designing Ideas.",
          date: "22 December,2022",
          link: "Interior / Home / Decore",
          firstpargth:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don t look even slightly believable.",
          secondpargth:
            "Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          src: require("../assets/blog_bedroom.jpeg"),
          alt: "photo",
          quote: "The details are not the details. They make the design.",
          subtitle: "Design sprints are great",
          thirdpargth:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          firstnumber: "1",
          secondnumber: "2",
          thirdnumber: "3",
          fourthpargth:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          secondsrc: require("../assets/bedroom.jpeg"),
        },
        {
          id: "building",
          title:
            "Building, a usually roofed and walled structure built for permanent use.",
          date: "20 December,2022",
          link: "Country / City / Building",
          firstpargth:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don t look even slightly believable.",
          secondpargth:
            "Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          src: require("../assets/blog_building.jpeg"),
          alt: "photo",
          quote:
            "Good buildings come from good people, and all problems are solved by good design.",
          subtitle: "We shape our buildings; thereafter, they shape us.",
          thirdpargth:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          firstnumber: "1",
          secondnumber: "2",
          thirdnumber: "3",
          fourthpargth:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          secondsrc: require("../assets/blog_building_2.jpeg"),
        },
        {
          id: "architecture",
          title:
            "Our paper emphasizes the importance of the kitchen layout in facilitating consumers food hygiene practices.",
          date: "29 December,2022",
          link: "Country / City / Architecture",
          firstpargth:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don t look even slightly believable.",
          secondpargth:
            "Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          src: require("../assets/blog_architecture.jpeg"),
          alt: "photo",
          quote: "Architecture is a visual art, and the buildings speak for themselves.",
          subtitle:
            "Architecture around the world by contemporary architects including cutting-edge houses, skyscrapers, cultural buildings, hotels, airports, apartments.",
          thirdpargth:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          firstnumber: "1",
          secondnumber: "2",
          thirdnumber: "3",
          fourthpargth:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          secondsrc: require("../assets/blog_architecture_2.jpeg"),
        },
        {
          id: "kitchen-planning",
          title: "Kitchen Planning: Selecting the Right Layout",
          date: "25 December,2022",
          link: "Interior / Home / Kitchen",
          firstpargth:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don t look even slightly believable.",
          secondpargth:
            "Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          src: require("../assets/kitchen_planning.jpeg"),
          alt: "photo",
          quote: "The kitchen is the heart of the home.",
          subtitle:
            "Kitchens should be designed around whats truly important – fun, food, and life.",
          thirdpargth:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          firstnumber: "1",
          secondnumber: "2",
          thirdnumber: "3",
          fourthpargth:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          secondsrc: require("../assets/kitchen_planning_2.jpeg"),
        },
      ],

      buttons: [
        { id: "kitchen", text: "Kitchen" },
        { id: "bedroom", text: "Bedroom" },
        { id: "building", text: "Building" },
        { id: "architecture", text: "Architecture" },
        { id: "kitchen-planning", text: "Kitchen Planning" },
      ],
    };
  },
  methods: {
    sortArticles(e) {
      console.log(e.target);
      if (document.querySelector(".blog-details__button-active") !== null) {
        document
          .querySelector(".blog-details__button-active")
          .classList.remove("blog-details__button-active");
      }
      const divButton = e.target.closest(".blog-details__button");
      divButton.classList.add("blog-details__button-active");
    },
    filters(e) {
      this.sortedArray = this.articles.filter(
        (article) => article.id === e.target.dataset.id
      );
    },
  },
};
</script>
