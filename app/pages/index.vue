<script setup lang="ts">
import { Button } from "~/components/ui/button";
import { LucideIcon } from "~/components/ui/lucide-icon";

const features = [
  {
    icon: "i-lucide-rocket",
    title: "Production-ready from day one",
    description: "Pre-configured with TypeScript, ESLint, Tailwind CSS, and all the best practices. Focus on building features, not setting up tooling.",
  },
  {
    icon: "i-lucide-sparkles",
    title: "Beautiful by default",
    description: "Leveraging shadcn-vue's design system with automatic dark mode, consistent spacing, and polished components that look great out of the box.",
  },
  {
    icon: "i-lucide-zap",
    title: "Lightning fast",
    description: "Optimized for performance with SSR/SSG support, automatic code splitting, and edge-ready deployment. Your users will love the speed.",
  },
  {
    icon: "i-lucide-code-xml",
    title: "Own the components",
    description: "shadcn-vue components live in your project as source code. Read them, customize them, and adapt them to your design — no vendor lock-in.",
  },
  {
    icon: "i-lucide-terminal",
    title: "Developer experience first",
    description: "Auto-imports, hot module replacement, and TypeScript support. Write less boilerplate and ship more features.",
  },
  {
    icon: "i-lucide-shield-check",
    title: "Built for scale",
    description: "Enterprise-ready architecture with proper error handling, SEO optimization, and security best practices built-in.",
  },
];
</script>

<template>
  <div>
    <section class="container py-20 md:py-28">
      <div class="mx-auto max-w-3xl text-center">
        <h1 class="mx-auto max-w-[20ch] text-4xl font-semibold tracking-tight text-balance md:text-6xl">
          Stackhacker UI Starter Template
        </h1>
        <p class="text-muted-foreground mx-auto mt-6 max-w-[56ch] text-lg text-pretty">
          A production-ready starter template powered by shadcn-vue. Build beautiful, accessible, and performant applications in minutes, not hours.
        </p>
        <div class="mt-8 flex flex-wrap items-center justify-center gap-3">
          <Button
            as="a"
            href="https://ui.stackhacker.io/docs/getting-started"
            target="_blank"
            rel="noopener noreferrer"
            variant="default"
          >
            Get started
            <LucideIcon
              name="i-lucide-arrow-right"
              class="size-4"
              aria-hidden="true"
            />
          </Button>
          <Button
            as="a"
            href="https://github.com/stackhacker-ui/starter"
            target="_blank"
            rel="noopener noreferrer"
            variant="outline"
          >
            <Icon
              name="mdi:github"
              size="26"
              class="shrink-0"
              aria-hidden="true"
            />
            Use this template
          </Button>
        </div>
      </div>
    </section>

    <section class="border-grid border-t">
      <div class="container py-16 md:py-20">
        <div class="mx-auto mb-12 max-w-2xl text-center">
          <h2 class="mx-auto max-w-[35ch] text-3xl font-semibold tracking-tight text-balance md:text-4xl">
            Everything you need to build modern Nuxt apps
          </h2>
          <p class="text-muted-foreground mx-auto mt-4 max-w-[56ch] text-pretty">
            Start with a solid foundation. This template includes all the essentials for building production-ready applications with shadcn-vue's powerful component system.
          </p>
        </div>

        <dl class="mx-auto grid max-w-5xl gap-x-10 gap-y-10 md:grid-cols-2 lg:grid-cols-3">
          <div
            v-for="feature in features"
            :key="feature.title"
          >
            <dt class="text-foreground flex items-center gap-3 text-base font-medium">
              <LucideIcon
                :name="feature.icon"
                class="text-muted-foreground size-5 shrink-0"
                aria-hidden="true"
              />
              <span>{{ feature.title }}</span>
            </dt>
            <dd class="text-muted-foreground mt-2 max-w-[56ch] text-sm leading-relaxed text-pretty">
              {{ feature.description }}
            </dd>
          </div>
        </dl>
      </div>
    </section>

    <section class="border-grid container border-t py-16 md:py-20">
      <div class="bg-muted/40 border-grid mx-auto max-w-4xl rounded-xl border p-8 text-center md:p-12">
        <h2 class="mx-auto max-w-[35ch] text-3xl font-semibold tracking-tight text-balance">
          Ready to build your next Nuxt app?
        </h2>
        <p class="text-muted-foreground mx-auto mt-4 max-w-[56ch] text-pretty">
          Join thousands of developers building with Nuxt and shadcn-vue. Get this template and start shipping today.
        </p>
        <div class="mt-8 flex flex-wrap items-center justify-center gap-3">
          <Button
            as="a"
            href="https://ui.stackhacker.io/docs/getting-started"
            target="_blank"
            rel="noopener noreferrer"
            variant="default"
          >
            Start building
            <LucideIcon
              name="i-lucide-arrow-right"
              class="size-4"
              aria-hidden="true"
            />
          </Button>
          <Button
            as="a"
            href="https://github.com/stackhacker-ui/starter"
            target="_blank"
            rel="noopener noreferrer"
            variant="outline"
          >
            <Icon
              name="mdi:github"
              size="26"
              class="shrink-0"
              aria-hidden="true"
            />
            View on GitHub
          </Button>
        </div>
      </div>
    </section>
  </div>
</template>
