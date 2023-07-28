<script setup>
const persons = [
  {
    id: 1,
    name: "Jane Doe",
    title: "CEO-Founder",
    img: "https://tailus.io/sources/blocks/classic/preview/images/woman1.jpg"
  },
  {
    id: 2,
    name: "Jane Doe",
    title: "Chief Technical Officer",
    img: "https://tailus.io/sources/blocks/classic/preview/images/man.jpg"
  },
  {
    id: 3,
    name: "Jessy Doe",
    title: "Chief Operations Officer",
    img: "https://tailus.io/sources/blocks/classic/preview/images/woman.jpg"
  },
]
</script>

<template>
  <div class="py-20 bg-gray-50">
        <div class="container mx-auto px-6 px-32">
            <div class="mb-16 text-center">
                <h2 class="mb-4 text-center text-2xl text-gray-900 font-bold text-4xl">Team Member</h2>
                <p class="text-gray-600 w-8/12 mx-auto">Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni deleniti veniam laudantium itaque perferendis dolor maxime incidunt voluptatem. </p>
            </div>
            <div class="grid gap-12 items-center grid-cols-3">
                <div class="space-y-4 text-center" v-for="person in persons" key="key.id">
                    <img class="w-64 mx-auto object-cover rounded-xl w-64 h-64" :src="person.img" :class=" 2===person.id ? 'h-80' : 'h-64' ">
                    <div>
                        <h4 class="text-2xl">{{ person.name }}</h4>
                        <span class="block text-sm text-gray-500">{{ person.title }}</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped></style>
