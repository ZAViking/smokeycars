<script setup lang="ts">
    const isOpen = ref(false)
</script>

<style scoped>
  .button-container {
    display: flex; /* Enables flexbox */
    justify-content: flex-end; /* Aligns content to the right */
    padding-right: 20px; /* Adds padding from the right side */
  }
</style>

<template>
  <div class="button-container">
    <UButton label="Quick Navigation" @click="isOpen = true" />

    <USlideover v-model="isOpen">
      <UCard
        class="flex flex-col flex-1"
        :ui="{ body: { base: 'flex-1' }, ring: '', divide: 'divide-y divide-grey-100 dark:divide-grey-800' }"
      >
        <template #header>
          <!-- <UButton
            color="gray"
            variant="ghost"
            size="sm"
            icon="i-heroicons-x-mark-20-solid"
            class="flex sm:hidden absolute end-5 top-5 z-10"
            square
            padded
            @click="isOpen = false"
          /> -->
          <UButton color="gray" variant="ghost" icon="i-heroicons-x-mark-20-solid" class="-my-1" @click="isOpen = false" />

          <div class="h-8"></div>
        </template>

          <Placeholder class="h-full" />
          <UDivider
            label="Navigation"
            :ui="{ label: 'text-white dark:text-white' }"
          />
          <NuxtLink to="/">Home</NuxtLink><br />
          <NuxtLink to="/About">About</NuxtLink><br />
          <UDivider
            label="FiveM Car Development"
            :ui="{ label: 'text-white dark:text-white' }"
          />
          <NuxtLink to="/fivem-cars/car-handling">Car Handling Guide</NuxtLink><br />
          <NuxtLink to="/fivem-cars/">Nothing</NuxtLink><br />
          
        <template #footer>
          <div class="h-8"></div>
        </template>

      </UCard>
    </USlideover>
    
  </div>
</template>