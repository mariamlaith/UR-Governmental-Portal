<template>
  <section class="w-full max-w-[1500px] mx-auto px-4 sm:px-8 font-sans space-y-6" dir="rtl">
    
    <!-- TOP ROW: APP DOWNLOAD BANNER + AI ASSISTANT BANNER -->
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-4">
      
      <!-- APP DOWNLOAD BANNER (LEFT SIDE IN RTL) -->
      <div class="bg-[#faf7f2] hover:bg-white rounded-2xl p-4 border-2 border-[#e6ded5] hover:border-[#702923] shadow-md hover:shadow-xl transition-all duration-300 flex items-center justify-between relative overflow-hidden transition-all">
        <!-- Phone Mockups Image -->
        <div class="w-24 sm:w-28 shrink-0 z-10">
          <img 
            src="/urauth.png" 
            alt="تطبيق أور" 
            class="w-full h-auto object-contain drop-shadow-md transform "
          />
        </div>

       <!-- Text & Action Buttons -->
<div class="flex-grow px-6 text-center z-10 space-y-3">
  <h3 class="text-xl font-black text-[#702923]">حمل تطبيق بوابة أور</h3>
  <p class="text-sm text-stone-600 font-bold">وتواصل مع خدماتك الحكومية في أي وقت</p>
  
  <!-- App Store Buttons -->
  <div class="flex items-center justify-center gap-3 pt-2">
    <!-- App Store Button -->
    <a href="#" class="bg-stone-900 text-white px-4 py-2.5 rounded-xl flex items-center gap-2.5 hover:bg-stone-800 transition-colors shadow-sm">
      <svg class="w-6 h-6 fill-current shrink-0" viewBox="0 0 24 24">
        <path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.32-3.14-2.53C4.25 17 2.94 12.45 4.7 9.39c.87-1.52 2.43-2.48 4.12-2.51 1.28-.02 2.5.87 3.29.87.78 0 2.26-1.07 3.81-.91.65.03 2.47.26 3.64 1.98-.09.06-2.17 1.28-2.15 3.81.03 3.02 2.65 4.03 2.68 4.04-.03.07-.42 1.44-1.38 2.83M15.97 6.85c.66-.8 1.11-1.92.99-3.04-.96.04-2.12.64-2.8 1.44-.61.71-1.14 1.86-1 2.98 1.08.08 2.16-.58 2.81-1.38z"/>
      </svg>
      <div class="text-right leading-tight">
        <span class="block text-[10px] text-stone-300 uppercase tracking-wider">Download on the</span>
        <span class="block text-xs font-bold">App Store</span>
      </div>
    </a>
    
    <!-- Google Play Button -->
    <a href="#" class="bg-stone-900 text-white px-4 py-2.5 rounded-xl flex items-center gap-2.5 hover:bg-stone-800 transition-colors shadow-sm">
      <svg class="w-6 h-6 fill-current shrink-0" viewBox="0 0 24 24">
        <path d="M3.609 1.814L13.792 12 3.61 22.186a1.18 1.18 0 0 1-.36-.88V2.694c0-.34.135-.652.359-.88zm11.3 9.071l2.583-2.583 2.868 1.637c.753.43.753 1.134 0 1.564l-2.868 1.637-2.583-2.255zm.883 1.115l-3.344 3.344 6.883 6.883c.271.271.64.42.997.351l-4.536-10.578zm-3.344-3.985l3.344-3.344 4.536-10.578c-.357-.069-.726.08-.997.351l-6.883 6.883z"/>
      </svg>
      <div class="text-right leading-tight">
        <span class="block text-[10px] text-stone-300 uppercase tracking-wider">GET IT ON</span>
        <span class="block text-xs font-bold">Google Play</span>
      </div>
    </a>
  </div>
</div>

<!-- View Details Link -->
<a href="#" class="flex items-center gap-1.5 text-lg font-black text-stone-700 hover:text-[#702923] shrink-0 z-10 transition-colors">
  <span>عرض التفاصيل</span>
  <svg class="w-4 h-4 fill-current transform rotate-180" viewBox="0 0 24 24">
    <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z"/>
  </svg>
