<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Приглашение на свадьбу</title>

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes:wght@400;600&family=Poppins:wght@300;400&display=swap" rel="stylesheet">

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
font-family:Montserrat,sans-serif;
background:#f8f5f2;
color:#4a4a4a;
overflow-x:hidden;
}

.hero{
height:100vh;
display:flex;
align-items:center;
justify-content:center;
flex-direction:column;
text-align:center;
background:linear-gradient(rgba(255,255,255,.45),rgba(255,255,255,.45)),
url("https://images.unsplash.com/photo-1511285560929-80b456fea0bc?auto=format&fit=crop&w=1400&q=80");
background-size:cover;
background-position:center;
}

h1{
font-family:"Cormorant Garamond",serif;
font-size:70px;
font-weight:600;
}

h2{
font-family:"Cormorant Garamond",serif;
font-size:34px;
margin:20px 0;
}

p{
font-size:18px;
line-height:1.8;
}

.section{
max-width:900px;
margin:auto;
padding:80px 25px;
text-align:center;
}

.date{
font-size:42px;
margin:30px 0;
font-family:"Cormorant Garamond",serif;
}

.timer{
display:flex;
justify-content:center;
gap:25px;
margin-top:35px;
}

.block{
background:white;
padding:20px;
border-radius:15px;
min-width:90px;
box-shadow:0 8px 25px rgba(0,0,0,.08);
}

.block span{
display:block;
font-size:34px;
font-weight:bold;
}

.button{
display:inline-block;
margin-top:35px;
padding:16px 35px;
background:#c8a97e;
color:white;
text-decoration:none;
border-radius:40px;
transition:.3s;
}

.button:hover{
transform:scale(1.05);
}

footer{
padding:60px;
text-align:center;
font-size:15px;
color:#888;
}

@media(max-width:700px){

h1{
font-size:46px;
}

.timer{
flex-wrap:wrap;
}

}
</style>
</head>

<body>

<section class="hero">

<p>Приглашение на свадьбу</p>

<h1>Кир<br>&<br>Эва</h1>

<h2>Мы скажем друг другу «Да»</h2>

<div class="date">
25 июля 2026
</div>

<a class="button" href="#invite">
Открыть приглашение
</a>

</section>

<section class="section" id="invite">

<h2>Дорогие родные и друзья!</h2>

<p>

Мы счастливы пригласить вас разделить
самый важный день нашей жизни.

Будем рады видеть вас на нашей свадебной церемонии.

</p>

</section>

<section class="section">

<h2>Когда</h2>

<p>
25 июля 2026<br>
Начало в 14:00
</p>

</section>

<section class="section">

<h2>Где</h2>

<p>

Загс<br>

г. Переславль-Залесский

</p>

<a class="button"
href="https://yandex.ru/maps/-/CTQ3N4kr"
target="_blank">

Показать на карте

</a>

</section>

<section class="section">

<h2>До нашей встречи осталось</h2>

<div class="timer">

<div class="block">
<span id="days"></span>
Дней
</div>

<div class="block">
<span id="hours"></span>
Часов
</div>

<div class="block">
<span id="minutes"></span>
Минут
</div>

<div class="block">
<span id="seconds"></span>
Секунд
</div>

</div>

</section>

<section class="section">

<h2>Подтвердите присутствие</h2>

<p>
Будем благодарны за ответ до 1 июля.
</p>

<a class="button"
href="https://forms.google.com">

Ответить

</a>

</section>

<footer>

С любовью ❤️<br>

Кир и Эва

</footer>

<script>

const weddingDate = new Date("Jul 25, 2026 14:00:00").getTime();

setInterval(()=>{

const now=new Date().getTime();

const distance=weddingDate-now;

document.getElementById("days").innerHTML=Math.floor(distance/(1000*60*60*24));

document.getElementById("hours").innerHTML=Math.floor((distance%(1000*60*60*24))/(1000*60*60));

document.getElementById("minutes").innerHTML=Math.floor((distance%(1000*60*60))/(1000*60));

document.getElementById("seconds").innerHTML=Math.floor((distance%(1000*60))/1000);

},1000);

</script>

</body>
</html>
