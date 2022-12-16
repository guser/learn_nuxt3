<template>
  <div>
    <ClientOnly>
      <!-- ... -->
      <template #fallback>
        <!-- this will be rendered on server side -->
        <p>Loading comments...</p>
      </template>
   </ClientOnly> 
  </div>
</template>

<script setup> 
useHead({  title: 'My App'})
</script>
