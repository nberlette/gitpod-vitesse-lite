<script setup lang="ts">
const name = $ref('')

const router = useRouter()
const go = () => {
  if (name)
    router.push(`/hi/${encodeURIComponent(name)}`)
}
</script>

<template>
  <div>
    <p>
      <a
        rel="noreferrer"
        href="https://github.com/nberlette/gitpod-vitesse-lite"
        target="_blank"
        inline-flex gap-4 mb-4 pb-4 px-20
        duration-700 ease-in-out transition-colors
        hover="text-[#ffae33]"
        border="b-1 gray-200 dark:gray-600"
        outline="none active:none hover:none"
     >
        <i i-carbon-campsite text-4xl flex />
        <span class="mt-2.5 op-60">+</span>
        <i i-simple-gitpod text-4xl flex class="scale-[0.8]" />
      </a>
    </p>
    <p>
      <em text-sm op75>Opinionated Vite Starter Template</em>
    </p>

    <div py-4 />

    <input
      id="input"
      v-model="name"
      placeholder="What's your name?"
      type="text"
      autocomplete="false"
      p="x-4 y-2"
      w="250px"
      text="center"
      bg="transparent"
      border="~ rounded gray-200 dark:gray-700"
      outline="none active:none"
      @keydown.enter="go"
    >

    <div>
      <button
        class="m-3 text-sm btn"
        :disabled="!name"
        @click="go"
      >
        Go
      </button>
    </div>
  </div>
</template>
