<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>نظام إدارة المنتجات والأسعار</title>
<script src="https://unpkg.com/html5-qrcode@2.3.8/html5-qrcode.min.js"></script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700&display=swap');
*{box-sizing:border-box;margin:0;padding:0}
:root{
--bg:#0D1117;--surface:#161B22;--surfaceEl:#1C2333;
--card:rgba(30,40,55,.85);--cardBorder:rgba(48,65,86,.5);
--primary:#2EA67A;--primaryLight:#3BD99A;--primaryDark:#1E8A5F;
--accent:#58A6FF;--text:#E6EDF3;--textSec:#8B949E;--textMuted:#484F58;
--danger:#F85149;--dangerBg:rgba(248,81,73,.1);
--warning:#D29922;--success:#2EA67A;--successBg:rgba(46,166,122,.1);
--border:#30363D;--inputBg:rgba(22,27,34,.9);--inputBorder:#30363D;
--overlay:rgba(0,0,0,.6);--glass:rgba(22,27,34,.7);
}
html,body{height:100%;overflow:hidden}
body{font-family:'Cairo',sans-serif;background:var(--bg);color:var(--text);direction:rtl}
.app{display:flex;flex-direction:column;height:100vh;height:100dvh;max-width:480px;margin:0 auto;position:relative;overflow:hidden}

