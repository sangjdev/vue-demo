<template>
    <div id="single-blog">
        <h1>{{blog.title}}</h1>
        <article>{{blog.content}}</article>
        <p>Author: {{blog.author}}</p>
        <ul>
            <li v-for="(category,i) in blog.categories" :key='i'>{{category}}</li>
        </ul>
    </div>
</template>

<script>
export default {
  data() {
      return {
          id: this.$route.params.id,
          blog: {}
      }
  },
  created() {
      this.$http.get('https://vue-demo-ee84f.firebaseio.com/posts/' + this.id + '.json').then(function (data) {
          return data.json();
        //  console.log(data);
        //  this.blog = data.body 
      }).then(function (data) {
          this.blog = data;
          console.log(data);
      })
  }
}
</script>

<style scoped>
#single-blog{
    max-width: 960px;
    margin: 0 auto;
}
</style>


