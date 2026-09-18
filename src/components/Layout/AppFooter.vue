<template>
  <footer class="w-full font-sans text-stone-200" dir="rtl">
    
    <div class="bg-[#1e110c] pt-12 pb-8 text-stone-200">
      <div class="max-w-[1500px] mx-auto px-4 sm:px-8 grid grid-cols-1 md:grid-cols-4 gap-10 pb-10 border-b border-stone-800">
        
        <!-- Column 1: Logo & Social Links -->
        <div class="flex flex-col items-start gap-5">
          <img src="/urlogotrans.png" alt="بوابة أور" class="h-28 md:h-32 w-auto object-contain scale-105 origin-right" />
          
          <!-- Social Icons -->
          <div class="flex items-center gap-3 mt-1">
            <a href="#" class="w-10 h-10 rounded-full bg-stone-800 flex items-center justify-center hover:bg-[#702923] transition-colors" title="Facebook">
              <svg class="w-5 h-5 fill-current text-stone-200" viewBox="0 0 24 24"><path d="M9 8H6v4h3v12h5V12h3.642L18 8h-4V6.333C14 5.374 14.5 5 15.5 5H18V0h-3.808C10.592 0 9 1.583 9 4.615V8z"/></svg>
            </a>
            <a href="#" class="w-10 h-10 rounded-full bg-stone-800 flex items-center justify-center hover:bg-[#702923] transition-colors" title="LinkedIn">
              <svg class="w-5 h-5 fill-current text-stone-200" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
            </a>
            <a href="#" class="w-10 h-10 rounded-full bg-stone-800 flex items-center justify-center hover:bg-[#702923] transition-colors" title="Instagram">
              <svg class="w-5 h-5 fill-current text-stone-200" viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
            </a>
            <a href="#" class="w-10 h-10 rounded-full bg-stone-800 flex items-center justify-center hover:bg-[#702923] transition-colors" title="X">
              <svg class="w-4 h-4 fill-current text-stone-200" viewBox="0 0 24 24"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
            </a>
            <a href="#" class="w-10 h-10 rounded-full bg-stone-800 flex items-center justify-center hover:bg-[#702923] transition-colors" title="TikTok">
              <svg class="w-5 h-5 fill-current text-stone-200" viewBox="0 0 24 24"><path d="M12.525.02c1.31-.02 2.61-.01 3.91-.02.08 1.53.63 3.09 1.75 4.17 1.12 1.11 2.7 1.62 4.24 1.79v4.03c-1.44-.05-2.89-.35-4.2-.97-.57-.26-1.1-.59-1.62-.93-.01 2.92.01 5.84-.02 8.75-.08 1.4-.54 2.79-1.35 3.94-1.31 1.92-3.58 3.17-5.91 3.21-1.43.08-2.86-.31-4.08-1.03-2.02-1.19-3.44-3.37-3.65-5.71-.02-.5-.03-1-.01-1.49.18-1.9 1.12-3.72 2.58-4.96 1.66-1.44 3.98-2.13 6.15-1.72.02 1.48-.04 2.96-.04 4.44-.99-.32-2.15-.23-3.02.37-.82.57-1.31 1.56-1.3 2.56.01.81.4 1.6 1.08 2.07.72.52 1.68.68 2.53.46 1.02-.24 1.89-1.02 2.19-2.03.18-.57.24-1.17.22-1.77.02-4.99.01-9.98.01-14.97z"/></svg>
            </a>
            <a href="#" class="w-10 h-10 rounded-full bg-stone-800 flex items-center justify-center hover:bg-[#702923] transition-colors" title="YouTube">
              <svg class="w-5 h-5 fill-current text-stone-200" viewBox="0 0 24 24"><path d="M19.615 3.184c-3.604-.246-11.631-.245-15.23 0-3.897.266-4.356 2.62-4.385 8.816.029 6.185.484 8.549 4.385 8.816 3.6.245 11.626.246 15.23 0 3.897-.266 4.356-2.62 4.385-8.816-.029-6.185-.484-8.549-4.385-8.816zm-10.615 12.816v-8l8 3.993-8 4.007z"/></svg>
            </a>
          </div>
        </div>

        <!-- Column 2: Legal Links -->
        <div class="space-y-4 text-base">
          <p class="font-bold text-white text-lg mb-3 border-b border-stone-800 pb-2">عن المنصة</p>
          <ul class="space-y-2.5 text-stone-300 font-medium">
            <li><a href="#" class="hover:text-white transition-colors">عن أور</a></li>
            <li><a href="#" class="hover:text-white transition-colors">سياسة الخصوصية</a></li>
            <li><a href="#" class="hover:text-white transition-colors">شروط الاستخدام</a></li>
            <li><a href="#" class="hover:text-white transition-colors">اتصل بنا</a></li>
          </ul>
        </div>

        <!-- Column 3: Quick Navigation -->
        <div class="space-y-4 text-base">
          <p class="font-bold text-white text-lg mb-3 border-b border-stone-800 pb-2">روابط سريعة</p>
          <ul class="space-y-2.5 text-stone-300 font-medium">
            <li><a href="#" class="hover:text-white transition-colors">الخدمات الإلكترونية</a></li>
            <li><a href="#" class="hover:text-white transition-colors">الخدمات المقترحة</a></li>
            <li><a href="#" class="hover:text-white transition-colors">المستندات الإلكترونية</a></li>
            <li><a href="#" class="hover:text-white transition-colors">الجهات الخدمية</a></li>
            <li><a href="#" class="hover:text-white transition-colors">المواقع الحكومية</a></li>
          </ul>
        </div>

        <!-- Column 4: Copyright Info -->
        <div class="flex flex-col text-sm text-stone-300 pt-36">
          <div>
            <p class="font-semibold text-stone-200 leading-relaxed">جمهورية العراق - الأمانة العامة لمجلس الوزراء</p>
          </div>
          <p class="leading-relaxed text-stone-400 font-medium">
            جميع الحقوق محفوظة © 2026 بوابة أور الإلكترونية للخدمات الحكومية
          </p>
        </div>

      </div>

      <!-- COPYRIGHT BOTTOM LINE -->
      <div class="max-w-[1500px] mx-auto px-4 sm:px-8 pt-6 flex flex-col sm:flex-row justify-between items-center text-sm text-stone-400 gap-2 font-medium">
        <p>2026 بوابة أور - جميع الحقوق محفوظة</p>
        <p>منصة الخدمات الحكومية الإلكترونية</p>
      </div>
    </div>

  </footer>
</template>

<script>
export default {
  name: 'AppFooter'
}
</script>