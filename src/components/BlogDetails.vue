<template>
  <header class="header center">
    <a class="header__left" href="main.html">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="34"
        height="34"
        viewBox="0 0 34 34"
        fill="none"
      >
        <path
          d="M0 34.0003H13.4588V24.499C13.4588 22.4853 15.0898 20.8543 17.1035 20.8543C19.1172 20.8543 20.7482 22.4853 20.7482 24.499V34.0003H33.9975V0C15.2211 0 0 15.2211 0 34.0003Z"
          fill="#CDA274"
        />
      </svg>
      <h3 class="header__left_title">Interno</h3>
    </a>
    <nav class="header__right">
      <a href="#" class="header__right_nav">Home</a>
      <a href="#" class="header__right_nav">Project</a>
      <a href="#" class="header__right_nav">Blog</a>
    </nav>
  </header>
  <div class="details_banner center"></div>
  <div class="articles center">
    <div class="articles__details">
      <div
        class="articles__details_article"
        v-for="item in details"
        :key="item.id"
      >
        <h2 class="articles__details_article_header">{{ item.header1 }}</h2>
        <img
          :src="item.image1"
          class="articles__details_article_image1"
          alt="image"
        />
        <div class="articles__details_article_wrapper">
          <p>{{ item.date }}</p>
          <p>{{ item.nav }}</p>
        </div>
        <p class="articles__details_article_text">{{ item.text1 }}</p>
        <p class="articles__details_article_text">{{ item.text2 }}</p>
        <div class="articles__details_article_slogan">
          <img :src="item.commas" alt="commas" />
          <h1 class="articles__details_article_slogan_header">
            {{ item.slogan }}
          </h1>
        </div>
        <h2 class="articles__details_article_header">{{ item.header2 }}</h2>
        <p class="articles__details_article_text">{{ item.text3 }}</p>
        <ol class="articles__details_article_ol">
          <li class="articles__details_article_li">{{ item.list2 }}</li>
          <li class="articles__details_article_li">{{ item.list1 }}</li>
          <li class="articles__details_article_li">{{ item.list3 }}</li>
        </ol>
        <img
          :src="item.image2"
          class="articles__details_article_image2"
          alt="image"
        />
        <p class="articles__details_article_text">{{ item.text4 }}</p>
      </div>
    </div>
    <div class="articles__sidebar">
      <h3 class="articles__sidebar_header">Tags</h3>
      <div class="articles__sidebar_tags">
        <button
          class="articles__sidebar_tags_button"
          v-for="item in tags"
          :key="item.id"
          @click="chooseArticle(item.id)"
        >
          {{ item.tagName }}
        </button>
      </div>
    </div>
  </div>
  <footer class="footer center">
    <div class="footer__link">
      <a class="footer__link_logo" href="main.html">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="34"
          height="34"
          viewBox="0 0 34 34"
          fill="none"
        >
          <path
            d="M0 34.0003H13.4588V24.499C13.4588 22.4853 15.0898 20.8543 17.1035 20.8543C19.1172 20.8543 20.7482 22.4853 20.7482 24.499V34.0003H33.9975V0C15.2211 0 0 15.2211 0 34.0003Z"
            fill="#CDA274"
          />
        </svg>
        <h3 class="footer__link_logo_title">Interno</h3>
      </a>
      <p class="footer__link_text">
        It is a long established fact that a reader will be distracted lookings.
      </p>
      <div class="footer__link_icons">
        <a href="#"
          ><img src="../assets/image/footer_icon_1.svg" alt="twitter"
        /></a>
        <a href="#"
          ><img src="../assets/image/footer_icon_2.svg" alt="insta"
        /></a>
      </div>
    </div>
    <div class="footer__pages">
      <h3 class="footer__pages_header">Pages</h3>
      <a class="footer__pages_item">Home</a>
      <a class="footer__pages_item">Project</a>
      <a class="footer__pages_item">Blog</a>
    </div>
    <div class="footer__contacts">
      <h3 class="footer__contacts_header">Contact</h3>
      <div class="footer__contacts_wrapper">
        <p class="footer__contacts_text">
          55 East Birchwood Ave. Brooklyn, New York 11201
        </p>
        <p class="footer__contacts_text">contact@interno.com</p>
        <p class="footer__contacts_text">(123) 456 - 7890</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      details: [
        {
          id: 1,
          header1: "Let’s Get Solution for Building Construction Work",
          image1: require("@/assets/image/details_1_1.jpg"),
          date: "26 December,2022 ",
          nav: "Interior / Home / Decore",
          text1:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable.",
          text2:
            "Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          commas: require("@/assets/image/details_commas.png"),
          slogan: "The details are not the details. They make the design.",
          header2: "Design sprints are great",
          text3:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list1:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list2:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list3:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          image2: require("@/assets/image/details_1_2.jpg"),
          text4:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
        },
        {
          id: 2,
          header1: "Low Cost Latest Invented Interior Designing Ideas.",
          image1: require("@/assets/image/details_2_1.jpg"),
          date: "22 December,2022 ",
          nav: "Interior / Home / Decore",
          text1:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable.",
          text2:
            "Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          commas: require("@/assets/image/details_commas.png"),
          slogan: "The details are not the details. They make the design.",
          header2: "Design sprints are great",
          text3:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list1:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list2:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list3:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          image2: require("@/assets/image/details_2_2.jpg"),
          text4:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
        },
        {
          id: 3,
          header1: "Best For Any Office & Business Interior Solution",
          image1: require("@/assets/image/details_3_1.jpg"),
          date: "25 December,2022 ",
          nav: "Interior / Home / Decore",
          text1:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable.",
          text2:
            "Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          commas: require("@/assets/image/details_commas.png"),
          slogan: "The details are not the details. They make the design.",
          header2: "Design sprints are great",
          text3:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list1:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list2:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list3:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          image2: require("@/assets/image/details_3_2.jpg"),
          text4:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
        },
        {
          id: 4,
          header1: "Let’s Get Solution for Building Construction Work",
          image1: require("@/assets/image/details_4_1.jpg"),
          date: "26 December,2022 ",
          nav: "Interior / Home / Decore",
          text1:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable.",
          text2:
            "Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          commas: require("@/assets/image/details_commas.png"),
          slogan: "The details are not the details. They make the design.",
          header2: "Design sprints are great",
          text3:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list1:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list2:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list3:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          image2: require("@/assets/image/details_4_2.jpg"),
          text4:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
        },
        {
          id: 5,
          header1: "Low Cost Latest Invented Interior Designing Ideas.",
          image1: require("@/assets/image/details_5_1.jpg"),
          date: "22 December,2022 ",
          nav: "Interior / Home / Decore",
          text1:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable.",
          text2:
            "Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          commas: require("@/assets/image/details_commas.png"),
          slogan: "The details are not the details. They make the design.",
          header2: "Design sprints are great",
          text3:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list1:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list2:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list3:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          image2: require("@/assets/image/details_5_2.jpg"),
          text4:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
        },
        {
          id: 6,
          header1: "Best For Any Office & Business Interior Solution",
          image1: require("@/assets/image/details_6_1.jpg"),
          date: "25 December,2022 ",
          nav: "Interior / Home / Decore",
          text1:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which don't look even slightly believable.",
          text2:
            "Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.",
          commas: require("@/assets/image/details_commas.png"),
          slogan: "The details are not the details. They make the design.",
          header2: "Design sprints are great",
          text3:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list1:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list2:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          list3:
            "Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
          image2: require("@/assets/image/details_6_2.jpg"),
          text4:
            "Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.",
        },
      ],
      tags: [
        {
          id: 1,
          tagName: "Kitchen",
        },
        {
          id: 2,
          tagName: "Bedroom",
        },
        {
          id: 3,
          tagName: "Building",
        },
        {
          id: 4,
          tagName: "Architecture",
        },
        {
          id: 5,
          tagName: "Kitchen Planning",
        },
        {
          id: 6,
          tagName: "Bedroom",
        },
      ],
    };
  },
  methods: {
    chooseArticle(id) {
      this.details = this.details.filter((el) => el.id === id);
    },
  },
};
</script>

<style scoped lang="scss"></style>
