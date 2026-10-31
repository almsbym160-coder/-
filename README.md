# -
تطبيق خاص في قطع غيار و سطحات وما يخص سيارات
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>الفزعة — كل خدمات سيارتك</title>
<style>
  :root{
    --yellow:#FFD400;
    --yellow-dark:#E6BE00;
    --dark:#141414;
    --dark2:#1E1E1E;
    --card:#252525;
    --line:#333;
    --gray:#9A9A9A;
    --danger:#E5484D;
    --radius:16px;
  }
  *{box-sizing:border-box; margin:0; padding:0; font-family:"Segoe UI", Tahoma, sans-serif;}
  body{
    background:#0A0A0A;
    display:flex; justify-content:center;
    min-height:100vh; padding:0;
  }

  .phone{
    width:100%; max-width:430px;
    background:var(--dark);
    min-height:100vh; position:relative;
    padding-bottom:90px; overflow-x:hidden;
  }

  /* ===== الهيدر ===== */
  header{
    background:linear-gradient(160deg,#1E1E1E,#141414);
    padding:18px 16px 16px;
    position:sticky; top:0; z-index:20;
    border-bottom:1px solid var(--line);
  }
  .top-row{display:flex; justify-content:space-between; align-items:center;}
  .brand{display:flex; align-items:center; gap:10px;}
  .logo{
    width:44px; height:44px; border-radius:14px;
    background:var(--yellow); display:grid; place-items:center;
    font-size:22px; box-shadow:0 6px 16px rgba(255,212,0,.25);
  }
  .brand h1{font-size:20px; color:#fff; font-weight:800;}
  .brand p{font-size:11px; color:var(--gray);}
  .bell{
    width:40px; height:40px; border-radius:12px; background:var(--card);
    display:grid; place-items:center; font-size:18px; color:#fff; cursor:pointer;
    border:1px solid var(--line);
  }

  /* ===== شريط الموقع ===== */
  .location{
    margin-top:14px; background:var(--card); border:1px solid var(--line);
    border-radius:12px; padding:10px 12px; display:flex; align-items:center; gap:10px;
    color:#fff; font-size:13px;
  }
  .location .pin{color:var(--yellow); font-size:16px;}
  .location span{flex:1; white-space:nowrap; overflow:hidden; text-overflow:ellipsis;}
  .location button{
    background:var(--yellow); border:none; padding:6px 12px; border-radius:9px;
    font-weight:700; font-size:12px; cursor:pointer; color:#111;
  }

  /* ===== البحث ===== */
  .search{
    margin-top:12px; background:var(--card); border:1px solid var(--line);
    border-radius:12px; padding:11px 14px; display:flex; align-items:center; gap:10px;
  }
  .search input{
    flex:1; background:transparent; border:none; outline:none;
    color:#fff; font-size:14px;
  }
  .search input::placeholder{color:#777;}
  .search .ic{color:var(--gray); font-size:16px;}

  /* ===== الطوارئ ===== */
  .sos{
    margin:14px 16px 0; background:linear-gradient(135deg,#E5484D,#B3161A);
    border-radius:var(--radius); padding:14px 16px; display:flex;
    align-items:center; gap:12px; cursor:pointer; box-shadow:0 8px 20px rgba(229,72,77,.25);
  }
  .sos .ic{font-size:26px;}
  .sos h3{color:#fff; font-size:15px; font-weight:800;}
  .sos p{color:#FFD9DA; font-size:11.5px;}
  .sos .arrow{margin-inline-start:auto; color:#fff; font-size:20px;}

  /* ===== العناوين ===== */
  .section-title{
    display:flex; align-items:center; justify-content:space-between;
    padding:22px 16px 12px;
  }
  .section-title h2{font-size:16px; color:#fff; font-weight:800;}
  .section-title a{color:var(--yellow); font-size:12px; text-decoration:none;}

  /* ===== شبكة الخدمات ===== */
  .grid{
    display:grid; grid-template-columns:repeat(4,1fr);
    gap:12px; padding:0 16px;
  }
  .service{
    background:var(--card); border:1px solid var(--line); border-radius:14px;
    padding:12px 4px; display:flex; flex-direction:column; align-items:center;
    gap:7px; cursor:pointer; transition:.15s; text-align:center;
  }
  .service:active{transform:scale(.95); background:#2F2F2F;}
  .service .ic{font-size:24px;}
  .service span{font-size:10.5px; color:#ddd; line-height:1.25;}

  /* خدمة مميزة (صفراء) */
