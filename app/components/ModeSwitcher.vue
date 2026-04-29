<script setup lang="ts">
import { Button } from "~/components/ui/button";
import { LucideIcon } from "~/components/ui/lucide-icon";

const colorMode = useColorMode();

function toggle() {
  colorMode.preference = colorMode.value === "dark" ? "light" : "dark";
}
</script>

<template>
  <Button
    variant="ghost"
    size="icon"
    type="button"
    title="Toggle theme"
    class="text-muted-foreground hover:text-foreground"
    @click="toggle"
  >
    <span class="sr-only">Toggle theme</span>
    <LucideIcon
      name="i-lucide-moon"
      class="size-4 dark:hidden"
      aria-hidden="true"
    />
    <LucideIcon
      name="i-lucide-sun"
      class="hidden size-4 dark:block"
      aria-hidden="true"
    />
  </Button>
</template>
