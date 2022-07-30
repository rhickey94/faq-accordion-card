<script setup>
import { ref } from "vue";

defineProps({
  header: {
    type: String,
    required: true,
  },
  body: {
    type: String,
    required: true,
  },
});

const isActive = ref(false);

function resetDropdown() {
  [...document.querySelectorAll(".panel")].forEach((panel) => {
    panel.style.maxHeight = null;
  });
  [...document.querySelectorAll(".faq-header")].forEach((header) => {
    header.classList.remove("active");
  });
}

function toggleDropdown(e) {
  isActive.value = !isActive.value;
  resetDropdown();
  const header = e.currentTarget.querySelector(".faq-header");
  header.classList.add("active");

  const panel = e.currentTarget.nextElementSibling;
  const { maxHeight } = window.getComputedStyle(panel);
  if (maxHeight === "0px") {
    panel.style.maxHeight = `${panel.scrollHeight}px`;
  } else {
    panel.style.maxHeight = null;
  }
}
</script>
<template>
  <li>
    <button @click="toggleDropdown">
      <span class="faq-header">{{ header }}</span>
      <span :class="{ activeArrow: isActive }" class="arrow"></span>
    </button>
    <div class="panel">
      <p>
        {{ body }}
      </p>
    </div>
  </li>
</template>
<style lang="scss" scoped>
li {
  border-bottom: 1px solid;
  border-color: var(--color-divider);
  padding: 15px 0;
  button {
    color: var(--color-text);
    border: none;
    background: none;
    font: 13px "Kumbh Sans";
    padding: 0;
    width: 100%;
    display: flex;
    justify-content: space-between;
  }
  p {
    margin-top: 12px;
    font-size: 12px;
    line-height: 18px;
    color: var(--color-text-info);
  }
}
.arrow {
  border: none;
  background: no-repeat url(../assets/icon-arrow-down.svg);
  height: 7px;
  width: 10px;
  align-self: center;
  transition: transform 0.35s ease-in-out;
}

.activeArrow {
  transform: rotate(180deg);
}
.panel {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.35s ease-in-out;
}

.active {
  font-weight: bold;
}

@media screen and (min-width: 1440px) {
  li {
    button {
      font: 14px "Kumbh Sans";
    }
  }
}
</style>
