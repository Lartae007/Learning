<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>StudyHub — คลังข้อมูลการเรียนมหาวิทยาลัย</title>

  <!-- Google Fonts: Prompt สำหรับหัวข้อและปุ่ม, Sarabun สำหรับเนื้อหาที่อ่านง่าย -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Prompt:wght@300;400;500;600;700&family=Sarabun:wght@300;400;500;600;700&display=swap" rel="stylesheet" />

  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            heading: ['Prompt', 'sans-serif'],
            sans: ['Sarabun', 'sans-serif'],
          },
          boxShadow: {
            soft: '0 4px 24px -4px rgba(15, 23, 42, 0.06)',
            card: '0 10px 30px -8px rgba(15, 23, 42, 0.08)',
          }
        }
      }
    };
  </script>

  <style>
    /* ตั้งค่าฟอนต์พื้นฐานและแอนิเมชันที่นุ่มนวล */
    body {
      font-family: 'Sarabun', sans-serif;
      background-color: #F8FAFC;
      color: #1E293B;
      overflow-x: hidden;
    }

    h1, h2, h3, h4, .font-heading, button, label, select, input::placeholder {
      font-family: 'Prompt', sans-serif;
    }

    /* Custom Scrollbar */
    ::-webkit-scrollbar {
      width: 6px;
      height: 6px;
    }
    ::-webkit-scrollbar-track {
      background: transparent;
    }
    ::-webkit-scrollbar-thumb {
      background: #CBD5E1;
      border-radius: 9999px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: #94A3B8;
    }

    /* Animation Helpers */
    @keyframes fadeSlideUp {
      from {
        opacity: 0;
        transform: translateY(10px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    .animate-fade-up {
      animation: fadeSlideUp 0.28s cubic-bezier(0.16, 1, 0.3, 1) forwards;
    }

    /* Lightbox Image Pan & Zoom */
    #lightboxImg {
      transition: transform 0.15s ease-out;
      user-select: none;
      -webkit-user-drag: none;
    }
    #lightboxImg.dragging {
      transition: none;
      cursor: grabbing;
    }
  </style>
</head>
<body class="min-h-screen flex flex-col selection:bg-indigo-100 selection:text-indigo-900">

  <!-- ===================================================================== -->
  <!-- TOP NAVIGATION BAR (แสดงตลอดเวลา ปรับเปลี่ยนตามหน้าที่อยู่)              -->
  <!-- ===================================================================== -->
  <header class="sticky top-0 z-30 bg-white/85 backdrop-blur-md border-b border-slate-200/70">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 h-16 flex items-center justify-between gap-3">
      <!-- โลโก้แอป -->
      <button onclick="navigateToHome()" class="flex items-center gap-2.5 text-left group focus:outline-none">
        <div class="w-9 h-9 rounded-xl bg-slate-900 text-white flex items-center justify-center shadow-sm group-hover:scale-105 transition-transform">
          <svg class="w-5 h-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M22 10v6M2 10l10-5 10 5-10 5z"/>
            <path d="M6 12v5c3 3 9 3 12 0v-5"/>
          </svg>
        </div>
        <div>
          <span class="font-heading font-semibold text-base sm:text-lg text-slate-900 tracking-tight block leading-none">StudyHub</span>
          <span class="text-[11px] text-slate-400 font-heading hidden sm:block mt-0.5">คลังข้อมูลการเรียนมหาวิทยาลัย</span>
        </div>
      </button>

      <!-- ปุ่มสำรองข้อมูล / นำเข้าข้อมูล (แสดงบนหน้าแรก) -->
      <div id="homeHeaderActions" class="flex items-center gap-2">
        <button onclick="exportBackupData()" title="ดาวน์โหลดไฟล์สำรองข้อมูลทั้งหมด"
          class="inline-flex items-center gap-1.5 px-3 py-2 rounded-xl text-xs sm:text-sm font-medium text-slate-600 hover:text-slate-900 hover:bg-slate-100 border border-slate-200/80 bg-white transition-all">
          <svg class="w-4 h-4 text-slate-500" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/>
          </svg>
          <span>สำรองข้อมูล</span>
        </button>

        <label title="กู้คืนข้อมูลจากไฟล์สำรอง (.json)"
          class="cursor-pointer inline-flex items-center gap-1.5 px-3 py-2 rounded-xl text-xs sm:text-sm font-medium text-slate-600 hover:text-slate-900 hover:bg-slate-100 border border-slate-200/80 bg-white transition-all">
          <svg class="w-4 h-4 text-slate-500" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="17 8 12 3 7 8"/><line x1="12" y1="3" x2="12" y2="15"/>
          </svg>
          <span>นำเข้า</span>
          <input type="file" id="importFileInput" accept=".json" class="hidden" onchange="importBackupData(event)" />
        </label>
      </div>

      <!-- ปุ่มกลับหน้าแรก (แสดงเมื่ออยู่ในหน้าวิชาเรียน) -->
      <div id="workspaceHeaderActions" class="hidden items-center gap-2">
        <button onclick="navigateToHome()"
          class="inline-flex items-center gap-1.5 px-3.5 py-2 rounded-xl text-xs sm:text-sm font-medium text-slate-700 hover:text-slate-900 bg-slate-100 hover:bg-slate-200/80 transition-all">
          <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2">
            <line x1="19" y1="12" x2="5" y2="12"/><polyline points="12 19 5 12 12 5"/>
          </svg>
          <span>กลับหน้าแรก</span>
        </button>
      </div>
    </div>
  </header>

  <!-- ===================================================================== -->
  <!-- VIEW 1: CLEAN HOME DASHBOARD (หน้าแรกโล่ง สบายตา + ปุ่มวิชาเรียนใหญ่ๆ)    -->
  <!-- ===================================================================== -->
  <main id="homeView" class="flex-1 max-w-6xl w-full mx-auto px-4 sm:px-6 py-8 sm:py-12 flex flex-col">

    <!-- สถานะเริ่มต้น (หน้าโล่งเมื่อยังไม่มีวิชาเรียน) -->
    <section id="emptyHomeState" class="hidden flex-1 flex flex-col items-center justify-center text-center py-12 sm:py-20 animate-fade-up">
      <div class="w-20 h-20 rounded-3xl bg-white border border-slate-200/80 shadow-soft flex items-center justify-center text-slate-400 mb-6">
        <svg class="w-9 h-9 text-indigo-500" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
          <path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"/>
          <path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"/>
          <line x1="12" y1="8" x2="12" y2="14"/>
          <line x1="9" y1="11" x2="15" y2="11"/>
        </svg>
      </div>

      <h1 class="font-heading text-2xl sm:text-3xl font-semibold text-slate-900 tracking-tight mb-2">
        พื้นที่เก็บข้อมูลการเรียนของคุณ
      </h1>
      <p class="text-slate-500 text-base sm:text-lg max-w-md mb-8 leading-relaxed">
        เริ่มต้นด้วยการสร้างรายวิชาแรก เพื่อเก็บรูปภาพกระดานเลกเชอร์ ลิงก์ติว โน้ตสรุป และใช้ผู้ช่วยติว AI ในที่เดียว
      </p>

      <button onclick="openSubjectModal()"
        class="group inline-flex items-center gap-3 px-8 py-4 rounded-2xl bg-slate-900 hover:bg-indigo-600 text-white font-heading font-medium text-base sm:text-lg shadow-card hover:shadow-xl hover:-translate-y-0.5 active:translate-y-0 transition-all duration-200">
        <span class="w-7 h-7 rounded-xl bg-white/15 flex items-center justify-center group-hover:rotate-90 transition-transform duration-200">
          <svg class="w-5 h-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
            <line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/>
          </svg>
        </span>
        <span>+ เพิ่มวิชาเรียน</span>
      </button>
    </section>

    <!-- สถานะเมื่อมีรายวิชาแล้ว (Grid ปุ่มการ์ดวิชาเรียนขนาดใหญ่) -->
    <section id="populatedHomeState" class="hidden animate-fade-up">
      <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 mb-8">
        <div>
          <div class="flex items-center gap-2.5">
            <h1 class="font-heading text-2xl sm:text-3xl font-semibold text-slate-900 tracking-tight">รายวิชาเรียนของคุณ</h1>
            <span id="subjectCountBadge" class="px-2.5 py-0.5 rounded-full text-xs font-heading font-medium bg-slate-200/70 text-slate-700">0 วิชา</span>
          </div>
          <p class="text-slate-500 text-sm sm:text-base mt-1">แตะที่ปุ่มรายวิชาเพื่อเปิดคลังภาพเลกเชอร์ โน้ตสรุป และผู้ช่วยติว AI</p>
        </div>

        <button onclick="openSubjectModal()"
          class="inline-flex items-center justify-center gap-2 px-5 py-3 rounded-2xl bg-slate-900 hover:bg-indigo-600 text-white font-heading font-medium text-sm sm:text-base shadow-soft hover:shadow-md transition-all shrink-0">
          <svg class="w-5 h-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4">
            <line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/>
          </svg>
          <span>+ เพิ่มวิชาเรียน</span>
        </button>
      </div>

      <!-- Responsive Grid ของปุ่มการ์ดวิชาเรียนขนาดใหญ่ -->
      <div id="subjectsGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-5 sm:gap-6">
        <!-- การ์ดวิชาเรียนจะถูกสร้างแบบไดนามิกที่นี่ -->
      </div>
    </section>
  </main>

  <!-- ===================================================================== -->
  <!-- VIEW 2: SUBJECT WORKSPACE (พื้นที่ภายในแต่ละวิชาเรียน)                   -->
  <!-- ===================================================================== -->
  <main id="workspaceView" class="hidden flex-1 max-w-6xl w-full mx-auto px-4 sm:px-6 py-6 sm:py-8 animate-fade-up">

    <!-- แถบหัวข้อวิชาเรียน (Subject Header Banner) -->
    <div id="workspaceHeaderCard" class="rounded-3xl p-5 sm:p-7 mb-6 border transition-all relative overflow-hidden">
      <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 relative z-10">
        <div class="flex items-start sm:items-center gap-4">
          <div id="wsSubjectIconBox" class="w-14 h-14 sm:w-16 sm:h-16 rounded-2xl flex items-center justify-center shrink-0 shadow-sm bg-white">
            <!-- ไอคอนประจำวิชา -->
          </div>
          <div>
            <div class="flex flex-wrap items-center gap-2 mb-1">
              <span id="wsSubjectCode" class="inline-flex items-center px-2.5 py-0.5 rounded-lg text-xs font-heading font-medium bg-white/80 text-slate-700 border border-black/5">
                รหัสวิชา
              </span>
            </div>
            <h1 id="wsSubjectName" class="font-heading text-xl sm:text-2xl md:text-3xl font-semibold text-slate-900 tracking-tight">
              ชื่อวิชาเรียน
            </h1>
          </div>
        </div>

        <div class="flex items-center gap-2 self-end sm:self-center">
          <button onclick="editCurrentSubject()"
            class="inline-flex items-center gap-1.5 px-3.5 py-2 rounded-xl text-xs sm:text-sm font-medium bg-white/85 hover:bg-white text-slate-700 border border-black/5 shadow-sm transition-all">
            <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M11 4H4a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"/>
              <path d="M18.5 2.5a2.121 2.121 0 0 1 3 3L12 15l-4 1 1-4 9.5-9.5z"/>
            </svg>
            <span>แก้ไขข้อมูลวิชา</span>
          </button>
        </div>
      </div>
    </div>

    <!-- แถบเลือก 3 แท็บหลัก -->
    <div class="bg-white p-1.5 rounded-2xl border border-slate-200/80 shadow-soft mb-6 grid grid-cols-3 gap-1.5">
      <button onclick="switchWorkspaceTab('photos')" id="tabBtn-photos"
        class="ws-tab-btn flex items-center justify-center gap-2 py-2.5 sm:py-3 px-2 sm:px-4 rounded-xl text-xs sm:text-sm font-heading font-medium transition-all">
        <svg class="w-4 h-4 shrink-0" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <rect x="3" y="3" width="18" height="18" rx="2" ry="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/>
        </svg>
        <span class="truncate">คลังภาพเลกเชอร์</span>
        <span id="tabPhotoCount" class="hidden sm:inline-flex px-2 py-0.5 rounded-full text-[11px] bg-slate-100 text-slate-600">0</span>
      </button>

      <button onclick="switchWorkspaceTab('resources')" id="tabBtn-resources"
        class="ws-tab-btn flex items-center justify-center gap-2 py-2.5 sm:py-3 px-2 sm:px-4 rounded-xl text-xs sm:text-sm font-heading font-medium transition-all">
        <svg class="w-4 h-4 shrink-0" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/>
        </svg>
        <span class="truncate">ตัวช่วย & โน้ตสรุป</span>
        <span id="tabResourceCount" class="hidden sm:inline-flex px-2 py-0.5 rounded-full text-[11px] bg-slate-100 text-slate-600">0</span>
      </button>

      <button onclick="switchWorkspaceTab('ai')" id="tabBtn-ai"
        class="ws-tab-btn flex items-center justify-center gap-2 py-2.5 sm:py-3 px-2 sm:px-4 rounded-xl text-xs sm:text-sm font-heading font-medium transition-all">
        <svg class="w-4 h-4 shrink-0" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M12 2l2.4 7.4L22 12l-7.6 2.6L12 22l-2.4-7.4L2 12l7.6-2.6L12 2z"/>
        </svg>
        <span class="truncate">ผู้ช่วยติว AI</span>
      </button>
    </div>

    <!-- =================================================================== -->
    <!-- TAB 1: คลังภาพเลกเชอร์ & กระดาน (Lecture Photos Gallery)              -->
    <!-- =================================================================== -->
    <div id="tabContent-photos" class="ws-tab-panel space-y-6">
      <!-- พื้นที่อัปโหลดรูปภาพ (Drag & Drop + เลือกหลายรูป) -->
      <div id="photoDropzone"
        class="bg-white border-2 border-dashed border-slate-300 hover:border-indigo-400 rounded-3xl p-6 sm:p-8 text-center transition-all cursor-pointer group"
        onclick="document.getElementById('photoUploadInput').click()">
        <input type="file" id="photoUploadInput" accept="image/*" multiple class="hidden" onchange="handlePhotoFilesSelected(event)" />

        <div class="w-12 h-12 rounded-2xl bg-indigo-50 text-indigo-600 flex items-center justify-center mx-auto mb-3 group-hover:scale-105 transition-transform">
          <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="17 8 12 3 7 8"/><line x1="12" y1="3" x2="12" y2="15"/>
          </svg>
        </div>
        <h3 class="font-heading font-medium text-base sm:text-lg text-slate-800">
          อัปโหลดรูปภาพกระดานไวท์บอร์ด สไลด์ หรือชีทสรุป
        </h3>
        <p class="text-slate-500 text-xs sm:text-sm mt-1">
          คลิกเพื่อเลือกรูปภาพ (เลือกได้หลายรูปพร้อมกัน) หรือลากไฟล์มาวางที่นี่
        </p>
      </div>

      <!-- แถบกรองแท็กและค้นหาภาพ -->
      <div id="photoFilterBar" class="hidden flex flex-col sm:flex-row sm:items-center justify-between gap-3">
        <div class="flex items-center gap-1.5 overflow-x-auto pb-1" id="photoTagFilters">
          <!-- ปุ่มกรองแท็กจะสร้างที่นี่ -->
        </div>
        <div class="relative w-full sm:w-64">
          <svg class="w-4 h-4 text-slate-400 absolute left-3.5 top-1/2 -translate-y-1/2" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/>
          </svg>
          <input type="text" id="photoSearchInput" oninput="renderPhotosGrid()" placeholder="ค้นหาชื่อภาพหรือคำอธิบาย..."
            class="w-full pl-9 pr-3.5 py-2 rounded-xl bg-white border border-slate-200 text-sm focus:outline-none focus:border-indigo-400" />
        </div>
      </div>

      <!-- แสดงแกลเลอรีรูปภาพ -->
      <div id="photosGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-5">
        <!-- การ์ดรูปภาพจะแสดงที่นี่ -->
      </div>

      <div id="emptyPhotosState" class="bg-white rounded-3xl border border-slate-200/70 p-10 text-center">
        <p class="text-slate-400 text-sm sm:text-base">ยังไม่มีรูปภาพเลกเชอร์ในวิชานี้ ลองอัปโหลดรูปกระดานหรือสไลด์แรกของคุณได้เลย</p>
      </div>
    </div>

    <!-- =================================================================== -->
    <!-- TAB 2: รวมตัวช่วยเรียน & โน้ตสรุป (Study Resources & Notes)          -->
    <!-- =================================================================== -->
    <div id="tabContent-resources" class="ws-tab-panel hidden grid grid-cols-1 lg:grid-cols-12 gap-6">

      <!-- ฝั่งซ้าย (7 คอลัมน์): ลิงก์ตัวช่วยการเรียน -->
      <div class="lg:col-span-7 space-y-5">
        <div class="bg-white rounded-3xl border border-slate-200/80 p-5 sm:p-6 shadow-soft">
          <div class="flex items-center justify-between mb-4">
            <div>
              <h2 class="font-heading font-semibold text-lg text-slate-900">ลิงก์ตัวช่วยการเรียน</h2>
              <p class="text-xs sm:text-sm text-slate-500">รวบรวมคลิปติว YouTube, Google Drive ชีทเรียน หรือเว็บอ้างอิง</p>
            </div>
          </div>

          <!-- ฟอร์มเพิ่มลิงก์ใหม่ -->
          <form onsubmit="handleAddLink(event)" class="bg-slate-50 rounded-2xl p-4 border border-slate-200/60 space-y-3 mb-5">
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-3">
              <div class="sm:col-span-2">
                <input type="text" id="linkTitleInput" required placeholder="ชื่อลิงก์ เช่น คลิปติวบทที่ 1-3, ชีทสรุปอาจารย์..."
                  class="w-full px-3.5 py-2.5 rounded-xl bg-white border border-slate-200 text-sm focus:outline-none focus:border-indigo-500" />
              </div>
              <div>
                <select id="linkCategoryInput"
                  class="w-full px-3 py-2.5 rounded-xl bg-white border border-slate-200 text-sm text-slate-700 focus:outline-none focus:border-indigo-500">
                  <option value="คลิปติว">🎬 คลิปติว</option>
                  <option value="ชีทสรุป">📄 ชีทสรุป</option>
                  <option value="แนวข้อสอบ">📝 แนวข้อสอบ</option>
                  <option value="อื่นๆ">🔗 อื่นๆ</option>
                </select>
              </div>
            </div>

            <div class="flex flex-col sm:flex-row gap-2.5">
              <input type="text" id="linkUrlInput" required placeholder="วางลิงก์ URL ที่นี่ (เช่น https://youtube.com/...)"
                class="flex-1 px-3.5 py-2.5 rounded-xl bg-white border border-slate-200 text-sm focus:outline-none focus:border-indigo-500" />
              <button type="submit"
                class="px-5 py-2.5 rounded-xl bg-slate-900 hover:bg-indigo-600 text-white font-heading font-medium text-sm transition-colors shrink-0">
                + บันทึกลิงก์
              </button>
            </div>
          </form>

          <!-- ตัวกรองหมวดหมู่ลิงก์ -->
          <div class="flex items-center gap-1.5 overflow-x-auto pb-2 mb-3" id="linkCategoryFilters">
            <button type="button" onclick="setLinkFilter('ทั้งหมด')" class="link-filter-btn px-3 py-1 rounded-lg text-xs font-heading font-medium bg-slate-900 text-white">ทั้งหมด</button>
            <button type="button" onclick="setLinkFilter('คลิปติว')" class="link-filter-btn px-3 py-1 rounded-lg text-xs font-heading font-medium bg-slate-100 text-slate-600 hover:bg-slate-200">🎬 คลิปติว</button>
            <button type="butto
