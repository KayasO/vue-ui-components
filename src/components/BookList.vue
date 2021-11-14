<template>
  <div id="books">
    <h1>Books</h1>
    <ul>
      <li v-for="book in books" :key="book.title">
        <h3>{{ book.author }}</h3>
        <p>{{ book.title }}</p>
        <img :src="book.img" :alt="book.title" />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Counter',
  data() {
    return {
      books: [
        {
          author: 'Test1',
          title: 'Some title 1',
          img: '../assets/book-covers/1.jpg',
          isFav: true,
        },
        {
          author: 'Test2',
          title: 'Some title 2',
          img: '../assets/book-covers/2.jpg',
          isFav: false,
        },
        {
          author: 'Test3',
          title: 'Some title 3',
          img: '../assets/book-covers/3.jpg',
          isFav: false,
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
