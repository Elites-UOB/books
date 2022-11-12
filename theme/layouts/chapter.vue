<template>
    <div class="slidev-layout" flex="~ col" justify="end" :style="`background: ${$slidev.nav.currentRoute.meta.themeConfig?.primary}`">
        <div flex="~ col gap-10" h="3xl">
            <span text="4rem" :style="`color: ${$slidev.nav.currentRoute.meta.themeConfig?.textSecondary}`">
                الفصل {{$slidev.nav.currentRoute.meta?.chapterNumber}}
            </span>
            <span text="10rem" font="bold">
                {{$slidev.nav.currentRoute.meta?.slide?.title}}
            </span>
            
            <div mt="10">
                <slot />
            </div>
        </div>
    </div>
</template>

<style scoped>
h1 {
    font-size: 12rem;
    font-weight: 700;
}
</style>
  