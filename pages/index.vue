<template>
  <main>
  <header>
    <nav>
      <ul>
        <li><NuxtLink to="/about">About</NuxtLink></li>
        <li><NuxtLink to="/posts/1">Post 1</NuxtLink></li>
        <li><NuxtLink to="/posts/2">Post 2</NuxtLink></li>
      </ul>
    </nav>
  </header>

    <listItem
      v-for="(item, index) in database"
      :name="item.name"
      :department="item.deparment"
      :salary="item.salary"
      :position="index"
      v-on:deleteItem="deleteItem"
    />
  </main>
</template>

<script setup>
let database = ref([
  {
    name: 'Johnny',
    deparment: 'Marketing',
    salary: 30000,
  },
  {
    name: 'Sarah',
    deparment: 'Engineering',
    salary: 72000,
  },
  {
    name: 'Terrance',
    deparment: 'Executive',
    salary: 125000,
  },
]);

function deleteItem(position) {
  database.value.splice(position, 1);
}
</script>

<style>
.some {
  &-class {
    @apply text-green-300;
  }
}
</style>