</a>
</div>
      <!-- AI ASSISTANT BANNER (RIGHT SIDE IN RTL) -->
      <div class="bg-[#faf7f2] hover:bg-white rounded-2xl p-4 border-2 border-[#e6ded5] hover:border-[#702923] shadow-md hover:shadow-xl transition-all duration-300 flex items-center justify-between gap-4 transition-all">
      <div class="w-20 h-20 rounded-2xl bg-[#702923]/10 flex items-center justify-center shrink-0 overflow-hidden p-1">    <img 
      src="/ai.png" 
      alt="مساعد أور الذكي" 
      class="w-full h-full object-contain"
    />
  </div>

        <div class="flex-grow space-y-2">
    <h3 class="text-lg font-black text-[#702923]">مرحباً، أنا مساعد أور الذكي</h3>
    <p class="text-sm text-stone-600 font-bold">يمكنني مساعدتك في العثور على الخدمة المناسبة والإجابة على استفساراتك</p>

    <div class="relative flex items-center mt-2">
      <input 
        type="text" 
        placeholder="اكتب سؤالك هنا..." 
        class="w-full bg-stone-100/90 border-2 border-stone-200/80 rounded-full py-2.5 pr-5 pl-12 text-sm font-semibold text-stone-800 focus:outline-none focus:bg-white focus:border-[#702923] shadow-inner transition-all"
      />
      <button class="absolute left-1.5 w-9 h-9 rounded-full bg-[#702923] text-white flex items-center justify-center hover:bg-[#521d18] transition-colors shadow-sm">
        <svg class="w-4 h-4 fill-current transform rotate-180" viewBox="0 0 24 24">
          <path d="M2.01 21L23 12 2.01 3 2 10l15 2-15 2z"/>
        </svg>
      </button>
    </div>
  </div>
</div>

    </div>

    <!-- BOTTOM STATS BAR -->
    <div class="bg-white/60 backdrop-blur-md rounded-2xl p-4 border border-stone-200/70 shadow-sm grid grid-cols-2 md:grid-cols-4 gap-4 divide-y md:divide-y-0 md:divide-x md:divide-x-reverse divide-stone-200">
      
      <!-- Stat 1 -->
      <div class="flex items-center justify-center gap-3 p-2">
        <div class="w-10 h-10 rounded-full bg-[#702923]/10 text-[#702923] flex items-center justify-center shrink-0">
          <svg class="w-5 h-5 fill-current" viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm1 15h-2v-6h2v6zm0-8h-2V7h2v2z"/></svg>
        </div>
        <div class="text-right">
          <p class="font-extrabold text-stone-900 text-sm">1,200+</p>
          <p class="text-[11px] text-stone-500 font-medium">جهة حكومية مرتبطة</p>
        </div>
      </div>

      <!-- Stat 2 -->
      <div class="flex items-center justify-center gap-3 p-2 pt-4 md:pt-2">
        <div class="w-10 h-10 rounded-full bg-[#702923]/10 text-[#702923] flex items-center justify-center shrink-0">
          <svg class="w-5 h-5 fill-current" viewBox="0 0 24 24"><path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-5 14H7v-2h7v2zm3-4H7v-2h10v2zm0-4H7V7h10v2z"/></svg>
        </div>
        <div class="text-right">
          <p class="font-extrabold text-stone-900 text-sm">2,000+</p>
          <p class="text-[11px] text-stone-500 font-medium">خدمة إلكترونية</p>
        </div>
      </div>

      <!-- Stat 3 -->
      <div class="flex items-center justify-center gap-3 p-2 pt-4 md:pt-2">
        <div class="w-10 h-10 rounded-full bg-[#702923]/10 text-[#702923] flex items-center justify-center shrink-0">
          <svg class="w-5 h-5 fill-current" viewBox="0 0 24 24"><path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/></svg>
        </div>
        <div class="text-right">
          <p class="font-extrabold text-stone-900 text-sm">+10,000,000</p>
          <p class="text-[11px] text-stone-500 font-medium">مستخدم مسجل</p>
        </div>
      </div>

      <!-- Stat 4 -->
      <div class="flex items-center justify-center gap-3 p-2 pt-4 md:pt-2">
        <div class="w-10 h-10 rounded-full bg-[#702923]/10 text-[#702923] flex items-center justify-center shrink-0">
          <svg class="w-5 h-5 fill-current" viewBox="0 0 24 24"><path d="M20 15.5c-1.25 0-2.45-.2-3.57-.57-.35-.11-.74-.03-1.02.24l-2.2 2.2c-2.83-1.44-5.15-3.75-6.59-6.59l2.2-2.21c.28-.26.36-.65.25-1C8.7 6.45 8.5 5.25 8.5 4c0-.55-.45-1-1-1H4c-.55 0-1 .45-1 1 0 9.39 7.61 17 17 17 .55 0 1-.45 1-1v-3.5c0-.55-.45-1-1-1z"/></svg>
        </div>
        <div class="text-right">
          <p class="font-extrabold text-stone-900 text-sm">24/7</p>
          <p class="text-[11px] text-stone-500 font-medium">خدمة على مدار الساعة</p>
        </div>
      </div>

    </div>

  </section>
</template>

<script setup>
</script>