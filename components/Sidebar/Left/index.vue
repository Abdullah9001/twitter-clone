<template>
  <div class="flex flex-col h-screen">
    <div
      class="p-2 m-2 hover:bg-blue-50 rounded-full w-min dark:hover:bg-white/20"
      :class="defaultTransition"
    >
      <NuxtLink to="/">
        <div class="w-8 h-8">
          <LogoTwitter />
        </div>
      </NuxtLink>
    </div>

    <div>
      <SidebarLeftTab active>
        <template v-slot:icon>
          <HomeIcon />
        </template>
        <template v-slot:name>Home</template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
          <MagnifyingGlassIcon />
        </template>
        <template v-slot:name>Explore</template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
          <BellIcon />
        </template>
        <template v-slot:name>Notification</template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
          <EnvelopeIcon />
        </template>
        <template v-slot:name>Messages</template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
          <DocumentTextIcon />
        </template>
        <template v-slot:name>List</template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
          <BookmarkIcon />
        </template>
        <template v-slot:name>Bookmarks</template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
          <UserIcon />
        </template>
        <template v-slot:name>Profile</template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
          <EllipsisHorizontalCircleIcon />
        </template>
        <template v-slot:name>More</template>
      </SidebarLeftTab>
    </div>
  </div>
</template>

<script setup>
import { HomeIcon } from "@heroicons/vue/24/solid";
import {
  MagnifyingGlassIcon,
  BellIcon,
  EnvelopeIcon,
  DocumentTextIcon,
  BookmarkIcon,
  UserIcon,
  EllipsisHorizontalCircleIcon,
} from "@heroicons/vue/24/outline";
const { defaultTransition } = useTailwindConfig();
</script>
