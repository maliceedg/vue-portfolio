<template>
  <div class="min-h-screen flex items-center justify-center bg-gray-50 py-12 px-4 sm:px-6 lg:px-8">
    <div class="max-w-md w-full space-y-8">
      <div>
        <img
          class="mx-auto h-12 w-auto"
          src="https://tailwindui.com/img/logos/workflow-mark-indigo-600.svg"
          alt="Workflow"
        />
        <h2 class="mt-6 text-center text-3xl font-extrabold text-gray-900">Create a new account</h2>
      </div>
      <form class="mt-8 space-y-6" action="#" method="POST">
        <input type="hidden" name="remember" value="true" />
        <div v-if="step === 0" class="rounded-md -space-y-px">
          <div class="flex items-center justify-between w-full">
            <label for="name" class="sr-only">Name</label>
            <input
              id="name"
              name="name"
              type="text"
              autocomplete="name"
              v-model="form.name"
              class="appearance-none relative block w-1/2 px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm mb-2"
              placeholder="Name"
            />
            <div class="input-errors" v-for="error of v$.name.$errors" :key="error.$uid">
              <div class="error-msg">{{ error.$message }}</div>
            </div>
            <label for="lastname" class="sr-only">Appellido</label>
            <input
              id="lastname"
              name="lastname"
              type="text"
              autocomplete="lastname"
              required
              class="appearance-none relative block w-1/2 px-3 py-2 ml-3 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm mb-2"
              placeholder="Lastname"
            />
          </div>
          <div>
            <label for="identification" class="sr-only">Id</label>
            <input
              id="identification"
              name="identification"
              type="text"
              autocomplete="identification"
              required
              class="appearance-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm mb-2"
              placeholder="Identification"
            />
          </div>
          <div>
            <label for="birthdate" class="sr-only">Id</label>
            <input
              id="birthdate"
              name="birthdate"
              type="date"
              autocomplete="birthdate"
              required
              class="appearance-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm mb-2"
              placeholder="Birth Date"
            />
          </div>
          <div>
            <label for="avatar" class="sr-only">Id</label>
            <input
              id="avatar"
              name="avatar"
              type="file"
              autocomplete="avatar"
              required
              accept="image/png, image/jpeg"
              class="appearance-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm mb-2"
              placeholder="Image"
            />
          </div>
          <div class="flex justify-evenly py-5">
            <button
              type="button"
              class="group relative w-25 flex justify-center py-2 px-4 border border-transparent text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
              @click="counter('next')"
            >
              Next
              <span class="absolute right-0 inset-y-0 flex items-center pl-3 text-light-50">
                <!-- Heroicon name: solid/lock-closed -->
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="text-white mr-3"
                  fill="currentColor"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                >
                  <path d="M6.028 0v6.425l5.549 5.575-5.549 5.575v6.425l11.944-12z" />
                </svg>
              </span>
            </button>
          </div>
        </div>

        <div v-else-if="step === 1" class="rounded-md -space-y-px">
          <div class="flex items-center justify-between w-full">
            <label for="address" class="sr-only">Address</label>
            <input
              id="address"
              name="address"
              type="text"
              autocomplete="address"
              required
              class="appearance-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm mb-2"
              placeholder="Address"
            />
          </div>
          <div class="flex items-center justify-between w-full">
            <select
              id="state"
              name="state"
              v-model="selections.state"
              class="relative block w-1/2 px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm mb-2"
            >
              <option selected>Choose your state</option>
              <option v-for="state in data" :key="state.estado">{{ state.estado }}</option>
            </select>
            <select
              id="city"
              name="city"
              v-model="selections.municipality"
              class="relative block w-1/2 px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm mb-2"
            >
              <option selected>Choose your city</option>
              <option v-for="muni in municipalities" :key="muni.municipio">{{ muni.municipio }}</option>
            </select>
          </div>
          <div class="flex items-center justify-between py-5">
            <button
              type="button"
              class="group relative w-30 flex justify-center py-2 px-4 border border-transparent text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
              @click="counter('prev')"
            >
              <span class="absolute left-0 inset-y-0 flex items-center pr-3 text-light-50">
                <!-- Heroicon name: solid/lock-closed -->
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="text-white ml-3"
                  fill="currentColor"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                >
                  <path d="M16.67 0l2.83 2.829-9.339 9.175 9.339 9.167-2.83 2.829-12.17-11.996z" />
                </svg>
              </span>
              Previous
            </button>
            <button
              type="button"
              class="group relative w-25 flex justify-center py-2 px-4 border border-transparent text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
              @click="counter('next')"
            >
              Next
              <span class="absolute right-0 inset-y-0 flex items-center pl-3 text-light-50">
                <!-- Heroicon name: solid/lock-closed -->
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="text-white mr-3"
                  fill="currentColor"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                >
                  <path d="M6.028 0v6.425l5.549 5.575-5.549 5.575v6.425l11.944-12z" />
                </svg>
              </span>
            </button>
          </div>
        </div>
        <div v-else class="rounded-md -space-y-px">
          <div class="flex items-center justify-between w-full">
            <div class="flex items-center justify-between w-full">
              <label for="email" class="sr-only">Email</label>
              <input
                id="email"
                name="email"
                type="email"
                autocomplete="email"
                required
                class="appearance-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm mb-2"
                placeholder="Email"
              />
            </div>
          </div>
          <div class="flex items-center justify-between w-full">
            <div class="flex items-center justify-between w-full">
              <label for="password" class="sr-only">Password</label>
              <input
                v-model="form.password"
                id="password"
                name="password"
                type="password"
                required
                class="appearance-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm mb-2"
                placeholder="Password"
              />
              <!-- Error Message -->
              <div
                class="input-errors"
                v-for="error of v$.passwordConfirmation.$errors"
                :key="error.$uid"
              >
                <div class="error-msg">{{ error.$message }}</div>
              </div>
            </div>
          </div>
          <div class="flex items-center justify-between w-full">
            <div class="flex items-center justify-between w-full">
              <label for="passwordConfirmation" class="sr-only">Password Confirmation</label>
              <input
                v-model="form.passwordConfirmation"
                id="passwordConfirmation"
                name="passwordConfirmation"
                type="password"
                required
                class="appearance-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm mb-2"
                placeholder="Password Confirmation"
              />
              <!-- Error Message -->
              <div
                class="input-errors"
                v-for="error of v$.passwordConfirmation.$errors"
                :key="error.$uid"
              >
                <div class="error-msg">{{ error.$message }}</div>
              </div>
            </div>
          </div>
          <div class="flex items-center justify-between py-5">
            <button
              type="button"
              class="group relative w-30 flex justify-center py-2 px-4 border border-transparent text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
              @click="counter('prev')"
            >
              <span class="absolute left-0 inset-y-0 flex items-center pr-3 text-light-50">
                <!-- Heroicon name: solid/lock-closed -->
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="text-white ml-3"
                  fill="currentColor"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                >
                  <path d="M16.67 0l2.83 2.829-9.339 9.175 9.339 9.167-2.83 2.829-12.17-11.996z" />
                </svg>
              </span>
              Previous
            </button>
            <button
              type="submit"
              class="group relative w-30 flex justify-center py-2 px-4 border border-transparent text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
            >
              <span class="absolute left-0 inset-y-0 flex items-center px-3">
                <!-- Heroicon name: solid/lock-closed -->
                <svg
                  class="h-5 w-5 text-indigo-500 group-hover:text-indigo-400"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                  aria-hidden="true"
                >
                  <path
                    fill-rule="evenodd"
                    d="M5 9V7a5 5 0 0110 0v2a2 2 0 012 2v5a2 2 0 01-2 2H5a2 2 0 01-2-2v-5a2 2 0 012-2zm8-2v2H7V7a3 3 0 016 0z"
                    clip-rule="evenodd"
                  />
                </svg>
              </span>
              Sign in
            </button>
          </div>
        </div>
        <div class="flex items-center justify-between">
          <router-link class="text-sm" to="/login">
            <a href="#" class="font-medium text-indigo-600 hover:text-indigo-500">Or login?</a>
          </router-link>
        </div>
      </form>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { useFetch } from '@vueuse/core'
import useVuelidate from '@vuelidate/core'
import { required, email, minLength } from '@vuelidate/validators'

// States and Cities Api
const url = 'https://raw.githubusercontent.com/CodersVenezuela/Venezuela-JSON/master/venezuela.json'
const { data } = useFetch(url).get().json()

// States and Cities Computed
const selections = reactive({
  state: '',
  municipality: ''
})
const municipalities = computed(() => data.value.find(({ estado }) => selections.state === estado)?.municipios)

const rules = {
  name: { required },
  lastname: { required },
  identification: { required },
  birthdate: { required },
  avatar: { required },
  address: { required },
  state: { required },
  city: { required },
  email: { required, email },
  password: { required, min: minLength(8) },
  passwordConfirmation: { required }
}

const form = reactive({
  name: '',
  lastname: '',
  identification: '',
  birthdate: '',
  avatar: '',
  address: '',
  state: '',
  city: '',
  email: '',
  password: '',
  passwordConfirmation: '',
})

const v$ = useVuelidate(rules, form)

const step = ref(0)
function counter(type: any) {
  if (type === 'prev') step.value--
  else step.value++
}

</script>
