<template>
  <div id="books">
    <h1>Books</h1>
    <button @click="toggleShowBooks()">
      <span v-if="showBooks">Show books</span>
      <span v-else>Hide books</span>
    </button>

    <ul v-if="showBooks">
      <li v-for="book in books" :key="book.title" :class="{ fav: book.isFav }">
        <h3>{{ book.author }}</h3>
        <p>{{ book.title }}</p>
        <img :src="book.img" :alt="book.title" />
      </li>
    </ul>
  </div>
</template>

<script>
import image1 from '../assets/book-covers/1.jpg';
import image2 from '../assets/book-covers/2.jpg';
import image3 from '../assets/book-covers/3.jpg';

export default {
  name: 'BookList',
  data() {
    return {
      showBooks: true,
      books: [
        {
          author: 'Test1',
          title: 'Some title 1',
          img: image1,
          isFav: true,
        },
        {
          author: 'Test2',
          title: 'Some title 2',
          img: image2,
          isFav: false,
        },
        {
          author: 'Test3',
          title: 'Some title 3',
          img: image3,
          isFav: false,
        },
      ],
    };
  },
  methods: {
    toggleShowBooks() {
      this.showBooks = !this.showBooks;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