/* Bottom Nav */
.bottom-nav{display:flex;border-top:1px solid var(--border);background:var(--surface);flex-shrink:0;padding-bottom:env(safe-area-inset-bottom,0)}
.nav-btn{flex:1;display:flex;flex-direction:column;align-items:center;gap:2px;padding:10px 0 8px;background:none;border:none;color:var(--textMuted);cursor:pointer;font-family:'Cairo',sans-serif;font-size:11px;transition:color .2s}
.nav-btn.active{color:var(--primary)}
.nav-btn svg{width:22px;height:22px;fill:currentColor}
.nav-btn .badge{position:absolute;top:4px;right:calc(50% - 18px);width:16px;height:16px;border-radius:50%;background:var(--warning);color:#fff;font-size:9px;display:flex;align-items:center;justify-content:center;font-weight:700}

/* Pages */
.page{display:none;flex:1;overflow-y:auto;overflow-x:hidden;-webkit-overflow-scrolling:touch}
.page.active{display:flex;flex-direction:column}
.page-scroll{flex:1;overflow-y:auto;padding:0 16px 80px}
.page-header{padding:16px 16px 8px;padding-top:max(16px,env(safe-area-inset-top))}
.page-title{font-size:26px;font-weight:700;margin-bottom:4px}

/* Search */
.search-box{display:flex;align-items:center;gap:10px;background:var(--inputBg);border:1px solid var(--inputBorder);border-radius:12px;padding:10px 14px;margin:0 16px 8px}
.search-box input{flex:1;background:none;border:none;outline:none;color:var(--text);font-family:'Cairo',sans-serif;font-size:14px;direction:rtl}
.search-box input::placeholder{color:var(--textMuted)}
.search-box svg{width:18px;height:18px;fill:var(--textMuted);flex-shrink:0;cursor:pointer}

/* Filters */
.filters-row{display:flex;justify-content:space-between;padding:0 16px 8px;gap:6px;flex-wrap:wrap}
.filter-group{display:flex;gap:5px}
.chip{padding:4px 10px;border-radius:8px;border:1px solid rgba(48,54,61,.5);background:none;color:var(--textSec);font-family:'Cairo',sans-serif;font-size:12px;font-weight:600;cursor:pointer;transition:.2s}
.chip.active-sort{background:rgba(46,166,122,.2);border-color:var(--primary);color:var(--primaryLight)}
.chip.active-filter{background:rgba(88,166,255,.2);border-color:var(--accent);color:var(--accent)}

/* Product Card */
.product-card{background:var(--card);border:1px solid var(--cardBorder);border-radius:14px;padding:14px 16px;margin-bottom:10px;cursor:pointer;transition:opacity .15s}
.product-card:active{opacity:.8}
.card-top{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:8px}
.card-name{font-size:16px;font-weight:700;flex:1}
.card-barcode{font-size:12px;color:var(--textSec);margin-top:2px}
.sync-dot{width:8px;height:8px;border-radius:50%;background:var(--warning);flex-shrink:0;margin-top:6px;margin-right:8px}
.card-bottom{display:flex;justify-content:space-between;align-items:center}
.price-badge{background:rgba(30,138,95,.2);padding:3px 12px;border-radius:8px}
.price-text{font-size:15px;font-weight:700;color:var(--primaryLight)}
.arrow-icon{color:var(--textMuted);font-size:16px}

/* Empty state */
.empty-state{display:flex;flex-direction:column;align-items:center;justify-content:center;padding:60px 20px;color:var(--textMuted);text-align:center}
.empty-state svg{width:56px;height:56px;fill:var(--textMuted);margin-bottom:16px}
.empty-title{font-size:17px;color:var(--textSec);font-weight:600}
.empty-sub{font-size:13px;margin-top:4px}

/* Scanner */
.scanner-container{flex:1;display:flex;flex-direction:column;align-items:center;justify-content:center;padding:20px;position:relative;background:#000}
#reader{width:100%;max-width:350px;border-radius:12px;overflow:hidden}
.scan-title{color:#fff;font-size:18px;font-weight:600;margin-bottom:16px;text-align:center}
.scan-hint{color:rgba(255,255,255,.5);font-size:13px;margin-top:16px;text-align:center}
.scan-manual-btn{display:inline-flex;align-items:center;gap:8px;background:rgba(255,255,255,.15);color:#fff;padding:10px 20px;border-radius:12px;border:none;font-family:'Cairo',sans-serif;font-size:14px;font-weight:600;cursor:pointer;margin-top:16px}
.scan-web-card{background:var(--card);border:1px solid var(--cardBorder);border-radius:20px;padding:32px;text-align:center;max-width:340px}
.scan-web-card svg{width:56px;height:56px;fill:var(--primary);margin-bottom:16px}
.scan-web-title{font-size:20px;font-weight:700;margin-bottom:8px}
.scan-web-desc{font-size:14px;color:var(--textSec);line-height:1.7;margin-bottom:20px}
.scan-input-row{display:flex;gap:8px;margin-top:12px}
.scan-input-row input{flex:1;background:var(--inputBg);border:1px solid var(--inputBorder);border-radius:10px;padding:12px 14px;color:var(--text);font-family:'Cairo',sans-serif;font-size:14px;direction:ltr;text-align:left}
.scan-input-row input::placeholder{color:var(--textMuted)}

/* Form */
.form-card{background:var(--card);border:1px solid var(--cardBorder);border-radius:16px;padding:20px;margin-bottom:16px}
.field{margin-bottom:16px}
.field-label{font-size:13px;font-weight:600;color:var(--textSec);margin-bottom:6px;display:block}
.field-input{width:100%;background:var(--inputBg);border:1px solid var(--inputBorder);border-radius:10px;padding:12px 14px;color:var(--text);font-family:'Cairo',sans-serif;font-size:15px;outline:none;direction:rtl}
.field-input:focus{border-color:var(--primary)}
.field-input::placeholder{color:var(--textMuted)}
.field-textarea{min-height:70px;resize:vertical}
.price-row{display:flex;gap:12px}
.price-row .field:first-child{flex:1}
.currency-btns{display:flex;gap:6px}
.cur-btn{flex:1;padding:12px 0;border-radius:10px;border:1px solid var(--inputBorder);background:none;color:var(--textSec);font-family:'Cairo',sans-serif;font-size:14px;font-weight:700;cursor:pointer;transition:.2s}
.cur-btn.active-syp{background:rgba(46,166,122,.2);border-color:var(--primary);color:var(--primaryLight)}
.cur-btn.active-usd{background:rgba(88,166,255,.2);border-color:var(--accent);color:var(--accent)}

/* Buttons */
.btn-primary{width:100%;padding:14px;border-radius:14px;border:none;background:var(--primary);color:#fff;font-family:'Cairo',sans-serif;font-size:17px;font-weight:700;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:8px;transition:opacity .15s}
.btn-primary:active{opacity:.8}
.btn-primary:disabled{opacity:.5}
.btn-outline{width:100%;padding:13px;border-radius:12px;border:1px solid;background:none;font-family:'Cairo',sans-serif;font-size:15px;font-weight:700;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:8px;transition:opacity .15s}
.btn-outline:active{opacity:.7}
.btn-danger{border-color:var(--danger);color:var(--danger);background:var(--dangerBg)}
.btn-accent{border-color:var(--accent);color:var(--accent);background:rgba(88,166,255,.1)}
.btn-success{border-color:var(--success);color:var(--success);background:var(--successBg)}
.action-row{display:flex;gap:10px;margin-bottom:16px}
.action-row .btn-outline{flex:1}

/* Detail View */
.detail-header{display:flex;justify-content:space-between;align-items:center;padding:16px;padding-top:max(16px,env(safe-area-inset-top))}
.detail-back{background:none;border:none;color:var(--textSec);cursor:pointer;padding:4px}
.detail-back svg{width:24px;height:24px;fill:currentColor}
.detail-title{font-size:18px;font-weight:700;flex:1;text-align:center}
.detail-edit{background:none;border:none;color:var(--primary);cursor:pointer;padding:4px}
.detail-edit svg{width:22px;height:22px;fill:currentColor}
.price-display{background:var(--card);border:1px solid var(--cardBorder);border-radius:16px;padding:28px;text-align:center;margin:0 16px 14px}
.price-big{font-size:38px;font-weight:700;color:var(--primaryLight)}
.currency-name{font-size:15px;color:var(--textSec);font-weight:600;margin-top:4px}
.sync-badge-detail{display:inline-flex;align-items:center;gap:6px;background:rgba(210,153,34,.13);padding:4px 12px;border-radius:8px;margin-top:12px;color:var(--warning);font-size:12px;font-weight:600}
.detail-info{background:var(--card);border:1px solid var(--cardBorder);border-radius:16px;padding:16px 20px;margin:0 16px 14px}
.info-row{padding:12px 0;border-bottom:1px solid rgba(48,65,86,.25)}
.info-row:last-child{border-bottom:none}
.info-label{font-size:12px;color:var(--textMuted);font-weight:600;margin-bottom:3px;display:flex;align-items:center;gap:4px}
.info-value{font-size:14px;line-height:1.6}

/* Settings */
.section{background:var(--card);border:1px solid var(--cardBorder);border-radius:16px;padding:20px;margin-bottom:16px}
.section-header{display:flex;align-items:center;gap:10px;margin-bottom:16px}
.section-header svg{width:20px;height:20px;fill:var(--primary)}
.section-title{font-size:17px;font-weight:700}
.switch-row{display:flex;justify-content:space-between;align-items:center;padding-top:8px}
.switch-label{font-size:14px;font-weight:600}
.switch{position:relative;width:48px;height:28px;cursor:pointer}
.switch input{opacity:0;width:0;height:0}
.slider{position:absolute;inset:0;background:var(--border);border-radius:14px;transition:.3s}
.slider:before{content:'';position:absolute;width:22px;height:22px;border-radius:50%;background:#fff;top:3px;right:3px;transition:.3s}
.switch input:checked+.slider{background:var(--primary)}
.switch input:checked+.slider:before{transform:translateX(-20px)}
.switch-hint{font-size:12px;color:var(--textMuted);margin-top:6px;line-height:1.6}
.help-step{font-size:13px;color:var(--textSec);line-height:1.8;margin-bottom:8px}
.about-section{border-top:1px solid var(--border);text-align:center;padding:30px 0;margin-top:8px}
.about-section svg{width:32px;height:32px;fill:var(--primary);margin-bottom:8px}
.about-title{font-size:15px;font-weight:700}
.about-version{font-size:12px;color:var(--textMuted);margin-top:4px}

/* Toast */
.toast{position:fixed;top:20px;left:50%;transform:translateX(-50%);padding:12px 24px;border-radius:12px;font-family:'Cairo',sans-serif;font-size:14px;font-weight:600;z-index:9999;opacity:0;transition:opacity .3s;pointer-events:none;max-width:90%;text-align:center}
.toast.show{opacity:1}
.toast-success{background:var(--success);color:#fff}
.toast-error{background:var(--danger);color:#fff}
.toast-warning{background:var(--warning);color:#fff}

/* Modal */
.modal-overlay{position:fixed;inset:0;background:var(--overlay);z-index:1000;display:none;align-items:flex-end;justify-content:center}
.modal-overlay.show{display:flex}
.modal-content{background:var(--surface);border-radius:20px 20px 0 0;width:100%;max-width:480px;max-height:85vh;overflow-y:auto;padding:24px 20px;padding-bottom:calc(24px + env(safe-area-inset-bottom,0))}
.modal-title{font-size:18px;font-weight:700;text-align:center;margin-bottom:20px}
.modal-btns{display:flex;gap:10px;margin-top:20px}
.modal-btns button{flex:1}
.btn-cancel{padding:13px;border-radius:12px;border:1px solid var(--border);background:var(--surface);color:var(--textSec);font-family:'Cairo',sans-serif;font-size:15px;font-weight:600;cursor:pointer}
.btn-delete{padding:13px;border-radius:12px;border:none;background:var(--danger);color:#fff;font-family:'Cairo',sans-serif;font-size:15px;font-weight:700;cursor:pointer}

/* Header row actions */
.header-row{display:flex;justify-content:space-between;align-items:center}
.header-actions{display:flex;align-items:center;gap:12px}
.header-actions button{background:none;border:none;cursor:pointer;padding:4px;position:relative}
.header-actions svg{width:24px;height:24px;fill:var(--primary);pointer-events:none}
.sync-count{position:absolute;top:-4px;left:-4px;width:16px;height:16px;border-radius:50%;background:var(--warning);color:#fff;font-size:9px;display:flex;align-items:center;justify-content:center;font-weight:700}

/* Camera input for mobile */
.camera-scan-btn{width:100%;padding:14px;border-radius:14px;border:2px dashed var(--primary);background:rgba(46,166,122,.08);color:var(--primaryLight);font-family:'Cairo',sans-serif;font-size:16px;font-weight:700;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:10px;margin-bottom:12px;transition:.2s}
.camera-scan-btn:active{opacity:.7}
#scannerVideo{width:100%;max-width:400px;border-radius:12px;margin-bottom:12px}
.scanner-active #reader video{border-radius:12px}

/* Scrollbar */
::-webkit-scrollbar{width:4px}
::-webkit-scrollbar-track{background:transparent}
::-webkit-scrollbar-thumb{background:var(--border);border-radius:4px}
</style>
</head>
<body>

<div class="app">
  <!-- ===== Products Page ===== -->
  <div class="page active" id="page-products">
    <div class="page-header">
      <div class="header-row">
        <div class="page-title">المنتجات</div>
        <div class="header-actions">
          <button onclick="syncAll()" id="syncAllBtn" style="display:none" title="مزامنة الكل">
            <svg viewBox="0 0 24 24"><path d="M19.35 10.04C18.67 6.59 15.64 4 12 4 9.11 4 6.6 5.64 5.35 8.04 2.34 8.36 0 10.91 0 14c0 3.31 2.69 6 6 6h13c2.76 0 5-2.24 5-5 0-2.64-2.05-4.78-4.65-4.96zM14 13v4h-4v-4H7l5-5 5 5h-3z"/></svg>
            <span class="sync-count" id="syncCount">0</span>
          </button>
          <button onclick="showAddProduct()" title="إضافة منتج" data-testid="add-product-btn" type="button" aria-label="إضافة منتج">
            <svg viewBox="0 0 24 24" style="pointer-events:none"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm5 11h-4v4h-2v-4H7v-2h4V7h2v4h4v2z"/></svg>
          </button>
        </div>
      </div>
    </div>
    <div class="search-box">
      <svg viewBox="0 0 24 24"><path d="M15.5 14h-.79l-.28-.27A6.471 6.471 0 0016 9.5 6.5 6.5 0 109.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"/></svg>
      <input type="text" id="searchInput" placeholder="بحث بالاسم أو الباركود..." oninput="renderProducts()">
      <svg viewBox="0 0 24 24" id="clearSearch" style="display:none" onclick="clearSearch()"><path d="M12 2C6.47 2 2 6.47 2 12s4.47 10 10 10 10-4.47 10-10S17.53 2 12 2zm5 13.59L15.59 17 12 13.41 8.41 17 7 15.59 10.59 12 7 8.41 8.41 7 12 10.59 15.59 7 17 8.41 13.41 12 17 15.59z"/></svg>
    </div>
    <div class="filters-row">
      <div class="filter-group">
        <button class="chip active-sort" data-sort="date" onclick="setSort(this)">التاريخ</button>
        <button class="chip" data-sort="name" onclick="setSort(this)">الاسم</button>
        <button class="chip" data-sort="price" onclick="setSort(this)">السعر</button>
      </div>
      <div class="filter-group">
        <button class="chip active-filter" data-filter="all" onclick="setFilter(this)">الكل</button>
        <button class="chip" data-filter="USD" onclick="setFilter(this)">$</button>
        <button class="chip" data-filter="SYP" onclick="setFilter(this)">ل.س</button>
      </div>
    </div>
    <div class="page-scroll" id="productsList"></div>
  </div>

  <!-- ===== Scan Page ===== -->
  <div class="page" id="page-scan">
    <div class="page-header">
      <div class="page-title">مسح الباركود</div>
    </div>
    <div class="page-scroll" style="display:flex;flex-direction:column;align-items:center;justify-content:center;padding:20px">
      <div id="scanArea" style="width:100%;max-width:380px">
        <button class="camera-scan-btn" onclick="startScanner()" id="startScanBtn">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor"><path d="M9.5 6.5v3h-3v-3h3M11 5H5v6h6V5zm-1.5 9.5v3h-3v-3h3M11 13H5v6h6v-6zm6.5-6.5v3h-3v-3h3M19 5h-6v6h6V5zm-6 8h1.5v1.5H13V13zm1.5 1.5H16V16h-1.5v-1.5zM16 13h1.5v1.5H16V13zm-3 3h1.5v1.5H13V16zm1.5 1.5H16V19h-1.5v-1.5zM16 16h1.5v1.5H16V16zm1.5-1.5H19V16h-1.5v-1.5zm0 3H19V19h-1.5v-1.5z"/></svg>
          فتح الكاميرا لمسح الباركود
        </button>
        <div id="reader" style="display:none"></div>
        <button class="scan-manual-btn" id="stopScanBtn" style="display:none;margin:12px auto" onclick="stopScanner()">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12z"/></svg>
          إيقاف المسح
        </button>
        <div style="margin-top:20px;width:100%">
          <div style="text-align:center;color:var(--textSec);margin-bottom:12px;font-size:14px;font-weight:600">أو أدخل الباركود يدوياً</div>
          <div class="scan-input-row">
            <input type="text" id="manualBarcode" placeholder="رقم الباركود...">
            <button class="btn-primary" style="width:auto;padding:12px 20px;font-size:14px" onclick="manualSearch()">بحث</button>
          </div>
        </div>
        <div style="text-align:center;margin-top:20px">
          <span style="font-size:12px;color:var(--textMuted)">يدعم: QR, EAN-13, EAN-8, Code128, Code39, UPC</span>
        </div>
      </div>
    </div>
  </div>

  <!-- ===== Settings Page ===== -->
  <div class="page" id="page-settings">
    <div class="page-header">
      <div class="page-title">الإعدادات</div>
    </div>
    <div class="page-scroll">
      <div class="section">
        <div class="section-header">
          <svg viewBox="0 0 24 24"><path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm0 16H5V5h14v14z"/></svg>
          <span class="section-title">Google Sheets</span>
        </div>
        <div class="field">
          <label class="field-label">رابط Web App (Google Apps Script)</label>
          <input type="url" class="field-input" id="settingsWebAppUrl" placeholder="https://script.google.com/macros/s/..." dir="ltr" style="text-align:left">
        </div>
        <div class="field">
          <label class="field-label">معرّف ملف Google Sheets (Spreadsheet ID)</label>
          <input type="text" class="field-input" id="settingsSpreadsheetId" placeholder="أدخل Spreadsheet ID..." dir="ltr" style="text-align:left">
        </div>
        <div class="field">
          <label class="field-label">اسم الورقة (Sheet Name)</label>
          <input type="text" class="field-input" id="settingsSheetName" placeholder="Sheet1" dir="ltr" style="text-align:left">
        </div>
        <div class="switch-row">
          <span class="switch-label">المزامنة التلقائية</span>
          <label class="switch"><input type="checkbox" id="settingsAutoSync"><span class="slider"></span></label>
        </div>
        <div class="switch-hint">عند التفعيل، سيتم مزامنة المنتجات تلقائياً بعد كل عملية حفظ أو تعديل</div>
      </div>
      <div style="display:flex;flex-direction:column;gap:10px;margin-bottom:16px">
        <button class="btn-outline btn-accent" onclick="testSheetsConnection()">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M13 3c-4.97 0-9 4.03-9 9H1l3.89 3.89.07.14L9 12H6c0-3.87 3.13-7 7-7s7 3.13 7 7-3.13 7-7 7c-1.93 0-3.68-.79-4.94-2.06l-1.42 1.42C8.27 19.99 10.51 21 13 21c4.97 0 9-4.03 9-9s-4.03-9-9-9zm-1 5v5l4.28 2.54.72-1.21-3.5-2.08V8H12z"/></svg>
          اختبار الاتصال
        </button>
        <button class="btn-primary" onclick="saveSettings()">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M9 16.17L4.83 12l-1.42 1.41L9 19 21 7l-1.41-1.41z"/></svg>
          حفظ الإعدادات
        </button>
      </div>
      <div class="section">
        <div class="section-header">
          <svg viewBox="0 0 24 24" fill="var(--textSec)"><path d="M11 18h2v-2h-2v2zm1-16C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8zm0-14c-2.21 0-4 1.79-4 4h2c0-1.1.9-2 2-2s2 .9 2 2c0 2-3 1.75-3 5h2c0-2.25 3-2.5 3-5 0-2.21-1.79-4-4-4z"/></svg>
          <span class="section-title">كيفية إعداد Google Sheets</span>
        </div>
        <p class="help-step">1. أنشئ ملف Google Sheets جديد بالأعمدة التالية:<br>barcode, name, description, price, currency, notes, created_at, updated_at</p>
        <p class="help-step">2. من قائمة "الإضافات" اختر "Apps Script"</p>
        <p class="help-step">3. أنشئ Web App يستقبل طلبات POST ويكتب البيانات في الجدول</p>
        <p class="help-step">4. انسخ رابط Web App وأضفه في الحقل أعلاه</p>
        <p class="help-step">5. انسخ Spreadsheet ID من رابط الملف وأضفه أعلاه</p>
      </div>
      <div class="about-section">
        <svg viewBox="0 0 24 24"><path d="M9.5 6.5v3h-3v-3h3M11 5H5v6h6V5zm-1.5 9.5v3h-3v-3h3M11 13H5v6h6v-6zm6.5-6.5v3h-3v-3h3M19 5h-6v6h6V5z"/></svg>
        <div class="about-title">نظام إدارة المنتجات</div>
        <div class="about-version">الإصدار 1.0.0</div>
      </div>
    </div>
  </div>

  <!-- ===== Add/Edit Product Page ===== -->
  <div class="page" id="page-form">
    <div class="detail-header">
      <button class="detail-back" onclick="goBack()"><svg viewBox="0 0 24 24"><path d="M8.59 16.59L13.17 12 8.59 7.41 10 6l6 6-6 6z"/></svg></button>
      <span class="detail-title" id="formTitle">إضافة منتج</span>
      <div style="width:28px"></div>
    </div>
    <div class="page-scroll">
      <div class="form-card">
        <div class="field">
          <label class="field-label">الباركود *</label>
          <div style="display:flex;gap:8px">
            <input type="text" class="field-input" id="formBarcode" placeholder="رقم الباركود" style="flex:1;direction:ltr;text-align:left">
            <button class="btn-primary" style="width:auto;padding:10px 14px;font-size:13px;border-radius:10px" onclick="scanForForm()" title="مسح بالكاميرا">
              <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M9.5 6.5v3h-3v-3h3M11 5H5v6h6V5zm-1.5 9.5v3h-3v-3h3M11 13H5v6h6v-6zm6.5-6.5v3h-3v-3h3M19 5h-6v6h6V5zm-6 8h1.5v1.5H13V13zm1.5 1.5H16V16h-1.5v-1.5zM16 13h1.5v1.5H16V13zm-3 3h1.5v1.5H13V16zm1.5 1.5H16V19h-1.5v-1.5zM16 16h1.5v1.5H16V16zm1.5-1.5H19V16h-1.5v-1.5zm0 3H19V19h-1.5v-1.5z"/></svg>
            </button>
          </div>
          <div id="barcodeConfirm" style="display:none;margin-top:8px;padding:10px 14px;background:rgba(0,200,150,0.15);border:1px solid var(--accent);border-radius:10px;text-align:center">
            <span style="color:var(--accent);font-size:13px;font-weight:700">تم حفظ الباركود:</span>
            <span id="barcodeConfirmValue" style="color:#fff;font-size:15px;font-weight:700;margin-right:8px;direction:ltr;display:inline-block;letter-spacing:1px"></span>
          </div>
          <div id="formBarcodeScanner" style="margin-top:8px;display:none">
            <div id="formReader"></div>
            <button class="scan-manual-btn" style="margin:8px auto" onclick="stopFormScanner()">إيقاف المسح</button>
          </div>
        </div>
        <div class="field">
          <label class="field-label">اسم المنتج *</label>
          <input type="text" class="field-input" id="formName" placeholder="أدخل اسم المنتج">
        </div>
        <div class="field">
          <label class="field-label">الوصف (اختياري)</label>
          <textarea class="field-input field-textarea" id="formDesc" placeholder="وصف مختصر للمنتج"></textarea>
        </div>
        <div class="price-row">
          <div class="field">
            <label class="field-label">السعر *</label>
            <input type="number" class="field-input" id="formPrice" placeholder="0" dir="ltr" style="text-align:left">
          </div>
          <div class="field" style="width:120px">
            <label class="field-label">العملة</label>
            <div class="currency-btns">
              <button class="cur-btn active-syp" id="curSYP" onclick="setCur('SYP')">ل.س</button>
              <button class="cur-btn" id="curUSD" onclick="setCur('USD')">$</button>
            </div>
          </div>
        </div>
        <div class="field" style="margin-bottom:0">
          <label class="field-label">ملاحظات (اختياري)</label>
          <textarea class="field-input field-textarea" id="formNotes" placeholder="ملاحظات إضافية" style="min-height:50px"></textarea>
        </div>
      </div>
      <button class="btn-primary" onclick="saveProduct()" id="saveProductBtn" type="button" data-testid="save-product-btn">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M9 16.17L4.83 12l-1.42 1.41L9 19 21 7l-1.41-1.41z"/></svg>
        حفظ المنتج
      </button>
    </div>
  </div>

  <!-- ===== Product Detail Page ===== -->
  <div class="page" id="page-detail">
    <div class="detail-header">
      <button class="detail-back" onclick="goBack()"><svg viewBox="0 0 24 24"><path d="M8.59 16.59L13.17 12 8.59 7.41 10 6l6 6-6 6z"/></svg></button>
      <span class="detail-title">تفاصيل المنتج</span>
      <button class="detail-edit" onclick="editCurrentProduct()"><svg viewBox="0 0 24 24"><path d="M3 17.25V21h3.75L17.81 9.94l-3.75-3.75L3 17.25zM20.71 7.04c.39-.39.39-1.02 0-1.41l-2.34-2.34c-.39-.39-1.02-.39-1.41 0l-1.83 1.83 3.75 3.75 1.83-1.83z"/></svg></button>
    </div>
    <div class="page-scroll" id="detailContent"></div>
  </div>

  <!-- ===== Bottom Navigation ===== -->
  <nav class="bottom-nav">
    <button class="nav-btn active" data-page="products" onclick="switchPage('products')">
      <svg viewBox="0 0 24 24"><path d="M21 3H3c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h18c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm0 16H3V5h18v14zM5 15h14v3H5z"/></svg>
      المنتجات
    </button>
    <button class="nav-btn" data-page="scan" onclick="switchPage('scan')">
      <svg viewBox="0 0 24 24"><path d="M9.5 6.5v3h-3v-3h3M11 5H5v6h6V5zm-1.5 9.5v3h-3v-3h3M11 13H5v6h6v-6zm6.5-6.5v3h-3v-3h3M19 5h-6v6h6V5zm-6 8h1.5v1.5H13V13zm1.5 1.5H16V16h-1.5v-1.5zM16 13h1.5v1.5H16V13zm-3 3h1.5v1.5H13V16zm1.5 1.5H16V19h-1.5v-1.5zM16 16h1.5v1.5H16V16zm1.5-1.5H19V16h-1.5v-1.5zm0 3H19V19h-1.5v-1.5z"/></svg>
      المسح
    </button>
    <button class="nav-btn" data-page="settings" onclick="switchPage('settings')">
      <svg viewBox="0 0 24 24"><path d="M19.14 12.94c.04-.3.06-.61.06-.94 0-.32-.02-.64-.07-.94l2.03-1.58c.18-.14.23-.41.12-.61l-1.92-3.32c-.12-.22-.37-.29-.59-.22l-2.39.96c-.5-.38-1.03-.7-1.62-.94l-.36-2.54c-.04-.24-.24-.41-.48-.41h-3.84c-.24 0-.43.17-.47.41l-.36 2.54c-.59.24-1.13.57-1.62.94l-2.39-.96c-.22-.08-.47 0-.59.22L2.74 8.87c-.12.21-.08.47.12.61l2.03 1.58c-.05.3-.07.62-.07.94s.02.64.07.94l-2.03 1.58c-.18.14-.23.41-.12.61l1.92 3.32c.12.22.37.29.59.22l2.39-.96c.5.38 1.03.7 1.62.94l.36 2.54c.05.24.24.41.48.41h3.84c.24 0 .44-.17.47-.41l.36-2.54c.59-.24 1.13-.56 1.62-.94l2.39.96c.22.08.47 0 .59-.22l1.92-3.32c.12-.22.07-.47-.12-.61l-2.01-1.58zM12 15.6c-1.98 0-3.6-1.62-3.6-3.6s1.62-3.6 3.6-3.6 3.6 1.62 3.6 3.6-1.62 3.6-3.6 3.6z"/></svg>
      الإعدادات
    </button>
  </nav>
</div>

<!-- Delete Confirmation Modal -->
<div class="modal-overlay" id="deleteModal">
  <div class="modal-content">
    <div class="modal-title" id="deleteModalTitle">تأكيد الحذف</div>
    <p style="text-align:center;color:var(--textSec);font-size:14px;line-height:1.6" id="deleteModalMsg">هل أنت متأكد من حذف هذا المنتج؟</p>
    <div class="modal-btns">
      <button class="btn-cancel" onclick="closeDeleteModal()">إلغاء</button>
      <button class="btn-delete" onclick="confirmDelete()">حذف</button>
    </div>
  </div>
</div>

<!-- Toast -->
<div class="toast" id="toast"></div>

<script>
// ===================== DATA LAYER =====================
const DB_KEY = 'pm_products';
const SETTINGS_KEY = 'pm_settings';

function getProducts() {
  try { return JSON.parse(localStorage.getItem(DB_KEY)) || []; } catch { return []; }
}
function saveProducts(products) {
  localStorage.setItem(DB_KEY, JSON.stringify(products));
}
function genId() {
  return Date.now().toString(36) + Math.random().toString(36).substr(2, 9);
}
function getSettings() {
  try {
    return JSON.parse(localStorage.getItem(SETTINGS_KEY)) || { webAppUrl:'', spreadsheetId:'', sheetName:'Sheet1', autoSync:false };
  } catch {
    return { webAppUrl:'', spreadsheetId:'', sheetName:'Sheet1', autoSync:false };
  }
}
function saveSett(s) { localStorage.setItem(SETTINGS_KEY, JSON.stringify(s)); }

// ===================== STATE =====================
let currentSort = 'date';
let currentFilter = 'all';
let editingProductId = null;
let viewingProductId = null;
let deleteProductId = null;
let pageHistory = ['products'];
let html5QrCode = null;
let formHtml5QrCode = null;

// ===================== NAVIGATION =====================
function switchPage(name) {
  stopScanner();
  stopFormScanner();
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
  document.getElementById('page-' + name).classList.add('active');
  const navBtn = document.querySelector(`.nav-btn[data-page="${name}"]`);
  if (navBtn) navBtn.classList.add('active');
  if (name === 'products') renderProducts();
  if (name === 'settings') loadSettings();
  pageHistory = [name];
}

function showPage(name) {
  stopScanner();
  stopFormScanner();
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.getElementById('page-' + name).classList.add('active');
  document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
  pageHistory.push(name);
}

function goBack() {
  stopFormScanner();
  pageHistory.pop();
  const prev = pageHistory[pageHistory.length - 1] || 'products';
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.getElementById('page-' + prev).classList.add('active');
  const navBtn = document.querySelector(`.nav-btn[data-page="${prev}"]`);
  if (navBtn) {
    document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
    navBtn.classList.add('active');
  }
  if (prev === 'products') renderProducts();
}

// ===================== TOAST =====================
function showToast(msg, type = 'success') {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.className = 'toast toast-' + type + ' show';
  setTimeout(() => t.classList.remove('show'), 2500);
}

// ===================== PRODUCTS LIST =====================
function renderProducts() {
  let products = getProducts();
  const q = document.getElementById('searchInput').value.trim().toLowerCase();
  const clearBtn = document.getElementById('clearSearch');
  clearBtn.style.display = q ? 'block' : 'none';

  if (q) products = products.filter(p => p.name.toLowerCase().includes(q) || p.barcode.includes(q));
  if (currentFilter !== 'all') products = products.filter(p => p.currency === currentFilter);

  products.sort((a, b) => {
    if (currentSort === 'name') return a.name.localeCompare(b.name, 'ar');
    if (currentSort === 'price') return b.price - a.price;
    return new Date(b.createdAt) - new Date(a.createdAt);
  });

  const pendingCount = getProducts().filter(p => p.needsSync).length;
  document.getElementById('syncAllBtn').style.display = pendingCount > 0 ? 'block' : 'none';
  document.getElementById('syncCount').textContent = pendingCount;

  const container = document.getElementById('productsList');
  if (products.length === 0) {
    container.innerHTML = `<div class="empty-state">
      <svg viewBox="0 0 24 24"><path d="M21 3H3c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h18c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm0 16H3V5h18v14zM5 15h14v3H5z"/></svg>
      <div class="empty-title">${q ? 'لا توجد نتائج' : 'لا توجد منتجات بعد'}</div>
      <div class="empty-sub">${q ? 'جرب البحث بكلمات مختلفة' : 'امسح باركود أو أضف منتجاً جديداً'}</div>
    </div>`;
    return;
  }

  container.innerHTML = products.map(p => `
    <div class="product-card" onclick="viewProduct('${p.id}')">
      <div class="card-top">
        <div style="flex:1">
          <div class="card-name">${esc(p.name)}</div>
          <div class="card-barcode">${esc(p.barcode)}</div>
        </div>
        ${p.needsSync ? '<div class="sync-dot"></div>' : ''}
      </div>
      <div class="card-bottom">
        <div class="price-badge"><span class="price-text">${Number(p.price).toLocaleString()} ${p.currency === 'USD' ? '$' : 'ل.س'}</span></div>
        <span class="arrow-icon">&#x276E;</span>
      </div>
    </div>
  `).join('');
}

function esc(s) { const d = document.createElement('div'); d.textContent = s; return d.innerHTML; }
function clearSearch() { document.getElementById('searchInput').value = ''; renderProducts(); }

function setSort(btn) {
  currentSort = btn.dataset.sort;
  btn.parentElement.querySelectorAll('.chip').forEach(c => c.classList.remove('active-sort'));
  btn.classList.add('active-sort');
  renderProducts();
}
function setFilter(btn) {
  currentFilter = btn.dataset.filter;
  btn.parentElement.querySelectorAll('.chip').forEach(c => c.classList.remove('active-filter'));
  btn.classList.add('active-filter');
  renderProducts();
}

// ===================== VIEW PRODUCT =====================
function viewProduct(id) {
  viewingProductId = id;
  const p = getProducts().find(x => x.id === id);
  if (!p) return;

  const content = document.getElementById('detailContent');
  content.innerHTML = `
    <div class="price-display">
      <div class="price-big">${Number(p.price).toLocaleString()}</div>
      <div class="currency-name">${p.currency === 'USD' ? 'دولار أمريكي' : 'ليرة سورية'}</div>
      ${p.needsSync ? '<div class="sync-badge-detail"><svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M19.35 10.04C18.67 6.59 15.64 4 12 4 9.11 4 6.6 5.64 5.35 8.04 2.34 8.36 0 10.91 0 14c0 3.31 2.69 6 6 6h13c2.76 0 5-2.24 5-5 0-2.64-2.05-4.78-4.65-4.96zM14 13v4h-4v-4H7l5-5 5 5h-3z"/></svg> بحاجة مزامنة</div>' : ''}
    </div>
    <div class="detail-info">
      <div class="info-row"><div class="info-label">الباركود</div><div class="info-value" dir="ltr" style="text-align:right">${esc(p.barcode)}</div></div>
      <div class="info-row"><div class="info-label">اسم المنتج</div><div class="info-value">${esc(p.name)}</div></div>
      ${p.description ? `<div class="info-row"><div class="info-label">الوصف</div><div class="info-value">${esc(p.description)}</div></div>` : ''}
      ${p.notes ? `<div class="info-row"><div class="info-label">ملاحظات</div><div class="info-value">${esc(p.notes)}</div></div>` : ''}
      <div class="info-row"><div class="info-label">تاريخ الإضافة</div><div class="info-value">${formatDate(p.createdAt)}</div></div>
      <div class="info-row"><div class="info-label">آخر تعديل</div><div class="info-value">${formatDate(p.updatedAt)}</div></div>
    </div>
    <div class="action-row" style="padding:0 16px">
      <button class="btn-outline btn-accent" onclick="syncProduct('${p.id}')">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M19.35 10.04C18.67 6.59 15.64 4 12 4 9.11 4 6.6 5.64 5.35 8.04 2.34 8.36 0 10.91 0 14c0 3.31 2.69 6 6 6h13c2.76 0 5-2.24 5-5 0-2.64-2.05-4.78-4.65-4.96zM14 13v4h-4v-4H7l5-5 5 5h-3z"/></svg>
        مزامنة
      </button>
      <button class="btn-outline btn-danger" onclick="askDelete('${p.id}')">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M6 19c0 1.1.9 2 2 2h8c1.1 0 2-.9 2-2V7H6v12zM19 4h-3.5l-1-1h-5l-1 1H5v2h14V4z"/></svg>
        حذف
      </button>
    </div>`;
  showPage('detail');
}

function formatDate(iso) {
  if (!iso) return '-';
  try {
    const d = new Date(iso);
    return d.toLocaleDateString('ar-SA', { year:'numeric', month:'long', day:'numeric', hour:'2-digit', minute:'2-digit' });
  } catch { return iso; }
}

function editCurrentProduct() {
  if (!viewingProductId) return;
  const p = getProducts().find(x => x.id === viewingProductId);
  if (!p) return;
  showAddProduct(p);
}

// ===================== ADD / EDIT PRODUCT =====================
function showAddProduct(product = null) {
  editingProductId = product ? product.id : null;
  document.getElementById('formTitle').textContent = product ? 'تعديل المنتج' : 'إضافة منتج';
  document.getElementById('formBarcode').value = product ? product.barcode : '';
  document.getElementById('formName').value = product ? product.name : '';
  document.getElementById('formDesc').value = product ? product.description : '';
  document.getElementById('formPrice').value = product ? product.price : '';
  document.getElementById('formNotes').value = product ? product.notes : '';
  setCur(product ? product.currency : 'SYP');
  document.getElementById('saveProductBtn').innerHTML = `
    <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M9 16.17L4.83 12l-1.42 1.41L9 19 21 7l-1.41-1.41z"/></svg>
    ${product ? 'حفظ التعديلات' : 'حفظ المنتج'}`;
  document.getElementById('barcodeConfirm').style.display = 'none';
  if (product && product.barcode) {
    showBarcodeConfirm(product.barcode);
  }
  showPage('form');
}

function highlightBarcodeField() {
  const input = document.getElementById('formBarcode');
  const code = input.value.trim();
  if (code) {
    showBarcodeConfirm(code);
    input.style.borderColor = 'var(--accent)';
    input.style.boxShadow = '0 0 0 3px rgba(0,200,150,0.3)';
    setTimeout(() => {
      input.style.borderColor = '';
      input.style.boxShadow = '';
    }, 2000);
  }
}

function showBarcodeConfirm(code) {
  const el = document.getElementById('barcodeConfirm');
  document.getElementById('barcodeConfirmValue').textContent = code;
  el.style.display = 'block';
}

let formCurrency = 'SYP';
function setCur(c) {
  formCurrency = c;
  document.getElementById('curSYP').className = 'cur-btn' + (c === 'SYP' ? ' active-syp' : '');
  document.getElementById('curUSD').className = 'cur-btn' + (c === 'USD' ? ' active-usd' : '');
}

function saveProduct() {
  const barcode = document.getElementById('formBarcode').value.trim();
  const name = document.getElementById('formName').value.trim();
  const description = document.getElementById('formDesc').value.trim();
  const priceVal = document.getElementById('formPrice').value.trim();
  const notes = document.getElementById('formNotes').value.trim();

  if (!barcode) { showToast('يرجى إدخال الباركود', 'error'); return; }
  if (!name) { showToast('يرجى إدخال اسم المنتج', 'error'); return; }
  if (!priceVal || isNaN(Number(priceVal))) { showToast('يرجى إدخال سعر صحيح', 'error'); return; }

  const products = getProducts();
  const now = new Date().toISOString();

  if (editingProductId) {
    const idx = products.findIndex(p => p.id === editingProductId);
    if (idx !== -1) {
      // check barcode uniqueness (excluding current)
      const dup = products.find(p => p.barcode === barcode && p.id !== editingProductId);
      if (dup) { showToast('هذا الباركود مستخدم لمنتج آخر', 'error'); return; }
      products[idx] = { ...products[idx], barcode, name, description, price: Number(priceVal), currency: formCurrency, notes, needsSync: true, updatedAt: now };
      saveProducts(products);
      showToast('تم تعديل المنتج بنجاح');
      autoSyncIfEnabled(products[idx]);
      goBack();
      if (viewingProductId === editingProductId) viewProduct(editingProductId);
    }
  } else {
    const dup = products.find(p => p.barcode === barcode);
    if (dup) { showToast('هذا الباركود موجود بالفعل', 'warning'); viewProduct(dup.id); return; }
    const newP = { id: genId(), barcode, name, description, price: Number(priceVal), currency: formCurrency, notes, needsSync: true, createdAt: now, updatedAt: now };
    products.push(newP);
    saveProducts(products);
    showToast('تمت إضافة المنتج بنجاح');
    autoSyncIfEnabled(newP);
    goBack();
  }
  editingProductId = null;
}

// ===================== DELETE =====================
function askDelete(id) {
  deleteProductId = id;
  const p = getProducts().find(x => x.id === id);
  document.getElementById('deleteModalMsg').textContent = `هل أنت متأكد من حذف "${p ? p.name : ''}"؟`;
  document.getElementById('deleteModal').classList.add('show');
}
function closeDeleteModal() {
  document.getElementById('deleteModal').classList.remove('show');
  deleteProductId = null;
}
function confirmDelete() {
  if (!deleteProductId) return;
  let products = getProducts().filter(p => p.id !== deleteProductId);
  saveProducts(products);
  closeDeleteModal();
  showToast('تم حذف المنتج');
  switchPage('products');
}

// ===================== BARCODE SCANNER =====================
let scannerProcessing = false;
function startScanner() {
  scannerProcessing = false;
  const readerEl = document.getElementById('reader');
  readerEl.style.display = 'block';
  document.getElementById('startScanBtn').style.display = 'none';
  document.getElementById('stopScanBtn').style.display = 'flex';

  html5QrCode = new Html5Qrcode('reader');
  html5QrCode.start(
    { facingMode: 'environment' },
    { fps: 10, qrbox: { width: 250, height: 250 }, aspectRatio: 1.0 },
    (decodedText) => {
      if (scannerProcessing) return;
      scannerProcessing = true;
      stopScanner();
      handleScannedBarcode(decodedText);
    },
    () => {}
  ).catch(err => {
    showToast('تعذر فتح الكاميرا: ' + err, 'error');
    stopScanner();
  });
}

function stopScanner() {
  if (html5QrCode) {
    html5QrCode.stop().then(() => {
      html5QrCode.clear();
      html5QrCode = null;
    }).catch(() => { html5QrCode = null; });
  }
  const readerEl = document.getElementById('reader');
  if (readerEl) readerEl.style.display = 'none';
  const startBtn = document.getElementById('startScanBtn');
  if (startBtn) startBtn.style.display = 'flex';
  const stopBtn = document.getElementById('stopScanBtn');
  if (stopBtn) stopBtn.style.display = 'none';
}

function handleScannedBarcode(barcode) {
  if (!barcode || barcode.trim() === '') return;
  barcode = barcode.trim();
  const products = getProducts();
  const existing = products.find(p => p.barcode === barcode);
  if (existing) {
    showToast('تم العثور على المنتج: ' + existing.name);
    viewProduct(existing.id);
  } else {
    editingProductId = null;
    document.getElementById('formTitle').textContent = 'إضافة منتج';
    document.getElementById('formBarcode').value = barcode;
    document.getElementById('formName').value = '';
    document.getElementById('formDesc').value = '';
    document.getElementById('formPrice').value = '';
    document.getElementById('formNotes').value = '';
    setCur('SYP');
    document.getElementById('saveProductBtn').innerHTML = '<svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M9 16.17L4.83 12l-1.42 1.41L9 19 21 7l-1.41-1.41z"/></svg> حفظ المنتج';
    showPage('form');
    showBarcodeConfirm(barcode);
    highlightBarcodeField();
    showToast('تم مسح الباركود: ' + barcode + ' - أكمل بيانات المنتج', 'warning');
  }
}

function manualSearch() {
  const barcode = document.getElementById('manualBarcode').value.trim();
  if (!barcode) { showToast('أدخل رقم الباركود', 'error'); return; }
  handleScannedBarcode(barcode);
}

// Form barcode scanner
let formScanProcessing = false;
function scanForForm() {
  formScanProcessing = false;
  const scanArea = document.getElementById('formBarcodeScanner');
  scanArea.style.display = 'block';

  formHtml5QrCode = new Html5Qrcode('formReader');
  formHtml5QrCode.start(
    { facingMode: 'environment' },
    { fps: 10, qrbox: { width: 220, height: 220 }, aspectRatio: 1.0 },
    (decodedText) => {
      if (formScanProcessing) return;
      formScanProcessing = true;
      const code = decodedText.trim();
      document.getElementById('formBarcode').value = code;
      stopFormScanner();
      highlightBarcodeField();
      showToast('تم حفظ الباركود: ' + code);
    },
    () => {}
  ).catch(err => {
    showToast('تعذر فتح الكاميرا', 'error');
    stopFormScanner();
  });
}

function stopFormScanner() {
  if (formHtml5QrCode) {
    formHtml5QrCode.stop().then(() => {
      formHtml5QrCode.clear();
      formHtml5QrCode = null;
    }).catch(() => { formHtml5QrCode = null; });
  }
  const el = document.getElementById('formBarcodeScanner');
  if (el) el.style.display = 'none';
}

// ===================== SETTINGS =====================
function loadSettings() {
  const s = getSettings();
  document.getElementById('settingsWebAppUrl').value = s.webAppUrl || '';
  document.getElementById('settingsSpreadsheetId').value = s.spreadsheetId || '';
  document.getElementById('settingsSheetName').value = s.sheetName || 'Sheet1';
  document.getElementById('settingsAutoSync').checked = !!s.autoSync;
}

function saveSettings() {
  const s = {
    webAppUrl: document.getElementById('settingsWebAppUrl').value.trim(),
    spreadsheetId: document.getElementById('settingsSpreadsheetId').value.trim(),
    sheetName: document.getElementById('settingsSheetName').value.trim() || 'Sheet1',
    autoSync: document.getElementById('settingsAutoSync').checked,
  };
  saveSett(s);
  showToast('تم حفظ الإعدادات بنجاح');
}

// ===================== GOOGLE SHEETS SYNC =====================
async function syncProduct(id) {
  const s = getSettings();
  if (!s.webAppUrl) { showToast('لم يتم تعيين رابط Google Sheets', 'error'); return; }
  const products = getProducts();
  const p = products.find(x => x.id === id);
  if (!p) return;

  try {
    const res = await fetch(s.webAppUrl, {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        action: 'upsert', spreadsheetId: s.spreadsheetId, sheetName: s.sheetName,
        product: { barcode: p.barcode, name: p.name, description: p.description, price: p.price, currency: p.currency, notes: p.notes, createdAt: p.createdAt, updatedAt: p.updatedAt }
      })
    });
    if (res.ok) {
      p.needsSync = false;
      saveProducts(products);
      showToast('تمت المزامنة بنجاح');
      if (viewingProductId === id) viewProduct(id);
      renderProducts();
    } else {
      showToast('خطأ في المزامنة: ' + res.status, 'error');
    }
  } catch (e) {
    showToast('فشل الاتصال بالإنترنت', 'error');
  }
}

async function syncAll() {
  const s = getSettings();
  if (!s.webAppUrl) { showToast('لم يتم تعيين رابط Google Sheets', 'error'); return; }
  const products = getProducts();
  const toSync = products.filter(p => p.needsSync);
  if (toSync.length === 0) { showToast('لا توجد منتجات بحاجة مزامنة'); return; }

  try {
    const res = await fetch(s.webAppUrl, {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        action: 'bulk_upsert', spreadsheetId: s.spreadsheetId, sheetName: s.sheetName,
        products: toSync.map(p => ({ barcode: p.barcode, name: p.name, description: p.description, price: p.price, currency: p.currency, notes: p.notes, createdAt: p.createdAt, updatedAt: p.updatedAt }))
      })
    });
    if (res.ok) {
      toSync.forEach(p => p.needsSync = false);
      saveProducts(products);
      showToast(`تمت مزامنة ${toSync.length} منتج بنجاح`);
      renderProducts();
    } else {
      showToast('خطأ في المزامنة', 'error');
    }
  } catch (e) {
    showToast('فشل الاتصال بالإنترنت', 'error');
  }
}

async function testSheetsConnection() {
  const url = document.getElementById('settingsWebAppUrl').value.trim();
  if (!url) { showToast('أدخل رابط Web App أولاً', 'error'); return; }
  try {
    const res = await fetch(url, {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ action: 'test', spreadsheetId: document.getElementById('settingsSpreadsheetId').value.trim(), sheetName: document.getElementById('settingsSheetName').value.trim() || 'Sheet1' })
    });
    if (res.ok) { showToast('تم الاتصال بـ Google Sheets بنجاح'); }
    else { showToast('فشل الاتصال: ' + res.status, 'error'); }
  } catch (e) {
    showToast('تعذر الاتصال - تحقق من الرابط', 'error');
  }
}

function autoSyncIfEnabled(product) {
  const s = getSettings();
  if (s.autoSync && s.webAppUrl) {
    syncProduct(product.id).catch(() => {});
  }
}

// ===================== INIT =====================
document.addEventListener('DOMContentLoaded', () => {
  renderProducts();
  loadSettings();
  // Handle Enter key on manual barcode input
  document.getElementById('manualBarcode').addEventListener('keydown', (e) => {
    if (e.key === 'Enter') manualSearch();
  });
});
</script>
</body>
</html>
