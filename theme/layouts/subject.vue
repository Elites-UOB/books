<template>
    <div class="slidev-layout" h="full" flex="~ col" justify="between" :text="[$slidev.nav.currentRoute.meta?.slide?.frontmatter?.secondary ? 'gray-400' : '']">
        <h1>
            {{$slidev.nav.currentRoute.meta?.slide?.frontmatter?.subject}}
        </h1>

        <div h="2/3">
            <slot />
        </div>
    </div>
</template>

<style scoped>
h1 {
    font-size: 12rem;
    font-weight: 700;
}
</style>
  