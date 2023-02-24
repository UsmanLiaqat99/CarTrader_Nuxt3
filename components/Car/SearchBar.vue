<template>
  <div
    class="font-serif w-[750px] text-2xl rounded-full bg-white flex justify-between overflow-hidden drop-shadow-2xl mx-auto"
  >
    <input
      v-model="city"
      type="text"
      placeholder="Search by city..."
      class="py-3 px-5 w-full text-2xl rounded-full focus:outline-none"
    />
    <button @click="handleSearch" class="bg-sky-500 px-10 text-white">
      Search
    </button>
  </div>
</template>

<script setup>
const city = ref("");
const Router = useRouter();

const handleSearch = () => {
  Router.push(`/city/${city.value}/car`);
};
</script>
