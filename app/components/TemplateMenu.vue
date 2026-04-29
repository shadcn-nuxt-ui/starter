<script setup lang="ts">
import { Button } from "~/components/ui/button";
import { LucideIcon } from "~/components/ui/lucide-icon";

const items = [
  { label: "Starter", href: "https://shadcn-nuxt-ui-starter.stackhacker.io/" },
  { label: "Chat", href: "https://shadcn-nuxt-ui-chat.stackhacker.io/" },
  { label: "Docs", href: "https://shadcn-nuxt-ui.stackhacker.io/" },
];
</script>

<template>
  <details class="relative">
    <Button
      as="summary"
      variant="outline"
      size="sm"
      class="cursor-pointer"
    >
      <LucideIcon
        name="i-lucide-layout-template"
        class="size-3.5"
        aria-hidden="true"
      />
      Starter
      <LucideIcon
        name="i-lucide-chevron-down"
        class="size-3.5"
        aria-hidden="true"
      />
    </Button>
    <div class="bg-popover text-popover-foreground border-border absolute left-0 z-20 mt-2 w-56 rounded-md border p-1 shadow-md">
      <a
        v-for="item in items"
        :key="item.label"
        :href="item.href"
        target="_blank"
        rel="noopener noreferrer"
        class="hover:bg-accent hover:text-accent-foreground flex items-center gap-2 rounded-sm px-2 py-1.5 text-sm"
      >
        {{ item.label }}
        <LucideIcon
          name="i-lucide-external-link"
          class="ml-auto size-3.5 opacity-70"
          aria-hidden="true"
        />
      </a>
    </div>
  </details>
</template>
