<template>
  <Navbar></Navbar>
  <div class="flex flex-col justify-between h-auto">
    <div class="bg-gray-200 h-xl">
      <div class="flex flex-col px-10 py-12">
        <div class="-my-2 overflow-x-auto sm:-mx-6 lg:-mx-8">
          <div class="py-2 align-middle inline-block min-w-full sm:px-6 lg:px-8">
            <div class="shadow overflow-hidden border-b border-gray-200 sm:rounded-lg">
              <table class="min-w-full divide-y divide-gray-200">
                <thead class="bg-gray-50">
                  <tr>
                    <th
                      scope="col"
                      class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider"
                    >Name</th>
                    <th
                      scope="col"
                      class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider"
                    >Title</th>
                    <th
                      scope="col"
                      class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider"
                    >Status</th>
                    <th
                      scope="col"
                      class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider"
                    >Main Framework</th>
                    <th scope="col" class="relative px-6 py-3">
                      <span class="sr-only">Edit</span>
                    </th>
                  </tr>
                </thead>
                <tbody class="bg-white divide-y divide-gray-200">
                  <tr v-for="person in people" :key="person.email">
                    <td class="px-6 py-4 whitespace-nowrap">
                      <div class="flex items-center">
                        <div class="flex-shrink-0 h-10 w-10">
                          <img class="h-10 w-10 rounded-full" :src="person.image" alt />
                        </div>
                        <div class="ml-4">
                          <div class="text-sm font-medium text-gray-900">{{ person.name }}</div>
                          <div class="text-sm text-gray-500">{{ person.email }}</div>
                        </div>
                      </div>
                    </td>
                    <td class="px-6 py-4 whitespace-nowrap">
                      <div class="text-sm text-gray-900">{{ person.title }}</div>
                      <div class="text-sm text-gray-500">{{ person.department }}</div>
                    </td>
                    <td class="px-6 py-4 whitespace-nowrap">
                      <span
                        class="px-2 inline-flex text-xs leading-5 font-semibold rounded-full bg-green-100 text-green-800"
                      >Active</span>
                    </td>
                    <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">{{ person.role }}</td>
                    <td class="px-6 py-4 whitespace-nowrap text-right text-sm font-medium">
                      <a href="#" class="text-indigo-600 hover:text-indigo-900">Edit</a>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script setup lang="ts">
const people = [
  {
    name: 'Jane Cooper',
    title: 'Regional Paradigm Research',
    department: 'Optimization',
    role: 'C#',
    email: 'jane.cooper@example.com',
    image:
      'https://picsum.photos/200',
  },
  {
    name: 'Angely Tallavo',
    title: 'Neural Network Development',
    department: 'Artificial Intellingence',
    role: 'Django',
    email: 'lorem.ipsum@gmail.com',
    image:
      'https://picsum.photos/200?=1',
  },
  {
    name: 'Jesús Pérez',
    title: 'SAAS Solution',
    department: 'B2B',
    role: 'Angular',
    email: 'lorem.ipsum2@gmail.com',
    image:
      'https://picsum.photos/200?=2',
  },
  {
    name: 'Edgardo González',
    title: 'CMS Builder',
    department: 'CMS',
    role: 'Angular',
    email: 'lorem.ipsum3@gmail.com',
    image:
      'https://picsum.photos/200?=3',
  },
  {
    name: 'Cristian Palacios',
    title: 'Game of Life',
    department: 'Other',
    role: 'JS',
    email: 'lorem.ipsum4@gmail.com',
    image:
      'https://picsum.photos/200?=4',
  },
]
</script>

<style>
</style>
