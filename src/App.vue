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
    <section class="faq-body">
      <figure>
        <img
          class="main-image"
          src="../src/assets/illustration-woman-online-mobile.svg"
          alt=""
        />
        <img
          class="image-shadow"
          src="../src/assets/bg-pattern-mobile.svg"
          alt=""
        />
      </figure>
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
  height: 535px;
  background-color: var(--color-card-bg);
  border-radius: 23px;
  box-shadow: 0px 50px 50px -20px rgba(53, 18, 122, 0.5);
}

figure {
  text-align: center;
  height: 104px;
  margin-bottom: 28px;

  .main-image {
    position: absolute;
    top: -108px;
    left: 43px;
    width: 237px;
  }
  .image-shadow {
    position: absolute;
    width: 240px;
    left: 43px;
  }
}

article {
  width: 279px;
  margin: 0 auto;
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
</style>
