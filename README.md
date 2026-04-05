<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<title>النظام المالي</title>
<style>
body{font-family:Arial;background:#f5f7fb;margin:0;padding:20px}
.card{background:white;padding:20px;border-radius:10px;margin-bottom:15px}
h1{color:#1e3a8a}
</style>
</head>

<body>

<h1>مدارس الملك عبدالعزيز النموذجية</h1>

<div class="card">
<h3>اختر الشهر</h3>
<select id="month" onchange="loadData()">
<option value="01">يناير</option>
<option value="02">فبراير</option>
<option value="03">مارس</option>
<option value="04">أبريل</option>
</select>
</div>

<div class="card">
<h3>الإيرادات</h3>
<p id="income"></p>
</div>

<div class="card">
<h3>المصروفات</h3>
<p id="expense"></p>
</div>

<script>

const DATA = {
"01": {income: 120000, expense: 50000},
"02": {income: 150000, expense: 70000},
"03": {income: 180000, expense: 90000},
"04": {income: 200000, expense: 110000}
};

function loadData(){
let m = document.getElementById("month").value;
document.getElementById("income").innerText = DATA[m].income + " ريال";
document.getElementById("expense").innerText = DATA[m].expense + " ريال";
}

loadData();

</script>

</body>
</html>
