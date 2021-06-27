<template>
  <div class="min-h-screen dark:bg-gradient-to-tr from-gray-700 via-gray-900 to-black relative bg-white overflow-hidden">
    <div
      class="hidden sm:block sm:absolute sm:inset-y-0 sm:h-full sm:w-full"
    >
      <div class="relative h-full max-w-7xl mx-auto">
        <svg
          class="
              absolute
              right-full
              transform
              translate-y-1/4 translate-x-1/4
              lg:translate-x-1/2
            "
          width="404"
          height="784"
          fill="none"
          viewBox="0 0 404 784"
        >
          <defs>
            <pattern
              id="f210dbf6-a58d-4871-961e-36d5016a0f49"
              x="0"
              y="0"
              width="20"
              height="20"
              patternUnits="userSpaceOnUse"
            >
              <rect
                x="0"
                y="0"
                width="4"
                height="4"
                class="text-gray-400"
                fill="currentColor"
              />
            </pattern>
          </defs>
          <rect
            width="404"
            height="784"
            fill="url(#f210dbf6-a58d-4871-961e-36d5016a0f49)"
          />
        </svg>
        <svg
          class="
              absolute
              left-full
              transform
              -translate-y-3/4 -translate-x-1/4
              md:-translate-y-1/2
              lg:-translate-x-1/2
            "
          width="404"
          height="784"
          fill="none"
          viewBox="0 0 404 784"
        >
          <defs>
            <pattern
              id="5d0dd344-b041-4d26-bec4-8d33ea57ec9b"
              x="0"
              y="0"
              width="20"
              height="20"
              patternUnits="userSpaceOnUse"
            >
              <rect
                x="0"
                y="0"
                width="4"
                height="4"
                class="text-gray-400"
                fill="currentColor"
              />
            </pattern>
          </defs>
          <rect
            width="404"
            height="784"
            fill="url(#5d0dd344-b041-4d26-bec4-8d33ea57ec9b)"
          />
        </svg>
      </div>
    </div>
    <div class="relative pt-6 pb-12 sm:pb-22">
      <Popover>
        <div class="max-w-7xl mx-auto px-4 sm:px-6">
          <nav
            class="relative flex items-center justify-between sm:h-10 md:justify-center"
            aria-label="Global"
          >
            <div class="flex items-center flex-1 md:absolute md:inset-y-0 md:left-0">
              <div class="flex items-center justify-between w-full md:w-auto">
                <router-link to="/">
                  <span class="sr-only">Workflow</span>
                  <LogoRepo />
                </router-link>
              </div>
            </div>
            <div class="hidden md:flex md:space-x-10">
              <router-link
                v-for="item in navigation"
                :key="item.name"
                :to="item.path"
                class="font-medium text-gray-500 hover:text-gray-900"
              >
                {{ item.name }}
              </router-link>
            </div>
          </nav>
        </div>
      </Popover>

      <main class="mt-16 mx-auto max-w-7xl px-4 sm:mt-24">
        <div class="text-center">
          <h1
            class="
                text-4xl
                tracking-tight
                font-extrabold
                text-gray-900
                sm:text-5xl
                md:text-6xl
              "
          >
            <span class="text-gray-400 xl:mx-10 l:mx-7 md:mx-4 sm:mx-1 text-6xl block xl:inline">Veterinary Nursing</span><br />
            {{ " " }}
            <span
              class="text-5xl block text-gray-700 xl:inline"
            >Emergency Edition</span>
          </h1>
          <p
            class="
                mt-3
                max-w-md
                mx-auto
                text-base text-gray-500
                sm:text-lg
                md:mt-5 md:text-xl md:max-w-3xl
              "
          >
            Helping Vets to Save Pets
          </p>
        </div>
      </main>
    </div>
  </div>
</template>

<script setup lang="ts">
const navigation = [
  { name: 'Triage', path: '/triage' },
  { name: 'Initial Assessment', path: '/exam-one' },
  { name: 'Diagnsotics', path: '/exam-2' },
]
</script>
