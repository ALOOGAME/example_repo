# example_repo<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>ALOOGAME HOST</title>
<style>
*{box-sizing:border-box}
body{
 margin:0;background:#080808;color:white;
 font-family:Arial,sans-serif;text-align:center
}
header{
 padding:35px 10px;
 background:linear-gradient(140deg,#430000,#090909);
 border-bottom:2px solid #f22
}
.logo{
 font-size:42px;font-weight:bold;
 color:#ff2929;text-shadow:0 0 22px red
}
h2{color:#ff3939}
main{padding:20px}
.card{
 max-width:520px;margin:15px auto;padding:20px;
 background:#171717;border:1px solid #922;
 border-radius:14px
}
select{
 width:100%;padding:14px;margin:12px 0;
 background:#222;color:white;border:1px solid #f33;
 border-radius:8px;font-size:16px
}
.status{color:#ffb347}
footer{padding:25px;color:#777}
</style>
</head>
<body>
<header>
 <div class="logo">ALOOGAME</div>
 <h2>PS4 HOST</h2>
 <p>WELCOME TO THE GAMING WORLD</p>
</header>
<main>
 <div class="card">
  <h2>FIRMWARE SELECTOR</h2>
  <p>نسخه فریمور کنسول خود را انتخاب کن:</p>
  <select id="firmware" onchange="showStatus()">
   <option value="">انتخاب فریمور</option>
  </select>
  <p id="result" class="status">منتظر انتخاب نسخه...</p>
 </div>
 <div class="card">
  <h2>ALOOGAME INFO</h2>
  <p>این سایت برای نمایش اطلاعات و سازگاری نسخه‌های PS4 ساخته شده است.</p>
  <p>وضعیت جیلبریک هر نسخه باید جداگانه تأیید شود.</p>
 </div>
</main>
<footer>© 2026 ALOOGAME HOST</footer>
<script>
const select=document.getElementById("firmware");
for(let i=1;i<=14;i++){
 for(let j=0;j<=99;j++){
  if(i===14 && j>0) break;
  let v=i+(j===0?".00":"."+String(j).padStart(2,"0"));
  let op=document.createElement("option");
  op.value=v;op.textContent="Firmware "+v;
  select.appendChild(op);
 }
}
function showStatus(){
 document.getElementById("result").textContent=
 select.value ? "اطلاعات سازگاری "+select.value+" هنوز تأیید نشده است." :
 "منتظر انتخاب نسخه...";
}
</script>
</body>
</html>
