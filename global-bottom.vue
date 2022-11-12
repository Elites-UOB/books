<template>
    <footer
      translate-y="-50%"
      translate-x="-50%"
      class="absolute bottom-[10mm] left-[50%] text-black"
      :class="[ $slidev.nav.currentRoute.meta?.hidePageNumber ? 'invisible' : '' ]"
    > 
      {{$slidev.nav.currentPage}}
    </footer>
  </template>