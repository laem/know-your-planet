<template>
  <section>
    <br />

    <div>
      <router-link class="no-decoration" v-for="category in categories" :key="category.name" :to="{ name: 'category-detail', params: { categoryName: category.name } }">
        <span class="category">
          <h3>{{ category.name }}</h3>
          <p><strong>{{ category.question_count }}</strong> question<span v-if="category.question_count > 1">s</span></p>
        </span>
      </router-link>
    </div>

    <br />
    <hr v-if="categories" />
    <div v-if="categories" class="row actions">
      <div class="col-sm">
        <router-link :to="{ name: 'question-list' }">
          Toutes les questions
        </router-link>
        <br />
      </div>
      <div class="col-sm">
        <router-link :to="{ name: 'about' }">
          ℹ️&nbsp;À propos de cette application
        </router-link>
        <br />
      </div>
      <div class="col-sm">
        <HomeLink />
      </div>
    </div>
  </section>
</template>

<script>
import HomeLink from '../components/HomeLink.vue'

export default {
  name: 'CategoryListPage',
  components: {
    HomeLink
  },

  data () {
    return {
      categories: null,
      loading: false,
      error: null,
    }
  },

  mounted () {
    this.fetchCategories();
  },

  methods: {
    fetchCategories() {
      this.error = this.categories = null;
      this.loading = true;
      fetch(`${process.env.VUE_APP_API_ENDPOINT}/categories`)
        .then(response => {
          this.loading = false
          return response.json()
        })
        .then(data => {
          this.categories = data;
        })
        .catch(error => {
          console.log(error)
          this.error = error;
        })
    },
  }
}
</script>

<style scoped>
.category {
  width: 300px;
  display: inline-block;
  border: 1px solid var(--secondary);
  border-radius: 5px;
  margin: 2.5px;
  padding: 5px;
  cursor: pointer;
}
.category-active {
  background-color: #f88787;
  text-shadow: 0px 0px 1px black;
}
</style>
