<template>
  <header class="w-full bg-[#f3ede3] border-b border-stone-200/60 font-sans sticky top-0 z-50 text-[#3d271d]" dir="rtl">
    <div class="max-w-[1500px] mx-auto px-4 sm:px-8">
      
      <!--  NAV BAR -->
      <div class="flex items-center justify-between gap-10">
        
        <!-- Logo Image (INCREASED SIZE) -->
        <a href="#" class="flex items-center shrink-0">
          <img src="/urlogobg.png" alt="بوابة أور" class="h-24 md:h-28 w-auto object-contain scale-150" />
        </a>

        <!-- Nav Links -->
        <nav class="hidden lg:flex items-center justify-center gap-6 xl:gap-8 font-bold text-base xl:text-lg text-stone-800 ">
          <a href="#" class="text-[#702923] relative py-1 border-b-2 border-[#702923] shrink-0">الرئيسية</a>
          <a href="#" class="hover:text-[#702923] transition-colors py-1 shrink-0">الخدمات</a>
          
          <div class="relative group cursor-pointer py-1 flex items-center gap-1.5 hover:text-[#702923] shrink-0">
            <span>من نحن</span>
            <svg class="w-4 h-4 fill-current text-stone-600" viewBox="0 0 24 24"><path d="M7.41 8.59L12 13.17l4.59-4.58L18 10l-6 6-6-6z"/></svg>
          </div>

          <div class="relative group cursor-pointer py-1 flex items-center gap-1.5 hover:text-[#702923] shrink-0">
            <span>الأخبار</span>
            <svg class="w-4 h-4 fill-current text-stone-600" viewBox="0 0 24 24"><path d="M7.41 8.59L12 13.17l4.59-4.58L18 10l-6 6-6-6z"/></svg>
          </div>

          <div class="relative group cursor-pointer py-1 flex items-center gap-1.5 hover:text-[#702923] shrink-0">
            <span>المواقع الحكومية</span>
            <svg class="w-4 h-4 fill-current text-stone-600" viewBox="0 0 24 24"><path d="M7.41 8.59L12 13.17l4.59-4.58L18 10l-6 6-6-6z"/></svg>
          </div>

          <div class="relative group cursor-pointer py-1 flex items-center gap-1.5 hover:text-[#702923] shrink-0">
            <span>الاستفسارات</span>
            <svg class="w-4 h-4 fill-current text-stone-600" viewBox="0 0 24 24"><path d="M7.41 8.59L12 13.17l4.59-4.58L18 10l-6 6-6-6z"/></svg>
          </div>

          <div class="relative group cursor-pointer py-1 flex items-center gap-1.5 hover:text-[#702923] shrink-0">
            <span>الأسئلة الشائعة</span>
            <svg class="w-4 h-4 fill-current text-stone-600" viewBox="0 0 24 24"><path d="M7.41 8.59L12 13.17l4.59-4.58L18 10l-6 6-6-6z"/></svg>
          </div>
        </nav>

        <!-- Login Button -->
        <button class="flex items-center gap-2 bg-[#702923] hover:bg-[#5a211c] text-white px-6 py-3 rounded-full text-base font-bold shadow-md transition-all shrink-0 whitespace-nowrap">
          <svg class="w-5 h-5 fill-current" viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 3c1.66 0 3 1.34 3 3s-1.34 3-3 3-3-1.34-3-3 1.34-3 3-3zm0 14.2c-2.5 0-4.71-1.28-6-3.22.03-1.99 4-3.08 6-3.08 1.99 0 5.97 1.09 6 3.08-1.29 1.94-3.5 3.22-6 3.22z"/></svg>
          <span class="whitespace-nowrap">تسجيل الدخول</span>
        </button>

      </div>

    </div>
  </header>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>
