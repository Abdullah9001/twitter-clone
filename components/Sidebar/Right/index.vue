<template>
  <div class="flex flex-col">
    <!-- Preview Card : Trends For You -->
    <SidebarRightPreviewCard title="Trends For You">
      <SidebarRightPreviewCardItem
        v-for="trendForyou in trendForyouItems"
        :key="trendForyou"
      >
        <div>
          <h2 class="font-bold text-gray-800 text-md dark:text-white">
            {{ trendForyou.title }}
          </h2>
          <p class="text-xs text-gray-400">{{ trendForyou.count }}</p>
        </div>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>
    <!-- Preview Card : Who to follow -->
    <SidebarRightPreviewCard title="Who to follow">
      <SidebarRightPreviewCardItem
        v-for="whoToFollow in whoToFollowItems"
        :key="whoToFollow"
      >
        <div class="flex flex-row items-center justify-between p-2">
          <div class="flex flex-row">
            <img
              class="w-10 h-10 rounded-full"
              :src="whoToFollow.image"
              :alt="whoToFollow.name"
            />

            <div class="flex flex-col ml-2">
              <h1 class="text-sm font-bold text-gray-900 dark:text-white">
                {{ whoToFollow.name }}
              </h1>
              <p class="text-xs text-gray-400">{{ whoToFollow.handle }}</p>
            </div>
          </div>
          <div class="flex h-full">
            <button
              class="px-4 py-2 text-xs font-bold text-white bg-black rounded-full dark:text-black dark:bg-white"
            >
              Follow
            </button>
          </div>
        </div>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>
  </div>
</template>

<script setup>
const trendForyouItems = ref([
  {
    title: "#spaceX",
    count: "18.8k tweets",
  },
  {
    title: "#codingisFun",
    count: "8.8k tweets",
  },
  {
    title: "#artbetter",
    count: "1.8k tweets",
  },
]);

const whoToFollowItems = ref([
  {
    name: "Joe Biden",
    handle: "@JoeBiden",
    image: "https://picsum.photos/200/200",
  },
  {
    name: "Joe Biden",
    handle: "@JoeBiden",
    image: "https://picsum.photos/200/200",
  },
  {
    name: "Aj Style",
    handle: "@JoeBiden",
    image: "https://picsum.photos/200/200",
  },
]);
</script>
