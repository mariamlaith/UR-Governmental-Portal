<template>
  <section class="w-full px-2 sm:px-4 py-2 font-sans" dir="rtl">
    <div class="bg-[#f4efe8]/90 backdrop-blur-md rounded-2xl mx-16 sm:p-8 shadow-sm border border-[#e2d7c7]">
      
      <!-- HEADER ROW -->
      <div class="flex items-center justify-between pb-5 border-b border-[#e2d7c7]/80 mb-6">
        <!-- Title & Subtitle -->
        <div class="flex items-center gap-3.5">
          <div class="p-3 bg-[#702923]/10 text-[#702923] rounded-xl shrink-0">
            <svg class="w-7 h-7 fill-current" viewBox="0 0 24 24">
              <path d="M4 6h16v2H4zm0 5h16v2H4zm0 5h16v2H4z"/>
            </svg>
          </div>
          <div>
            <h2 class="text-2xl font-black text-stone-900">دليل الخدمات</h2>
            <p class="text-sm text-stone-600 font-bold mt-0.5">تصفح جميع الخدمات الحكومية حسب الفئة</p>
          </div>
        </div>

        <!-- View All Link -->
        <a href="#" class="flex items-center gap-2 text-sm font-extrabold text-[#702923] hover:text-[#521d18] transition-colors">
          <span>اعرض جميع الخدمات</span>
          <svg class="w-4 h-4 fill-current transform rotate-180" viewBox="0 0 24 24">
            <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z"/>
          </svg>
        </a>
      </div>

      <!-- 12-CARD GRID -->
      <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-6 gap-4 sm:gap-5">
        <div 
          v-for="(service, index) in services" 
          :key="index"
          class="group relative bg-[#faf7f2] hover:bg-[#fffdfa] rounded-2xl p-5 border-2 border-[#e6ded5] hover:border-[#702923] shadow-md hover:shadow-xl transition-all duration-300 flex flex-col items-center text-center cursor-pointer min-h-[170px] justify-between"
        >
          <!-- Icon inside soft circle -->
          <div class="w-14 h-14 rounded-full bg-[#f0e8df] group-hover:bg-[#702923]/10 flex items-center justify-center text-[#702923] transition-colors shrink-0">
            <svg class="w-7 h-7 fill-current" viewBox="0 0 24 24" v-html="service.svg"></svg>
          </div>

          <!-- Titles -->
          <div class="my-2">
            <h3 class="text-base font-black text-stone-800 group-hover:text-[#702923] transition-colors leading-tight">
              {{ service.title }}
            </h3>
            <p class="text-xs text-stone-500 font-bold mt-1 leading-snug">
              {{ service.subtitle }}
            </p>
          </div>

          <!-- Arrow Indicator -->
          <div class="w-6 h-6 rounded-full bg-[#e8ded3] group-hover:bg-[#702923] text-stone-500 group-hover:text-white flex items-center justify-center transition-all">
            <svg class="w-3.5 h-3.5 fill-current transform rotate-180" viewBox="0 0 24 24">
              <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z"/>
            </svg>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
