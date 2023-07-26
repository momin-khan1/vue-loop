<script setup>
const tasks = [
  { id: 1, title: "Complete project proposal", status: "In Progress" },
  { id: 2, title: "Update website content", status: "Completed" },
  { id: 3, title: "Fix bug in user authentication", status: "In Progress" },
  { id: 4, title: "Prepare presentation slides", status: "Completed" },
  { id: 5, title: "Test new feature implementation", status: "In Progress" },
];

function inProgressTask(){
    return tasks.filter(task => 'In Progress'===task.status)
}

const person = {
    Name: 'Momin Khan',
    Age: 25,
    Occupation: 'Web developer',
    Email: 'mominkhan8828@gmail.com'

}

</script>

<template>
  <section class="mx-auto container">
    <section class="mx-auto container space-y-3">
    <h1 class="text-2xl font-bold">All Tasks</h1>
      <div
        class="p-5 border border-gray-600 text-left"
        v-for="task in tasks"
        :key="task.id"
        :class=" 'Completed'===task.status ? 'bg-red-300' : 'bg-sky-300' "
      >
       {{ task.id }} - {{ task.title }}
      </div>

      <h1 class="text-2xl font-bold mt-6">Complete Tasks</h1>
      <div class="p-5 bg-red-300 text-left text-white" v-for="task in tasks" key="task.id" v-show=" 'Completed'===task.status ">{{ task.id }} - {{ task.title }}</div>

      <h1 class="text-2xl font-bold mt-6">In Progress Tasks</h1>
      <div class="p-5 bg-orange-300 text-left" v-for="task in inProgressTask()" key="task.id">{{ task.id }} - {{ task.title }}</div>

      <h1 class="text-2xl font-bold mt-6">Object</h1>
      <div class="p-5 bg-blue-300 text-left" v-for="(value, key, index) in person" :key="key"> {{ key }} = {{ value }} </div>

    </section>
  </section>
</template>

<style scoped></style>
