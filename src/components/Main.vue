<template>
  <main class="main">
    <div class="container--main">
      <div class="main__inner">
        <h1 class="main__title">Рецепты</h1>
        <section class="main__first_1 first_1" id="first_1">
          <h2 class="first_1.__title">Первые блюда</h2>
          <div class="blocks">
            <first_1 />
          </div>
        </section>
        <section class="main__two_2  two_2 " id="two_2 ">
          <h2 class="first_1__title">Вторые блюда</h2>
          <div class="blocks">
            <two_2 />
          </div>
        </section>
        <section class="main__three_3 three_3" id="three_3">
          <h2 class="three_3__title">Закуски</h2>
          <div class="blocks">
            <three_3 />
          </div>
        </section>
      </div>
    </div>
  </main>
</template>

<script>
import first_1 from "@/components/first_1.vue";
import two_2 from "@/components/two_2.vue";
import three_3 from "@/components/three_3.vue";

export default {
  name: "Main",
  components: {
    first_1,
    two_2,
    three_3,
  },
  props: {},
};
</script>

<style>
</style>