<script setup>
import BasicDropdown from "./components/BasicDropdown.vue";
const faqItems = [
  {
    id: 1,
    header: "How many team members can I invite?",
    body: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Beatae, quidem!",
  },
  {
    id: 2,
    header: "What is the maximum file upload size?",
    body: "No more than 2GB. All files in your account must fit your allotted storage space.",
  },
  {
    id: 3,
    header: "How do I reset my password?",
    body: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Beatae, quidem!",
  },
  {
    id: 4,
    header: "Can I cancel my subscription?",
    body: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Beatae, quidem!",
  },
  {
    id: 5,
    header: "Do you provide additional support?",
    body: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Beatae, quidem!",
  },
];
</script>

<template>
  <main>
    <div class="spacer"></div>
    <section class="faq-body">
      <figure>
        <img
          class="main-image-mobile"
          src="../src/assets/illustration-woman-online-mobile.svg"
          alt=""
        />
        <img
          class="image-shadow-mobile"
          src="../src/assets/bg-pattern-mobile.svg"
          alt=""
        />
        <img
          class="main-image-desktop"
          src="../src/assets/illustration-woman-online-desktop.svg"
          alt=""
        />
        <img
          class="image-shadow-desktop"
          src="../src/assets/bg-pattern-desktop.svg"
          alt=""
        />
      </figure>
      <img
        class="icon-desktop"
        src="../src/assets/illustration-box-desktop.svg"
        alt=""
      />
      <article>
        <h1>FAQ</h1>
        <ul>
          <BasicDropdown
            v-for="item in faqItems"
            :key="item.id"
            :header="item.header"
            :body="item.body"
          />
        </ul>
      </article>
    </section>
  </main>
</template>

<style lang="scss" scoped>
.faq-body {
  width: 327px;
  background-color: var(--color-card-bg);
  border-radius: 23px;
  box-shadow: 0px 50px 50px -20px rgba(53, 18, 122, 0.5);
}

figure {
  text-align: center;
  height: 104px;
  margin-bottom: 28px;

  .main-image-mobile {
    position: absolute;
    top: -108px;
    left: 43px;
    width: 237px;
  }
  .image-shadow-mobile {
    position: absolute;
    width: 240px;
    left: 43px;
  }
  .main-image-desktop {
    display: none;
  }
  .image-shadow-desktop {
    display: none;
  }
}
.icon-desktop {
  display: none;
}

article {
  width: 279px;
  margin: 0 auto 48px;
}

h1 {
  text-align: center;
  font: 700 32px "Kumbh Sans";
  color: var(--color-heading);
  margin-bottom: 30px;
}
ul {
  list-style-type: none;
  padding: 0;
  width: 279px;
}
.spacer {
  height: 100px;
  width: 100px;
}

@media screen and (min-width: 1440px) {
  .faq-body {
    width: 920px;
    height: 509px;
    display: flex;
  }

  figure {
    width: 388px;
    height: 100%;
    overflow: hidden;

    .main-image-mobile {
      display: none;
    }
    .image-shadow-mobile {
      display: none;
    }
    .main-image-desktop {
      display: block;
      position: absolute;
      top: 70px;
      left: -84px;
    }
    .image-shadow-desktop {
      display: block;
      position: absolute;
      top: -294px;
      left: -576px;
      width: 964px;
      opacity: 0.4;
    }
  }
  .icon-desktop {
    display: block;
    position: absolute;
    top: 205px;
    left: -95px;
  }

  article {
    width: 532px;
    padding: 65px 0 0 88px;
    margin: 0px;
  }
  h1 {
    text-align: left;
    margin-bottom: 20px;
  }
  ul {
    list-style-type: none;
    padding: 0;
    width: 350px;
  }
  .spacer {
    display: none;
  }
}
</style>
