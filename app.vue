<template>
  <div :class="{ dark: darkMode }">
    <div class="min-h-full">
      <div
        class="grid grid-cols-12 m-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-5"
      >
        <!-- Left Sidebar -->
        <div class="hidden bg-red-500 md:block xl-col-span-1 xl:col-span-2">
          <div class="sticky top-0">
            <SidebarLeft />
          </div>
        </div>
        <!-- Main Content -->
        <!-- Main Content -->
        <!-- Left Sidebar -->
        <!-- Right Sidebar -->
        <!-- Right Sidebar -->
      </div>
    </div>
  </div>
</template>

<script setup>
const darkMode = ref(true);
</script>
