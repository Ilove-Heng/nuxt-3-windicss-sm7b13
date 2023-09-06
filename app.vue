<template>
  <div class="">
    <div
      justify="center"
      h="screen"
      class="
        flex flex-col
        h-screen
        bg-gradient-to-b
        from-blue-50
        to-blue-300
        space-y-2
      "
    >
      <figure>
        <img
          class="
            mx-auto
            max-w-full
            w-auto
            max-h-120px
            block
            select-none
            transform
          "
          src="https://windicss.org/assets/logo.svg"
          alt="Windi CSS logo"
        />
      </figure>
      <div class="text-center">
        <h1 class="some-class">Windi CSS</h1>
        <p class="m-0 mt-1 text-lg opacity-75 leading-6 px-4 sm:text-xl">
          Next generation utility-first CSS framework.
        </p>
        <div class="flex space-x-4 mt-8 justify-center">
          <a
            href="https://windicss.org/guide/"
            target="_blank"
            class="
              inline-flex
              items-center
              justify-center
              px-3
              py-2
              border border-transparent
              rounded-md
              bg-blue-500
              hover:bg-primary-600
              shadow-sm
              text-base text-white
              font-medium
              transition
              duration-50
              ring-primary
              focus:ring-3
              ring-opacity-50
              text-base
              px-3
              py-2.5
              md:text-lg md:px-4 md:py-3
              border-2
            "
            ><!----><!--[-->Get Started hi
            <!--]--></a
          ><a
            href="https://windicss.org/features/"
            target="_blank"
            class="
              inline-flex
              items-center
              justify-center
              px-3
              py-2
              border border-transparent
              rounded-md
              bg-blue-500
              hover:bg-primary-600
              shadow-sm
              text-base text-white
              font-medium
              transition
              duration-50
              ring-primary
              focus:ring-3
              ring-opacity-50
              border border-primary
              text-primary
              hover:text-gray-100
              text-base
              px-3
              py-2.5
              md:text-lg md:px-4 md:py-3
              border-2
            "
            ><!----><!--[-->Learn More<!--]--></a
          >
        </div>
      </div>
    </div>
  </div>

  <main>
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
