<template>
  <section class="table-item">
    <h2 class="table-item__hl">All Books</h2>
    <table class="table-item__table">
      <thead>
        <tr>
          <th class="table-item__table-head-name">Name</th>
          <th class="table-item__table-head--isbn">ISBN</th>
          <th class="table-item__table-head-actions">Action</th>
          <th class="table-item__table-head-actions">Empty</th>
        </tr>
      </thead>
      <BookListRow :books="books"></BookListRow>
    </table>
  </section>
</template>

<script>
import BookListRow from "@/components/BookListRow.vue";

export default {
  components: {
    BookListRow,
  },
  name: "BookList",
  props: {
    books: Object,
  },
};
</script>

<style scoped>
.table-item__table {
  border-collapse: collapse;
  margin: 25px 0;
  font-size: 0.9em;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
  width: 100%;
}
.table-item__table-head-name {
  width: 65%;
}
.table-item__table-head-isbn {
  width: 20%;
}
.table-item__table-head-actions {
  width: 15%;
}
.table-item__table-row button {
  opacity: 0;
  padding: 5px;
  transition: opacity 500ms;
  cursor: pointer;
  border-radius: 5px;
}

.table-item__table-row:hover button {
  opacity: 1;
}
.table-item__table thead tr {
  background-color: var(--primary);
  color: #ffffff;
  text-align: left;
}
.table-item__table th,
.table-item__table td {
  padding: 12px 15px;
}
.table-item__table tbody tr {
  border-bottom: 1px solid #dddddd;
}
.table-item__table tbody tr:nth-of-type(even) {
  background-color: #f3f3f3;
}
.table-item__table tbody tr:last-of-type {
  border-bottom: 2px solid var(--primary);
}
.table-item__table tbody tr.active-row {
  font-weight: bold;
  color: var(--primary);
}
.table-item__hl {
  margin-top: 1rem;
  padding-bottom: 0.4rem;
  border-bottom: 2px solid var(--primary-dark);
}
</style>
