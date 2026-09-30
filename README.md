<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<meta name="theme-color" content="#0d5c63">
<title>福州 5 日旅行手册</title>
<style>
*{box-sizing:border-box;-webkit-tap-highlight-color:transparent}
body{margin:0;font:15px/1.65 -apple-system,BlinkMacSystemFont,"PingFang SC","Hiragino Sans GB","Microsoft YaHei",sans-serif;background:#f2f2f7;color:#1c1c1e;-webkit-text-size-adjust:100%;padding-bottom:calc(env(safe-area-inset-bottom) + 24px)}
header{position:sticky;top:0;z-index:50;background:rgba(255,255,255,.94);backdrop-filter:blur(14px);-webkit-backdrop-filter:blur(14px);border-bottom:1px solid #e5e5ea;padding-top:calc(env(safe-area-inset-top) + 8px)}
.hd{padding:0 16px}
h1{margin:0 0 8px;font-size:17px;font-weight:600;letter-spacing:.3px}
.tabs{display:flex}
.tab{flex:1;padding:9px 0 11px;border:0;background:none;font-size:15px;color:#8e8e93;font-weight:500;border-bottom:2px solid transparent;cursor:pointer;font-family:inherit}
.tab.on{color:#0d5c63;border-bottom-color:#0d5c63}
main{padding:12px;max-width:720px;margin:0 auto}
.panel{display:none}
.panel.on{display:block}
.day{background:#fff;border-radius:14px;margin-bottom:10px;box-shadow:0 1px 3px rgba(0,0,0,.06);overflow:hidden}
.day-hd{display:flex;align-items:center;gap:10px;padding:14px 16px;cursor:pointer;user-select:none}
.d-label{font-weight:600;color:#0d5c63;font-size:15px;flex:none}
.d-sub{flex:1;font-size:12.5px;color:#8e8e93;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.arrow{color:#c7c7cc;transition:transform .22s;font-size:12px;flex:none}
.day.open .arrow{transform:rotate(90deg)}
.day-bd{display:none;padding:0 14px 16px;border-top:1px solid #f2f2f7}
.day.open .day-bd{display:block}
.tools{display:flex;gap:8px;padding:12px 0 4px}
.btn{flex:1;padding:9px 8px;border-radius:10px;border:1px solid #d8e6e7;background:#f0f7f8;color:#0d5c63;font-size:13px;font-weight:500;cursor:pointer;font-family:inherit;text-align:center;text-decoration:none;display:block}
.btn:active{background:#e0eff1}
.btn.solid{background:#0d5c63;color:#fff;border-color:#0d5c63}
.btn.solid:active{background:#0a4a50}
.mapwrap{display:none;margin:10px 0 4px;background:#f8fafb;border-radius:12px;padding:10px;border:1px solid #e8eef0}
.mapwrap.on{display:block}
.mapwrap svg{border-radius:8px;display:block}
.legend{display:flex;flex-wrap:wrap;gap:12px;font-size:11.5px;color:#6b7280;padding:8px 2px 2px}
.legend i{display:inline-block;width:9px;height:9px;border-radius:50%;margin-right:4px;vertical-align:middle}
.hotel{display:flex;gap:8px;align-items:flex-start;background:#f7f4ff;border:1px solid #e8e0ff;border-radius:11px;padding:11px 12px;margin:10px 0 4px;font-size:13.5px}
.hotel .hb{flex:1;min-width:0}
.hotel .ht{font-weight:600;color:#7c3aed;margin-bottom:2px}
.hotel .ha{color:#6b7280;font-size:12.5px}
.spot{border:1px solid #ececf0;border-radius:12px;padding:12px;margin-top:10px;background:#fcfcfd}
.spot-top{display:flex;gap:9px;align-items:flex-start}
.idx{width:22px;height:22px;border-radius:50%;background:#2563eb;color:#fff;font-size:11.5px;display:flex;align-items:center;justify-content:center;flex:none;margin-top:1px;font-weight:600}
.idx.mv{background:#f59e0b}
.sname{flex:1;font-weight:600;font-size:15px;min-width:0;word-break:break-word}
.sname a{color:#1c1c1e;text-decoration:none;border-bottom:1px dashed #c7c7cc}
.tagmv{display:inline-block;font-size:10.5px;font-weight:500;color:#b45309;background:#fef3c7;padding:1px 6px;border-radius:5px;margin-left:5px;vertical-align:1px}
.nav{flex:none;font-size:12px;color:#0d5c63;background:#f0f7f8;border:1px solid #d8e6e7;border-radius:8px;padding:4px 9px;text-decoration:none;font-weight:500}
.hours{font-size:12.5px;color:#6b7280;margin:6px 0 0 31px}
.desc{font-size:13.5px;color:#3f3f46;margin:7px 0 0 31px;line-height:1.62}
.hint{font-size:12.5px;color:#9a6b00;background:#fffbeb;border-left:3px solid #fbbf24;padding:6px 9px;border-radius:0 7px 7px 0;margin:8px 0 0 31px}
.sub{margin:8px 0 0 31px;border-left:2px solid #e5e7eb;padding-left:11px}
.sub-i{font-size:13px;margin-bottom:8px}
.sub-i b{color:#0d5c63;font-weight:600}
.sub-i span{color:#52525b}
.foods{margin:9px 0 0 31px;padding-top:9px;border-top:1px dashed #ececf0}
.foods-t{font-size:12px;color:#9a3412;font-weight:600;margin-bottom:6px}
.food{display:flex;align-items:baseline;gap:7px;font-size:13px;margin-bottom:5px}
.food a{color:#c2410c;text-decoration:none;border-bottom:1px dashed #fdba74}
.food .fd{font-size:11.5px;color:#a1a1aa;flex:none;margin-left:auto}
.link{display:flex;align-items:center;gap:7px;margin-top:10px;padding-top:10px;border-top:1px dashed #ececf0;font-size:12.5px;color:#6b7280}
.link b{color:#0d5c63;font-weight:600}
.link .lv{margin-left:auto;color:#a1a1aa;font-size:11.5px}
.extra{background:#f0f9ff;border:1px solid #dbeafe;border-radius:11px;padding:11px 12px;margin-top:10px;font-size:13.5px}
.extra .et{font-weight:600;color:#1d4ed8;margin-bottom:3px;font-size:13px}
/* 备注页 */
.nbar{display:flex;gap:8px;margin-bottom:12px}
.nbar .btn{flex:1}
.nday{background:#fff;border-radius:14px;margin-bottom:10px;box-shadow:0 1px 3px rgba(0,0,0,.06);overflow:hidden}
.nday-hd{display:flex;align-items:center;gap:10px;padding:14px 16px;cursor:pointer;user-select:none;font-weight:600;color:#0d5c63;font-size:15px}
.nday-hd .nds{flex:1;font-size:12.5px;color:#8e8e93;font-weight:400}
.nday-bd{display:none;padding:0 14px 16px;border-top:1px solid #f2f2f7}
.nday.open .nday-bd{display:block}
.nblock{margin-top:14px}
.nlabel{font-size:13px;font-weight:600;color:#3f3f46;margin-bottom:6px;display:flex;align-items:center;gap:6px}
.nlabel .ni{width:18px;height:18px;border-radius:50%;background:#2563eb;color:#fff;font-size:10.5px;display:flex;align-items:center;justify-content:center;font-weight:600;flex:none}
textarea{width:100%;min-height:70px;border:1px solid #e4e4e7;border-radius:10px;padding:9px 11px;font:14px/1.6 inherit;font-family:inherit;resize:vertical;background:#fafafa;color:#1c1c1e;outline:none}
textarea:focus{border-color:#0d5c63;background:#fff}
.imgs{display:flex;flex-wrap:wrap;gap:8px;margin-top:8px}
.thumb{position:relative;width:72px;height:72px;border-radius:9px;overflow:hidden;border:1px solid #e4e4e7}
.thumb img{width:100%;height:100%;object-fit:cover;display:block}
.thumb .del{position:absolute;top:2px;right:2px;width:19px;height:19px;border-radius:50%;background:rgba(0,0,0,.6);color:#fff;font-size:13px;line-height:19px;text-align:center;cursor:pointer;font-style:normal}
.addimg{margin-top:8px;font-size:12.5px;color:#0d5c63;background:#f0f7f8;border:1px dashed #b8d4d6;border-radius:9px;padding:7px 12px;cursor:pointer;font-family:inherit;width:100%}
.addimg:active{background:#e0eff1}
.empty{text-align:center;color:#a1a1aa;font-size:13px;padding:30px 0}
.toast{position:fixed;left:50%;bottom:calc(env(safe-area-inset-bottom) + 24px);transform:translateX(-50%) translateY(20px);background:rgba(28,28,30,.92);color:#fff;font-size:13px;padding:9px 18px;border-radius:20px;opacity:0;transition:.25s;pointer-events:none;z-index:999;white-space:nowrap}
.toast.on{opacity:1;transform:translateX(-50%) translateY(0)}
</style>
</head>
<body>
<header>
  <div class="hd">
    <h1>福州 5 日旅行手册</h1>
    <div class="tabs">
      <button class="tab on" data-tab="iti">行程</button>
      <button class="tab" data-tab="not">备注</button>
    </div>
  </div>
</header>
<main>
  <section id="p-iti" class="panel on"></section>
  <section id="p-not" class="panel"></section>
</main>
<div class="toast" id="toast"></div>

<script>
/* ============ 数据 ============ */
const TRIP = {
  days: [
    {
      id: 'd1', label: 'Day 1', sub: '上下杭 · 烟台山',
      hotel: { name: '聚春园会展酒店', addr: '仓山区城门镇潘墩路189号', lng: 119.2783, lat: 26.0278 },
      spots: [
        { id:'d1-1', name:'古田会馆', lng:119.2977, lat:26.0538, hours:'8:30-12:00，13:30-17:00',
          desc:'民国四年（1915）由古田商帮集资建造，福州保存最完整的会馆之一，省级文保。馆内保留精美木雕、石雕与戏台。',
          metro:'达道站（1号线）约 700m' },
        { id:'d1-2', name:'陈文龙尚书庙', lng:119.3026, lat:26.0563, hours:'9:00-11:00，15:00-17:00',
          desc:'原万寿尚书庙，2006 年移建至三通桥北。主殿沿用明代梁架，存林则徐题匾、琉球碑刻、乾隆狮钮铁印，祀南宋抗元名臣陈文龙。' },
        { id:'d1-3', name:'张真君祖殿', lng:119.30182, lat:26.05544, hours:'9:00-11:30，14:30-17:00',
          desc:'南宋始建，闽商奉张真君为商神。殿前星安桥、三通桥，是上下杭商帮文化的核心地带。' },
        { id:'d1-4', name:'福州市非物质文化遗产展示馆', lng:119.2990, lat:26.0548, hours:'9:00-16:30 / 9:00-22:00',
          desc:'依托省级文保「罗氏绸缎庄」设立，展示软木画、脱胎漆器、寿山石雕等福州非遗项目。下杭路 181 号。',
          hint:'领卡包地点' },
        { id:'d1-5', name:'福州市博物馆', lng:119.32740, lat:26.06382, hours:'9:00-17:00 / 9:00-20:00', mv:true,
          desc:'国家二级博物馆，馆藏寿山石雕、脱胎漆器、书画等。位于晋安区文博路 8 号，与其他点位相距较远。' },
        { id:'d1-6', name:'黄培松故居', lng:119.2960, lat:26.0520, hours:'9:00-20:00',
          desc:'清朝最后一位武状元黄培松的故居，现为福州市美术馆。中平路 172 号。' },
        { id:'d1-7', name:'采峰别墅', lng:119.29952, lat:26.05626, hours:'10:00-20:00',
          desc:'马来西亚侨领杨鸿斌 1920 年所建，中西合璧，福州保存最完好的近代侨厝之一。' },
        { id:'d1-8', name:'永德会馆', lng:119.2993, lat:26.0549, hours:'9:00-22:00',
          desc:'清雍正年间永春、德化商帮共建，中西合璧，罗马式石柱。下杭路 179 号。' },
        { id:'d1-9', name:'建郡会馆', lng:119.2985, lat:26.0552, hours:'10:00-22:00',
          desc:'清嘉庆年间建宁府商帮所建，戏台藻井精美，市级文保。上杭路 128 号。' },
        { id:'d1-10', name:'何氏祠堂', lng:119.2972, lat:26.0562, hours:'9:00-22:00',
          desc:'民国初年何氏家祠，穿斗式木构。上杭路 43 号。',
          hint:'手工观演项目另收费' },
        { id:'d1-11', name:'上下杭展馆', lng:119.2988, lat:26.0545, hours:'9:00-22:00',
          desc:'利发巷 61 号，市级文保。展示上下杭商贾文化、码头文化与海丝历史。' },
        { id:'d1-12', name:'烟台山街区', lng:119.3055, lat:26.0439, hours:'全天开放',
          desc:'仓山区梅坞路、仓前路一带的万国建筑群，2021 年商业漫步街区开街，夜间散步胜地。',
          metro:'上藤站（1号线）约 500m' }
      ],
      foods: [
        { name:'大向沸腾鱼（怡丰小区店）', lng:119.3020, lat:26.0485 },
        { name:'兵俤粉干卤味（福州总店）', lng:119.3080, lat:26.0500 },
        { name:'没牙伯花生汤店', lng:119.3078, lat:26.0500 },
        { name:'凉凉冰饭·烧烤（王庄店）', lng:119.3230, lat:26.0770 },
        { name:'江五毛砂锅土豆粉（王庄店）', lng:119.3220, lat:26.0775 },
        { name:'松花堂寿司（振兴花园店）', lng:119.3090, lat:26.0420 },
        { name:'兄帝美食店·台湾美食', lng:119.3120, lat:26.0360 },
        { name:'乡知味拌面（下藤小区店）', lng:119.3180, lat:26.0400 },
        { name:'达道牛肉（融侨则徐道壹号B区店）', lng:119.3050, lat:26.0530 }
      ]
    },
    {
      id: 'd2', label: 'Day 2', sub: '文庙 · 三坊七巷 · 裴仙宫',
      spots: [
        { id:'d2-1', name:'福州文庙', lng:119.2940, lat:26.0865, hours:'9:00-17:00',
          desc:'全国重点文保，市区现存规模最大的清晚期官式建筑群，大成殿为清代风格。鼓楼区圣庙路 10 号。',
          metro:'南门兜站（1/2号线）约 450m' },
        { id:'d2-2', name:'萨镇冰故居', lng:119.2960, lat:26.0858, hours:'以现场公告为准',
          desc:'朱紫坊 22 号。萨镇冰（1859-1952），清末海军统制、民国海军总长、新中国第一届全国政协委员，晚年居此。' },
        { id:'d2-3', name:'三坊七巷', lng:119.2930, lat:26.0850, hours:'街区全天开放',
          desc:'国家 5A 级景区，中国十大历史文化名街。以南后街为中轴，西侧三坊、东侧七巷，呈「非」字形格局，现存古民居约 270 座。',
          metro:'东街口站（1号线）约 350m',
          hint:'10:00 沈葆桢故居有「名城少年」古厝情景表演（以现场公告为准）',
          sub:[
            { n:'南后街', d:'三坊七巷中轴，全长约 1000 米，唐宋年间已是繁华商业街。' },
            { n:'林觉民·冰心故居', d:'杨桥东路 17 号，「一座宅院，两位名人」。林觉民《与妻书》诞生地，后为冰心祖父购得，冰心幼年在此居住。全国重点文保，免费。' },
            { n:'严复故居', d:'郎官巷 20 号。1920 年李厚基为严复购置，严复在此居住至 1921 年病逝。主座为清代福州古民居，花厅中西合璧。' },
            { n:'水榭戏台', d:'衣锦坊 4 号。明万历郑氏宅院，清道光孙翼谋家族扩建。福州仅存的水上戏台，面积 30㎡，三面临水，池水回音声如绕梁。' },
            { n:'沈葆桢故居', d:'宫巷 26 号。始建于明天启年间，三坊七巷建设年代最久远的文保单位之一，占地超 2700㎡，可见明、清、民国三代建筑特征。' },
            { n:'小黄楼', d:'黄巷 36 号。相传为唐代黄璞故居遗址，清梁章钜重修，东花厅仿沧浪亭而建。现为中国涉台楹联博物馆。门票 20 元/人。' }
          ] },
        { id:'d2-4', name:'福州市海上丝绸之路展示馆', lng:119.2915, lat:26.0845, hours:'9:00-17:00 / 9:00-22:00',
          desc:'文儒坊 17 号，福州市博物馆分馆，展示福州海上丝绸之路历史。' },
        { id:'d2-5', name:'福州裴仙宫', lng:119.29201, lat:26.09113, hours:'6:00-18:00',
          desc:'北宋治平年间建，宫中古榕称「榕城第一古榕」。' },
        { id:'d2-6', name:'福州市博物馆', lng:119.32740, lat:26.06382, hours:'9:00-17:00 / 9:00-20:00', mv:true,
          desc:'国家二级博物馆，与 Day 1 为同一地点，作为机动行程。' }
      ],
      foods: [
        { name:'依珠小吃店捞化卤味', lng:119.3090, lat:26.0880 },
        { name:'食仙·闽味馆店（南门店）', lng:119.2960, lat:26.0800 },
        { name:'哇哈冰饭', lng:119.2980, lat:26.0830 },
        { name:'小叫天泡椒活田鸡（三坊七巷店）', lng:119.2940, lat:26.0860 },
        { name:'Le Temps时间甜品', lng:119.2920, lat:26.0848 },
        { name:'毓家茶铺（达明1号店）', lng:119.2950, lat:26.0890 },
        { name:'最福舟·闽菜·海鲜小馆（达明美食街店）', lng:119.2955, lat:26.0895 },
        { name:'Gogo泰面', lng:119.2960, lat:26.0870 },
        { name:'林小满福建砂锅焗海鲜（三坊七巷店）', lng:119.2950, lat:26.0865 },
        { name:'凉凉冰饭·烧烤（王庄店）', lng:119.3230, lat:26.0770 },
        { name:'江五毛砂锅土豆粉（王庄店）', lng:119.3220, lat:26.0775 }
      ]
    },
    {
      id: 'd3', label: 'Day 3', sub: '屏山 · 冶山 · 西湖',
      spots: [
        { id:'d3-1', name:'屏山公园', lng:119.2870, lat:26.1020, hours:'8:30-12:00，15:00-18:00',
          desc:'福州三山之一。镇海楼为明代福州最高建筑，2006 年重建，可俯瞰全城。鼓楼区福飞南路 139 号。',
          metro:'屏山站（1号线）约 600m' },
        { id:'d3-2', name:'华林寺', lng:119.2905, lat:26.0965, hours:'9:00-17:00（周一闭馆）',
          desc:'北宋乾德二年（964）建，长江以南最古老木构建筑，全国重点文保。门票 2 元。鼓楼区华林路 78 号。' },
        { id:'d3-3', name:'冶山春秋博物馆', lng:119.2940, lat:26.0920, hours:'9:00-12:00，13:00-17:00',
          desc:'展示冶山 2200 余年历史，西汉「万岁」瓦当残片为关键物证。鼓楼区冶山路 33 号。' },
        { id:'d3-4', name:'欧冶池', lng:119.2950, lat:26.0915, hours:'9:00-12:00，13:00-17:00',
          desc:'相传春秋欧冶子铸剑处，市级文保，现属省财政厅院内。' },
        { id:'d3-5', name:'福州冶山唐代马球场遗址', lng:119.2935, lat:26.0925, hours:'以现场公告为准',
          desc:'我国挖掘出土唯一的唐代马球场遗迹，位于冶山春秋园内。鼓东街道中山路 23 号中山大院。' },
        { id:'d3-6', name:'福建博物院', lng:119.28760, lat:26.09410, hours:'9:00-20:00',
          desc:'国家一级博物馆，位于西湖公园内。',
          hint:'重点看 9 号展厅' },
        { id:'d3-7', name:'西湖公园', lng:119.29627, lat:26.09942, hours:'全天开放',
          desc:'福州最古老的公园，五代时已是游览胜地。',
          metro:'屏山站（1号线）约 500m',
          hint:'则徐广场 19:30 有越剧综艺表演' }
      ],
      foods: []
    },
    {
      id: 'd4', label: 'Day 4', sub: '鼓山 · 涌泉寺',
      spots: [
        { id:'d4-1', name:'鼓山旅游景区', lng:119.3800, lat:26.0550, hours:'全天开放',
          desc:'福州最著名的风景区，海拔 925 米，摩崖石刻众多，登山古道 1800 余级。',
          metro:'鼓山站（2号线）约 800m' },
        { id:'d4-2', name:'涌泉寺', lng:119.3760, lat:26.0570, hours:'6:00-18:00',
          desc:'鼓山山腰，建于梁开平二年（908），全国重点佛教寺院。可乘景区区间车直达寺前。' }
      ],
      foods: []
    },
    {
      id: 'd5', label: 'Day 5', sub: '马尾 · 船政文化',
      spots: [
        { id:'d5-1', name:'中国船政文化博物馆', lng:119.4560, lat:25.9880, hours:'9:00-17:00（周一闭馆）',
          desc:'马尾区，展示马尾船政历史，中国近代海军的摇篮。免费开放。',
          metro:'马尾港站（2号线东延段，以实际开通为准）' }
      ],
      foods: []
    }
  ]
};

/* ============ 工具 ============ */
const $ = s => document.querySelector(s);
const esc = s => String(s == null ? '' : s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const R = 6371000, RAD = Math.PI / 180;
function dist(a, b) {
  const dLat = (b.lat - a.lat) * RAD, dLng = (b.lng - a.lng) * RAD;
  const x = Math.sin(dLat/2)**2 + Math.cos(a.lat*RAD) * Math.cos(b.lat*RAD) * Math.sin(dLng/2)**2;
  return 2 * R * Math.asin(Math.sqrt(x));
}
const fmtD = m => m < 1000 ? Math.round(m) + ' m' : (m/1000).toFixed(1) + ' km';
function toast(msg) {
  const t = $('#toast'); t.textContent = msg; t.classList.add('on');
  clearTimeout(t._t); t._t = setTimeout(() => t.classList.remove('on'), 1800);
}
function navUrl(s) {
  if (s.lat && s.lng) {
    return `https://uri.amap.com/marker?position=${s.lng},${s.lat}&name=${encodeURIComponent(s.name)}&src=travel&coordinate=gaode&callnative=1`;
  }
  return `https://uri.amap.com/search?keyword=${encodeURIComponent(s.name + ' 福州')}&src=travel&callnative=1`;
}
function foodUrl(f) {
  return `https://uri.amap.com/search?keyword=${encodeURIComponent(f.name + ' 福州')}&src=travel&callnative=1`;
}
function routeUrl(spots) {
  const v = spots.filter(s => s.lat && s.lng);
  if (!v.length) return null;
  if (v.length === 1) return navUrl(v[0]);
  const f = v[0], t = v[v.length - 1], via = v.slice(1, -1);
  let u = `https://uri.amap.com/navigation?from=${f.lng},${f.lat},${encodeURIComponent(f.name)}&to=${t.lng},${t.lat},${encodeURIComponent(t.name)}&mode=car&coordinate=gaode&callnative=1&src=travel`;
  if (via.length) u += `&via=${via.map(p => `${p.lng},${p.lat},${encodeURIComponent(p.name)}`).join('|')}`;
  return u;
}

/* ============ SVG 示意图 ============ */
function sketchSVG(day) {
  const spots = day.spots.filter(s => s.lat && s.lng);
  const foods = (day.foods || []).filter(f => f.lat && f.lng);
  const hotel = day.hotel && day.hotel.lat ? [day.hotel] : [];
  const all = [...spots, ...foods, ...hotel];
  if (all.length < 2) return '';
  const lngs = all.map(p => p.lng), lats = all.map(p => p.lat);
  let minLng = Math.min(...lngs), maxLng = Math.max(...lngs);
  let minLat = Math.min(...lats), maxLat = Math.max(...lats);
  if (maxLng - minLng < 1e-4) { minLng -= 5e-4; maxLng += 5e-4; }
  if (maxLat - minLat < 1e-4) { minLat -= 5e-4; maxLat += 5e-4; }
  const W = 360, H = 320, PAD = 42;
  const cosLat = Math.cos((minLat + maxLat) / 2 * RAD);
  const sx = (maxLng - minLng) * cosLat, sy = maxLat - minLat;
  const k = Math.min((W - 2*PAD) / sx, (H - 2*PAD) / sy);
  const ox = (W - sx * k) / 2, oy = (H - sy * k) / 2;
  const px = (lng, lat) => [ ox + (lng - minLng) * cosLat * k, H - oy - (lat - minLat) * k ];
  let s = `<svg viewBox="0 0 ${W} ${H}" xmlns="http://www.w3.org/2000/svg" font-family="-apple-system,BlinkMacSystemFont,PingFang SC,sans-serif">`;
  s += `<rect width="${W}" height="${H}" fill="#f8fafb" rx="10"/>`;
  const pts = spots.map(x => px(x.lng, x.lat));
  if (pts.length > 1) {
    s += `<path d="${pts.map((p,i)=>(i?'L':'M')+p[0].toFixed(1)+' '+p[1].toFixed(1)).join(' ')}" fill="none" stroke="#2563eb" stroke-width="1.6" stroke-dasharray="5 4" opacity=".5"/>`;
  }
  foods.forEach(f => {
    const [x, y] = px(f.lng, f.lat);
    s += `<circle cx="${x.toFixed(1)}" cy="${y.toFixed(1)}" r="3.6" fill="#ea580c" opacity=".85"/>`;
  });
  if (hotel.length) {
    const [x, y] = px(hotel[0].lng, hotel[0].lat);
    s += `<rect x="${(x-4.5).toFixed(1)}" y="${(y-4.5).toFixed(1)}" width="9" height="9" rx="2" fill="#7c3aed"/>`;
  }
  spots.forEach((sp, i) => {
    const [x, y] = px(sp.lng, sp.lat);
    s += `<circle cx="${x.toFixed(1)}" cy="${y.toFixed(1)}" r="9.5" fill="${sp.mv ? '#f59e0b' : '#2563eb'}"/>`;
    s += `<text x="${x.toFixed(1)}" y="${(y + 3.6).toFixed(1)}" text-anchor="middle" font-size="10" font-weight="600" fill="#fff">${i+1}</text>`;
  });
  s += `</svg>`;
  return s;
}

/* ============ 渲染行程 ============ */
function foodNear(day) {
  const spots = day.spots.filter(s => s.lat && s.lng);
  const map = {};
  (day.foods || []).forEach(f => {
    if (!f.lat || !f.lng || !spots.length) return;
    let best = null, bd = Infinity;
    spots.forEach(s => { const d = dist(f, s); if (d < bd) { bd = d; best = s; } });
    if (!best) return;
    (map[best.id] = map[best.id] || []).push({ f, d: bd });
  });
  Object.values(map).forEach(a => a.sort((x, y) => x.d - y.d));
  return map;
}

function renderItinerary() {
  let html = '';
  TRIP.days.forEach(day => {
    const fn = foodNear(day);
    const navSpots = day.spots;
    const routeHref = routeUrl(navSpots);
    html += `<div class="day" data-day="${day.id}">`;
    html += `<div class="day-hd"><span class="d-label">${day.label}</span><span class="d-sub">${esc(day.sub)}</span><span class="arrow">▶</span></div>`;
    html += `<div class="day-bd">`;
    html += `<div class="tools">`;
    html += `<button class="btn" data-map="${day.id}">展开路线示意图</button>`;
    if (routeHref) html += `<a class="btn solid" href="${routeHref}" target="_blank" rel="noopener">全天多点导航</a>`;
    html += `</div>`;
    html += `<div class="mapwrap" id="map-${day.id}">`;
    html += sketchSVG(day);
    html += `<div class="legend"><span><i style="background:#2563eb"></i>景点</span><span><i style="background:#f59e0b"></i>机动</span><span><i style="background:#ea580c"></i>美食</span><span><i style="background:#7c3aed"></i>酒店</span></div>`;
    html += `<div style="font-size:11.5px;color:#a1a1aa;padding:2px 2px 4px">示意图按经纬度等比绘制，非真实路网。点「全天多点导航」在高德内查看真实路线。</div>`;
    html += `</div>`;

    if (day.hotel) {
      html += `<div class="hotel"><div class="hb"><div class="ht">住宿 · ${esc(day.hotel.name)}</div><div class="ha">${esc(day.hotel.addr)}</div></div><a class="nav" href="${navUrl(day.hotel)}" target="_blank" rel="noopener">导航</a></div>`;
    }

    day.spots.forEach((sp, i) => {
      const foods = fn[sp.id] || [];
      html += `<div class="spot">`;
      html += `<div class="spot-top"><div class="idx${sp.mv ? ' mv' : ''}">${i+1}</div>`;
      html += `<div class="sname"><a href="${navUrl(sp)}" target="_blank" rel="noopener">${esc(sp.name)}</a>${sp.mv ? '<span class="tagmv">机动</span>' : ''}</div>`;
      html += `<a class="nav" href="${navUrl(sp)}" target="_blank" rel="noopener">导航</a></div>`;
      if (sp.hours) html += `<div class="hours">🕐 ${esc(sp.hours)}</div>`;
      if (sp.metro) html += `<div class="hours">🚇 ${esc(sp.metro)}</div>`;
      if (sp.desc) html += `<div class="desc">${esc(sp.desc)}</div>`;
      if (sp.hint) html += `<div class="hint">备注提示：${esc(sp.hint)}</div>`;
      if (sp.sub) {
        html += `<div class="sub">`;
        sp.sub.forEach(x => { html += `<div class="sub-i"><b>${esc(x.n)}</b><br><span>${esc(x.d)}</span></div>`; });
        html += `</div>`;
      }
      if (foods.length) {
        html += `<div class="foods"><div class="foods-t">附近美食</div>`;
        foods.forEach(({ f, d }) => {
          html += `<div class="food"><a href="${foodUrl(f)}" target="_blank" rel="noopener">{${esc(f.name)}}</a><span class="fd">距此约 ${fmtD(d)}</span></div>`;
        });
        html += `</div>`;
      }
      html += `</div>`;

      // 站间连接
      const next = day.spots[i + 1];
      if (next && sp.lat && next.lat) {
        const d = dist(sp, next);
        html += `<div class="link"><b>↓</b> 下一站 ${esc(next.name)}<span class="lv">约 ${fmtD(d)}（直线）</span></div>`;
      }
    });

    html += `</div></div>`;
  });
  $('#p-iti').innerHTML = html;

  // 事件
  document.querySelectorAll('#p-iti .day-hd').forEach(el => {
    el.addEventListener('click', () => el.parentElement.classList.toggle('open'));
  });
  document.querySelectorAll('#p-iti [data-map]').forEach(btn => {
    btn.addEventListener('click', () => {
      const w = document.getElementById('map-' + btn.dataset.map);
      w.classList.toggle('on');
      btn.textContent = w.classList.contains('on') ? '收起路线示意图' : '展开路线示意图';
    });
  });
}

/* ============ 备注：IndexedDB ============ */
const DBN = 'fz_trip_notes', STORE = 'notes';
let db = null;
function openDB() {
  return new Promise((res, rej) => {
    const r = indexedDB.open(DBN, 1);
    r.onupgradeneeded = e => { const d = e.target.result; if (!d.objectStoreNames.contains(STORE)) d.createObjectStore(STORE); };
    r.onsuccess = e => { db = e.target.result; res(db); };
    r.onerror = () => rej(r.error);
  });
}
function dbGet(k) {
  return new Promise(res => {
    const r = db.transaction(STORE, 'readonly').objectStore(STORE).get(k);
    r.onsuccess = () => res(r.result || null);
    r.onerror = () => res(null);
  });
}
function dbSet(k, v) {
  return new Promise(res => {
    const t = db.transaction(STORE, 'readwrite');
    t.objectStore(STORE).put(v, k);
    t.oncomplete = () => res(true);
    t.onerror = () => res(false);
  });
}
function dbAll() {
  return new Promise(res => {
    const t = db.transaction(STORE, 'readonly'), os = t.objectStore(STORE);
    const ks = os.getAllKeys(), vs = os.getAll();
    t.oncomplete = () => { const o = {}; ks.result.forEach((k, i) => o[k] = vs.result[i]); res(o); };
    t.onerror = () => res({});
  });
}
function dbClear() {
  return new Promise(res => {
    const t = db.transaction(STORE, 'readwrite');
    t.objectStore(STORE).clear();
    t.oncomplete = () => res(true);
  });
}

async function renderNotes() {
  const all = await dbAll();
  let html = `<div class="nbar"><button class="btn" id="btn-exp">导出备注</button><button class="btn" id="btn-imp">导入备注</button><input type="file" id="file-imp" accept="application/json,.json" style="display:none"></div>`;
  TRIP.days.forEach(day => {
    html += `<div class="nday" data-day="${day.id}">`;
    html += `<div class="nday-hd"><span>${day.label}</span><span class="nds">${esc(day.sub)}</span><span class="arrow">▶</span></div>`;
    html += `<div class="nday-bd">`;
    const dk = 'day:' + day.id, dv = all[dk] || {};
    html += `<div class="nblock"><div class="nlabel">📅 当天备注</div>`;
    html += `<textarea data-key="${dk}" placeholder="当天整体备注…">${esc(dv.text || '')}</textarea>`;
    html += `<div class="imgs" data-key="${dk}">${(dv.images||[]).map((src,i)=>`<div class="thumb"><img src="${src}"><i class="del" data-key="${dk}" data-i="${i}">×</i></div>`).join('')}</div>`;
    html += `<button class="addimg" data-key="${dk}">+ 添加图片</button></div>`;
    day.spots.forEach((sp, i) => {
      const k = 'spot:' + sp.id, v = all[k] || {};
      html += `<div class="nblock"><div class="nlabel"><span class="ni">${i+1}</span>${esc(sp.name)}</div>`;
      html += `<textarea data-key="${k}" placeholder="${esc(sp.hint || '写点什么…')}">${esc(v.text || '')}</textarea>`;
      html += `<div class="imgs" data-key="${k}">${(v.images||[]).map((src,j)=>`<div class="thumb"><img src="${src}"><i class="del" data-key="${k}" data-i="${j}">×</i></div>`).join('')}</div>`;
      html += `<button class="addimg" data-key="${k}">+ 添加图片</button></div>`;
    });
    html += `</div></div>`;
  });
  $('#p-not').innerHTML = html;
  bindNotes();
}

function bindNotes() {
  document.querySelectorAll('#p-not .nday-hd').forEach(el => {
    el.addEventListener('click', () => el.parentElement.classList.toggle('open'));
  });
  // 文本保存
  document.querySelectorAll('#p-not textarea').forEach(ta => {
    let timer;
    ta.addEventListener('input', () => {
      clearTimeout(timer);
      timer = setTimeout(async () => {
        const k = ta.dataset.key;
        const v = (await dbGet(k)) || {};
        v.text = ta.value;
        await dbSet(k, v);
      }, 500);
    });
  });
  // 添加图片
  document.querySelectorAll('#p-not .addimg').forEach(btn => {
    btn.addEventListener('click', () => {
      const inp = document.createElement('input');
      inp.type = 'file'; inp.accept = 'image/*'; inp.multiple = true;
      inp.onchange = async () => {
        const k = btn.dataset.key;
        const v = (await dbGet(k)) || {};
        v.images = v.images || [];
        for (const f of inp.files) {
          try { v.images.push(await compress(f)); } catch (e) {}
        }
        await dbSet(k, v);
        renderNotes();
        toast('已添加 ' + inp.files.length + ' 张图片');
      };
      inp.click();
    });
  });
  // 删除图片
  document.querySelectorAll('#p-not .thumb .del').forEach(el => {
    el.addEventListener('click', async () => {
      const k = el.dataset.key, i = +el.dataset.i;
      const v = (await dbGet(k)) || {};
      if (v.images) { v.images.splice(i, 1); await dbSet(k, v); renderNotes(); }
    });
  });
  // 导出
  $('#btn-exp').addEventListener('click', async () => {
    const all = await dbAll();
    const blob = new Blob([JSON.stringify(all, null, 2)], { type: 'application/json' });
    const a = document.createElement('a');
    a.href = URL.createObjectURL(blob);
    a.download = '福州行程备注_' + new Date().toISOString().slice(0, 10) + '.json';
    a.click();
    setTimeout(() => URL.revokeObjectURL(a.href), 3000);
    toast('已导出');
  });
  // 导入
  $('#btn-imp').addEventListener('click', () => $('#file-imp').click());
  $('#file-imp').addEventListener('change', async e => {
    const f = e.target.files[0]; if (!f) return;
    try {
      const data = JSON.parse(await f.text());
      if (typeof data !== 'object' || Array.isArray(data)) throw 0;
      for (const [k, v] of Object.entries(data)) await dbSet(k, v);
      renderNotes();
      toast('导入成功');
    } catch (err) { toast('文件格式不正确'); }
    e.target.value = '';
  });
}

function compress(file, maxW = 1280, q = 0.82) {
  return new Promise((res, rej) => {
    const rd = new FileReader();
    rd.onload = e => {
      const img = new Image();
      img.onload = () => {
        const sc = Math.min(1, maxW / img.width);
        const c = document.createElement('canvas');
        c.width = Math.round(img.width * sc);
        c.height = Math.round(img.height * sc);
        c.getContext('2d').drawImage(img, 0, 0, c.width, c.height);
        res(c.toDataURL('image/jpeg', q));
      };
      img.onerror = rej;
      img.src = e.target.result;
    };
    rd.onerror = rej;
    rd.readAsDataURL(file);
  });
}

/* ============ Tab 切换 ============ */
document.querySelectorAll('.tab').forEach(t => {
  t.addEventListener('click', () => {
    document.querySelectorAll('.tab').forEach(x => x.classList.remove('on'));
    document.querySelectorAll('.panel').forEach(x => x.classList.remove('on'));
    t.classList.add('on');
    $('#p-' + t.dataset.tab).classList.add('on');
    window.scrollTo(0, 0);
  });
});

/* ============ 启动 ============ */
(async function () {
  renderItinerary();
  try { await openDB(); await renderNotes(); }
  catch (e) { $('#p-not').innerHTML = '<div class="empty">当前浏览器不支持本地存储，备注功能不可用。<br>请用 Chrome / Safari / Edge 打开。</div>'; }
})();
</script>
</body>
</html>


name = "fuzhou-trip"
compatibility_date = "2025-01-01"

[assets]
directory = "."
not_found_handling = "single-page-application"
