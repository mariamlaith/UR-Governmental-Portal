<template>
  <section class="relative w-full h-[520px] bg-cover bg-center font-sans overflow-hidden" style="background-image: url('/urbg.png');" dir="rtl">
    <!-- Dark/Warm Overlay for readability -->
    <div class="absolute inset-0 bg-black/10"></div>

    <!-- MAIN CONTAINER: Aligned to the bottom using pb-20 -->
    <div class="relative max-w-[1500px] mx-auto h-full px-4 sm:px-8 flex flex-col justify-end items-center text-right mt-16 pb-12 md:pb-20">
      
      <!-- SEARCH BAR CONTAINER -->
      <div class="w-full max-w-3xl">
        <div class="bg-white/95 backdrop-blur-md rounded-full shadow-2xl p-1.5 flex items-center border border-stone-200">
          
          <!-- Search Button (Left in RTL layout) -->
          <button class="bg-[#702923] hover:bg-[#521d18] text-white p-3.5 rounded-full transition-colors flex items-center justify-center shrink-0">
            <svg class="w-5 h-5 fill-current" viewBox="0 0 24 24">
              <path d="M15.5 14h-.79l-.28-.27C15.41 12.59 16 11.11 16 9.5 16 5.91 13.09 3 9.5 3S3 5.91 3 9.5 5.91 16 9.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"/>
            </svg>
          </button>

          <!-- Input Text Area -->
          <input 
            type="text" 
            placeholder="ابحث عن خدمة، معاملة، أو جهة حكومية..." 
            class="w-full bg-transparent px-4 text-stone-800 text-sm md:text-base focus:outline-none text-right placeholder-stone-400 font-medium"
          />

          <!-- Categories Dropdown Button -->
          <div class="hidden sm:flex items-center gap-2 border-r border-stone-300 pr-4 pl-2 text-stone-700 hover:text-stone-900 cursor-pointer shrink-0">
            <svg class="w-5 h-5 text-[#702923]" viewBox="0 0 24 24" fill="currentColor">
              <path d="M12 7V3H2v4h10zm0 6V9H2v4h10zm0 6v-4H2v4h10zm10-12h-8v2h8V7zm0 6h-8v2h8v-2zm0 6h-8v2h8v-2z"/>
            </svg>
            <span class="text-xs md:text-sm font-bold">تصفح حسب الوزارات</span>
            <svg class="w-4 h-4 text-stone-500" viewBox="0 0 24 24" fill="currentColor">
              <path d="M7 10l5 5 5-5z"/>
            </svg>
          </div>

        </div>
      </div>

      <!-- Navigation Arrows Bottom-Left -->
      <div class="absolute bottom-6 left-8 flex items-center gap-2">
        <button class="w-9 h-9 rounded-full bg-white/80 hover:bg-white flex items-center justify-center text-stone-800 shadow transition-all">
          ‹
        </button>
        <button class="w-9 h-9 rounded-full bg-white/80 hover:bg-white flex items-center justify-center text-stone-800 shadow transition-all">
          ›
        </button>
      </div>

    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection'
}
</script>