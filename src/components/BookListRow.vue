<template>
  <tbody>
    <tr v-for="book in books" :key="book.isbn" class="table-item__table-row">
      <td>{{ book.title }}</td>
      <td>{{ book.isbn }}</td>
      <td><BaseButton text="Add Bookmark" variant="secondary"></BaseButton></td>
    </tr>
  </tbody>
</template>

<script>
import BaseButton from "@/components/BaseButton.vue";
export default {
  name: "BookListRow",
  components: {
    BaseButton,
  },
  props: {
    books: Object,
  },
};
</script>
<style>
.table-item__table td {
  padding: 12px 15px;
}
</style>
