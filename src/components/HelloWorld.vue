<template>
  <div class="personal-blog">
    <h1>{{ title }}</h1>
    <p>{{ description }}</p>
    <h3>About Me</h3>
    <p>{{ about }}</p>
    <h3>Latest Posts</h3>
    <ul>
      <li v-for="post in posts" :key="post.id">
        <a :href="post.link">{{ post.title }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'PersonalBlogIntro',
  props: {
    title: String,
    description: String,
    about: String,
    posts: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-size: 2em;
  margin-bottom: 20px;
}
p {
  font-size: 1.2em;
  line-height: 1.6;
  margin: 10px 0;
}
h3 {
  margin: 30px 0 10px;
  color: #333;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 10px 0;
}
a {
  color: #42b983;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
</style>
