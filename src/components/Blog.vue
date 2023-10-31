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
  <div class="blog_banner">
    <div class="blog_banner__intro">
      <h2 class="blog_banner__intro_header">Articles & News</h2>
      <p class="blog_banner__intro_text">Home / Blog</p>
    </div>
  </div>
  <div class="post center">
    <h2 class="post__header">Latest Post</h2>
    <div class="post__content">
      <img src="../assets/image/blog_post.jpg" alt="picture" />
      <div class="post__content_txt">
        <h3 class="post__content_txt_header">
          Low Cost Latest Invented Interior Designing Ideas
        </h3>
        <p class="post__content_txt_text">
          Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpis
          dignissim maximus.posuere in.Contrary to popular belief.
        </p>
        <p class="post__content_txt_text">
          Lorem Ipsum is not simply random text. It has roots in a piece of
          classica.
        </p>
        <div class="post__content_txt_wrapper">
          <p class="post__content_txt_wrapper_text">26 December,2022</p>
          <svg
            class="post__content_txt_wrapper_arrow"
            xmlns="http://www.w3.org/2000/svg"
            width="52"
            height="53"
            viewBox="0 0 52 53"
            fill="none"
          >
            <circle cx="26" cy="26.5" r="26" fill="#F4F0EC" />
            <path
              d="M23.771 33.1855L29.7139 26.4998L23.771 19.8141"
              stroke="#292F36"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </div>
      </div>
    </div>
  </div>
  <section class="news center">
    <h2 class="news__header">Articles & News</h2>
    <div class="news__content">
      <article
        class="news__content_item"
        v-for="(item, index) in articles"
        :key="index"
      >
        <div class="news__content_item_img">
          <img :src="item.image" alt="image" />
          <div class="news__content_item_label">
            <p class="news__content_item_label_text">{{ item.label }}</p>
          </div>
        </div>
        <div class="news__content_item_txtcontent">
          <h3 class="txtcontent_header">{{ item.heading }}</h3>
          <div class="wrapper">
            <p class="txtcontent_text">{{ item.date }}</p>
            <svg
              class="arrow"
              xmlns="http://www.w3.org/2000/svg"
              width="52"
              height="53"
              viewBox="0 0 52 53"
              fill="none"
            >
              <circle cx="26" cy="26.267" r="26" fill="#F4F0EC" />
              <path
                d="M23.7714 32.9527L29.7143 26.267L23.7714 19.5813"
                stroke="#292F36"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </div>
        </div>
      </article>
    </div>
    <div class="news__pagination"></div>
  </section>
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
      articles: [
        {
          image: require("@/assets/image/blog_item_1.jpg"),
          label: "Kitchan Design",
          heading: "Let’s Get Solution For Building Construction Work",
          date: "26 December,2022 ",
        },
        {
          image: require("@/assets/image/blog_item_2.jpg"),
          label: "Living Design",
          heading: "Low Cost Latest Invented Interior Designing Ideas.",
          date: "22 December,2022 ",
        },
        {
          image: require("@/assets/image/blog_item_3.jpg"),
          label: "Interior Design",
          heading: "Best For Any Office & Business Interior Solution",
          date: "25 December,2022 ",
        },
        {
          image: require("@/assets/image/blog_item_4.jpg"),
          label: "Kitchan Design",
          heading: "Let’s Get Solution For Building Construction Work",
          date: "26 December,2022 ",
        },
        {
          image: require("@/assets/image/blog_item_5.jpg"),
          label: "Living Design",
          heading: "Let’s Get Solution For Building Construction Work",
          date: "22 December,2022 ",
        },
        {
          image: require("@/assets/image/blog_item_6.jpg"),
          label: "Interior Design",
          heading: "Let’s Get Solution For Building Construction Work",
          date: "25 December,2022 ",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss"></style>
