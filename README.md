<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bài giảng Địa lí – Tự nhiên</title>

<style>
body{
    font-family: Arial, sans-serif;
    margin:0;
    background:#0f172a;
    color:#e5e7eb;
}
header{
    background:#020617;
    padding:10px;
    text-align:center;
    font-weight:bold;
}
nav{
    display:flex;
    gap:8px;
    padding:10px;
    overflow-x:auto;
    background:#020617;
}
nav button{
    flex:0 0 auto;
    padding:8px 12px;
    border:none;
    border-radius:6px;
    background:#1e293b;
    color:white;
    font-size:14px;
}
nav button.active{
    background:#38bdf8;
    color:black;
}
section{
    display:none;
    padding:15px;
}
section.active{
    display:block;
}
.box{
    background:#1e293b;
    padding:15px;
    border-radius:10px;
    margin-bottom:15px;
}
.orbit{
    width:200px;
    height:200px;
    border:1px dashed #64748b;
    border-radius:50%;
    position:relative;
    margin:auto;
}
.sun{
    width:30px;
    height:30px;
    background:gold;
    border-radius:50%;
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
}
.earth{
    width:14px;
    height:14px;
    background:#38bdf8;
    border-radius:50%;
    position:absolute;
    top:-7px;
    left:50%;
    transform:translateX(-50%);
}
.globe{
    width:180px;
    height:180px;
    border-radius:50%;
    background:radial-gradient(circle at 30% 30%,#38bdf8,#1e3a8a);
    margin:auto;
    position:relative;
}
.axis{
    position:absolute;
    top:-20px;
    bottom:-20px;
    left:50%;
    width:2px;
    background:white;
    transform:rotate(-23.5deg);
}
.wave{
    height:20px;
    background:linear-gradient(90deg,#38bdf8,#0ea5e9);
    border-radius:10px;
    animation:wave 2s infinite linear;
}
@keyframes wave{
    0%{transform:translateX(0)}
    100%{transform:translateX(-50px)}
}
</style>
</head>

<body>

<header>BÀI GIẢNG ĐỊA LÍ – TỰ NHIÊN</header>

<nav>
<button onclick="show(0)" class="active">Trái Đất quanh Mặt Trời</button>
<button onclick="show(1)">Trái Đất tự quay</button>
<button onclick="show(2)">Núi lửa</button>
<button onclick="show(3)">Sóng biển</button>
<button onclick="show(4)">Thủy triều</button>
</nav>

<section class="active">
<div class="box">
<h3>Trái Đất chuyển động quanh Mặt Trời</h3>
<div class="orbit" id="orbit">
<div class="sun"></div>
<div class="earth" id="earth"></div>
</div>
<p