const services = [
  { 
    title: 'التقاعد', 
    subtitle: 'خدمات المتقاعدين', 
    svg: '<path d="M16 11c1.66 0 2.99-1.34 2.99-3S17.66 5 16 5c-1.66 0-3 1.34-3 3s1.34 3 3 3zm-8 0c1.66 0 2.99-1.34 2.99-3S9.66 5 8 5C6.34 5 5 6.34 5 8s1.34 3 3 3zm0 2c-2.33 0-7 1.17-7 3.5V19h14v-2.5c0-2.33-4.67-3.5-7-3.5zm8 0c-.29 0-.62.02-.97.05 1.16.84 1.97 1.97 1.97 3.45V19h6v-2.5c0-2.33-4.67-3.5-7-3.5z"/>' 
  },
  { 
    title: 'الضرائب', 
    subtitle: 'الاستعلام والدفع', 
    svg: '<path d="M11.8 10.9c-2.27-.59-3-1.2-3-2.15 0-1.09 1.01-1.85 2.7-1.85 1.78 0 2.44.85 2.5 2.1h2.21c-.07-1.72-1.12-3.3-3.21-3.81V3h-3v2.16c-1.94.42-3.5 1.68-3.5 3.61 0 2.31 1.91 3.46 4.7 4.13 2.5.6 3 1.48 3 2.41 0 .69-.49 1.79-2.7 1.79-2.06 0-2.87-.92-2.98-2.1h-2.2c.12 2.19 1.76 3.42 3.68 3.83V21h3v-2.15c1.95-.37 3.5-1.5 3.5-3.55 0-2.84-2.43-3.81-4.7-4.4z"/>' 
  },
  { 
    title: 'الجوازات والسفر', 
    subtitle: 'إصدار أو تجديد', 
    svg: '<path d="M18 2H6c-1.1 0-2 .9-2 2v16c0 1.1.9 2 2 2h12c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2zm0 18H6V4h12v16zM12 6c-2.21 0-4 1.79-4 4s1.79 4 4 4 4-1.79 4-4-1.79-4-4-4zm0 6c-1.1 0-2-.9-2-2s.9-2 2-2 2 .9 2 2-.9 2-2 2z"/>' 
  },
  { 
    title: 'الإسكان والمشاريع', 
    subtitle: 'خدمات الإسكان', 
    svg: '<path d="M10 20v-6h4v6h5v-8h3L12 3 2 12h3v8z"/>' 
  },
  { 
    title: 'المرور والمركبات', 
    subtitle: 'تسجيل ودفع الرسوم', 
    svg: '<path d="M18.92 6.01C18.72 5.42 18.16 5 17.5 5h-11c-.66 0-1.21.42-1.42 1.01L3 12v8c0 .55.45 1 1 1h1c.55 0 1-.45 1-1v-1h12v1c0 .55.45 1 1 1h1c.55 0 1-.45 1-1v-8l-2.08-5.99zM6.5 16c-.83 0-1.5-.67-1.5-1.5S5.67 13 6.5 13s1.5.67 1.5 1.5S7.33 16 6.5 16zm11 0c-.83 0-1.5-.67-1.5-1.5s.67-1.5 1.5-1.5 1.5.67 1.5 1.5-.67 1.5-1.5 1.5zM5 11l1.5-4.5h11L19 11H5z"/>' 
  },
  { 
    title: 'البطاقة الوطنية', 
    subtitle: 'إصدار أو تجديد', 
    svg: '<path d="M20 4H4c-1.11 0-1.99.89-1.99 2L2 18c0 1.11.89 2 2 2h16c1.11 0 2-.89 2-2V6c0-1.11-.89-2-2-2zm0 14H4v-6h16v6zm0-10H4V6h16v2z"/>' 
  },
  { 
    title: 'الثقافة والسياحة', 
    subtitle: 'الآثار والمواقع السياحية', 
    svg: '<path d="M2 22h20v-2H2v2zm3-3h14v-2H5v2zm10-4v-6h2v6h-2zm-4 0v-6h2v6h-2zm-4 0v-6h2v6H7zm-1-8h12V5L12 2 6 5v2z"/>' 
  },
  { 
    title: 'الاقتصاد والمالية', 
    subtitle: 'الاستثمار والترخيص', 
    svg: '<path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm1 15h-2v-6h2v6zm0-8h-2V7h2v2z"/>' 
  },
  { 
    title: 'العمل والشؤون الاجتماعية', 
    subtitle: 'خدمات التوظيف والرعاية', 
    svg: '<path d="M16 11c1.66 0 2.99-1.34 2.99-3S17.66 5 16 5c-1.66 0-3 1.34-3 3s1.34 3 3 3zm-8 0c1.66 0 2.99-1.34 2.99-3S9.66 5 8 5C6.34 5 5 6.34 5 8s1.34 3 3 3zm0 2c-2.33 0-7 1.17-7 3.5V19h14v-2.5c0-2.33-4.67-3.5-7-3.5z"/>' 
  },
  { 
    title: 'الزراعة والثروة الحيوانية', 
    subtitle: 'دعم وتنمية', 
    svg: '<path d="M12 3c-4.97 0-9 4.03-9 9 0 2.12.74 4.07 1.97 5.61L4.35 19.4c-.39.39-.39 1.02 0 1.41.39.39 1.02.39 1.41 0l1.9-1.9C9.21 19.57 10.56 20 12 20c4.97 0 9-4.03 9-9s-4.03-9-9-9z"/>' 
  },
  { 
    title: 'الصحة', 
    subtitle: 'المستشفيات والخدمات', 
    svg: '<path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>' 
  },
  { 
    title: 'التعليم', 
    subtitle: 'القبول والمنح', 
    svg: '<path d="M5 13.18v4L12 21l7-3.82v-4L12 17l-7-3.82zM12 3L1 9l11 6 9-4.91V17h2V9L12 3z"/>' 
  },
]
</script>