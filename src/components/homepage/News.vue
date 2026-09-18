<template>
  <section class="w-full px-2 sm:px-4 py-4 font-sans" dir="rtl">
    <!-- HEADER ROW -->
    <div class="flex items-center justify-between pb-4 mb-4 mx-16">
      <!-- Title & Subtitle -->
      <div class="flex items-center gap-3.5">
        <div class="p-3 bg-[#702923]/10 text-[#702923] rounded-xl shrink-0">
          <svg class="w-7 h-7 fill-current" viewBox="0 0 24 24">
            <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-5 14H7v-2h7v2zm3-4H7v-2h10v2zm0-4H7V7h10v2z"/>
          </svg>
        </div>
        <div>
          <h2 class="text-2xl font-black text-stone-900">آخر الأخبار</h2>
          <p class="text-sm text-stone-600 font-bold mt-0.5">أحدث الأخبار والقرارات الحكومية</p>
        </div>
      </div>

      <!-- View All Link -->
      <a href="#" class="flex items-center gap-2 text-sm font-extrabold text-[#702923] hover:text-[#521d18] transition-colors">
        <span>اعرض جميع الأخبار</span>
        <svg class="w-4 h-4 fill-current transform rotate-180" viewBox="0 0 24 24">
          <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z"/>
        </svg>
      </a>
    </div>

    <!-- 4-CARD NEWS GRID -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-5 mx-16">
      <div 
        v-for="(item, index) in newsList" 
        :key="index"
        class="group bg-[#faf7f2] hover:bg-[#fffdfa] rounded-2xl p-4 border-2 border-[#e6ded5] hover:border-[#702923] shadow-md hover:shadow-xl transition-all duration-300 flex flex-col justify-between cursor-pointer"
      >
        <div>
          <!-- IMAGE CONTAINER -->
          <div class="relative w-full h-48 rounded-xl overflow-hidden mb-4 bg-stone-200">
            <img 
              :src="item.image" 
              :alt="item.title" 
              class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300"
            />
          </div>

          <!-- TITLE & DESCRIPTION -->
          <h3 class="text-base font-black text-[#1e5a8a] line-clamp-3 group-hover:text-[#702923] transition-colors leading-snug text-center px-1">
            {{ item.title }}
          </h3>
        </div>

        <!-- CARD FOOTER (Date & Arrow Button) -->
        <div class="flex items-center justify-between pt-3 mt-4 border-t border-[#e2d7c7] text-stone-400">
          <!-- Arrow Indicator -->
          <div class="w-7 h-7 rounded-full bg-[#e8ded3] group-hover:bg-[#702923] text-stone-500 group-hover:text-white flex items-center justify-center transition-all">
            <svg class="w-4 h-4 fill-current transform rotate-180" viewBox="0 0 24 24">
              <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z"/>
            </svg>
          </div>

          <!-- Date -->
          <span class="text-xs font-bold text-stone-500">{{ item.date }}</span>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
const newsList = [
  {
    title: 'الهيئة العليا للحج والعمرة تُطلق الاستمارة الخاصة بـ "لم الشمل" و "تعديل البيانات" عبر بوابة أور الإلكترونية',
    date: 'July 29, 2026',
    image: '/photo1.jpg'
  },
  {
    title: 'لضمان السرعة والأولوية في المتابعة... "بوابة أور" تطلق منصة "رسائلي" المباشرة للدعم الفني',
    date: 'July 30, 2026',
    image: '/photo4.png'
  },
  {
    title: 'الهيئة العليا للحج والعمرة تُطلق خدمة استرجاع مبالغ التسجيل لقرعة الحج إلكترونياً',
    date: 'August 1, 2026',
    image: '/photo3.png'
  },
  {
    title: 'هيئة التقاعد الوطنية تطلق استمارة تحديث بيانات المتقاعدين بالتنسيق مع المركز الوطني للتحول الرقمي',
    date: 'September 14, 2026',
    image: 'photo2.jpg'
  }
]
</script>