<template>
  <div
    class="first_1__block block"
    v-for="(t, id) in title"
    :key="t.title"
  >
    <h3 class="block__title">{{ title[id] }}</h3>
    <p class="block__description">
      {{ description[id] }}
    </p>
    <div class="block__button button">
      <button v-on:click="deleteBlock(id)">Удалить</button>
    </div>
  </div>
  <form action="#" class="main__form form">
<h3 class="form__title">Добавьте свой пост</h3>

<label class="form__label" for="title">Название поста:</label>
<input
class="form__input"
type="text"
placeholder="Введите название"
id="title"
name="title"
v-model="newTitle"
/>
<label class="form__label" for="description">Описание поста</label>
<textarea
class="form__input"
placeholder="Введите описание"
name="description"
id="description"
cols="30"
rows="5"
v-model="newDescription"
></textarea>
<button
type="reset"
class="form__button"
v-on:click="newPost(newTitle, newDescription)"
>
Добавить
</button>
</form>
</template>


<script>
export default {
  name: "first_1",
  components: {},
  data() {
    return {
      description: ['Куриный суп с плавленым сыром', 'Куриный суп с плавленым сыром','Куриный суп с плавленым сыром'
      ],
      title: ["Куриный суп с плавленым сыром, Куриный суп с плавленым сыром, Куриный суп с плавленым сыром"],
    };
  },
  methods: {
    deleteBlock(id) {
      this.description.splice(id, 1);
      this.title.splice(id, 1);
    },
    newPost(newTitle, newDescription) {
this.title.push(newTitle);
this.description.push(newDescription);
this.newTitle = "";
this.newDescription = "";
},
  },
  props: {},
};
</script>

<style>
</style>