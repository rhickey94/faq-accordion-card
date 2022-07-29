<script setup></script>

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
          <li>
            How many team members can I invite? <button></button>
            <!-- <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Beatae,
              quidem!
            </p> -->
          </li>
          <li>
            What is the maximum file upload size? <button></button>
            <!-- <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Beatae,
              quidem!
            </p> -->
          </li>
          <li>
            How do I reset my password?<button></button>
            <!-- <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Beatae,
              quidem!
            </p> -->
          </li>
          <li>
            Can I cancel my subscription? <button></button>
            <!-- <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Beatae,
              quidem!
            </p> -->
          </li>
          <li>
            Do you provide additional support? <button></button>
            <!-- <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Beatae,
              quidem!
            </p> -->
          </li>
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
  position: relative;
  margin-bottom: 28px;

  .main-image {
    position: absolute;
    top: -108px;
    left: 43px;
    width: 237px;
    height: 180px;
  }
  .image-shadow {
    position: absolute;
    width: 240px;
    left: 43px;
  }
}

article {
  width: 279px;
  padding: 0 0 48px;
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

li {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
  border-bottom: 1px solid;
  border-color: var(--color-divider);
  padding: 15px 0;
  font-size: 13px;
  color: var(--color-text);
  p {
    margin-top: 12px;
    font-size: 12px;
    line-height: 18px;
    color: var(--color-text-info);
  }
}
li.active {
  font-weight: bold;
}

button {
  border: none;
  background: no-repeat url(../src/assets/icon-arrow-down.svg);
  height: 7px;
  align-self: center;
}
</style>
