<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Anniversary Teena ❤️</title>

<style>
body{
    margin:0;
    font-family:'Segoe UI', sans-serif;
    background:linear-gradient(135deg,#ff5f9e,#ffc371);
    color:white;
    text-align:center;
    overflow:hidden;
}

/* FLOATING HEARTS */
.heart-float{
    position:fixed;
    bottom:-50px;
    font-size:24px;
    animation:floatUp 8s linear infinite;
    opacity:0.8;
}
@keyframes floatUp{
    0%{transform:translateY(0); opacity:0;}
    20%{opacity:1;}
    100%{transform:translateY(-120vh); opacity:0;}
}

/* PAGES */
.page{
    display:none;
    max-width:650px;
    margin:70px auto;
    padding:40px;
    background:rgba(255,255,255,0.18);
    border-radius:25px;
    animation:fadeSlide 0.8s ease;
}
.active{ display:block; }

@keyframes fadeSlide{
    from{opacity:0; transform:translateY(30px);}
    to{opacity:1; transform:translateY(0);}
}

/* HEARTS */
.heart{ font-size:70px; animation:beat 1s infinite; }
.bigheart{ font-size:100px; animation:beat 1.2s infinite; }
@keyframes beat{
    0%,100%{transform:scale(1);}
    50%{transform:scale(1.25);}
}

/* BUTTON */
button{
    margin-top:30px;
    padding:16px 38px;
    font-size:18px;
    background:white;
    color:#ff5f9e;
    border:none;
    border-radius:30px;
    font-weight:bold;
    cursor:pointer;
    animation:pulse 1.6s infinite;
}
@keyframes pulse{
    0%{box-shadow:0 0 0 0 rgba(255,255,255,0.6);}
    70%{box-shadow:0 0 0 20px rgba(255,255,255,0);}
    100%{box-shadow:0 0 0 0 rgba(255,255,255,0);}
}

.emojis{ font-size:26px; }
</style>

<script>
let musicStarted=false;

/* PAGE SWITCH */
function showPage(id){
    ["page1","page2","page3","page4"].forEach(p=>{
        document.getElementById(p).classList.remove("active");
    });
    document.getElementById(id).classList.add("active");

    if(!musicStarted){
        document.getElementById("bgMusic").volume=0.4;
        document.getElementById("bgMusic").play();
        musicStarted=true;
    }
}

/* FLOATING HEARTS */
setInterval(()=>{
    const h=document.createElement("div");
    h.className="heart-float";
    h.innerHTML=["❤️","💖","💘","💕","😍","🥰"][Math.floor(Math.random()*6)];
    h.style.left=Math.random()*100+"vw";
    h.style.animationDuration=(6+Math.random()*4)+"s";
    document.body.appendChild(h);
    setTimeout(()=>h.remove(),10000);
},700);
</script>
</head>

<body>

<!-- MUSIC -->
<audio id="bgMusic" loop>
  <source src="https://cdn.pixabay.com/audio/2022/10/30/audio_0f8b3b31c7.mp3" type="audio/mpeg">
</audio>

<!-- PAGE 1 -->
<div id="page1" class="page active">
    <div class="heart">❤️</div>
    <h1>Happy 3 Months Anniversary 🎉💖</h1>
    <h2>Teena Soni 🥰🌸</h2>

    <p class="emojis">
        A little surprise made with love 💝✨<br>
        Tap continue 💕👇
    </p>

    <button onclick="showPage('page2')">Continue 💖➡️</button>
</div>

<!-- PAGE 2 -->
<div id="page2" class="page">
    <h1>🌹 Shayari For You 🌹</h1>

    <p>
        Teena 😘 tum saath ho toh har pal khoobsurat lagta hai 💫<br>
        Tumhari muskaan meri sabse badi taqat hai 😍<br><br>
        Teen mahine sirf ek shuruaat hai jaan 💕<br>
        Tumhare saath har din jannat lagta hai ❤️
    </p>

    <button onclick="showPage('page3')">Next 💝➡️</button>
</div>

<!-- PAGE 3 -->
<div id="page3" class="page">
    <div class="bigheart">❤️💖</div>
    <h1>My Promise To You 💍✨</h1>

    <p>
        Teena Soni 🥰❤️<br><br>
        I promise to respect you 🙏<br>
        support you 🤝<br>
        and stay by your side always ♾️💞
    </p>

    <button onclick="showPage('page4')">Secret Page 🔐💌</button>
</div>

<!-- PAGE 4 (SECRET MESSAGE) -->
<div id="page4" class="page">
    <div class="bigheart">💖💫</div>
    <h1>🔐 Secret Message 🔐</h1>

    <p>
        Teena ❤️<br><br>
        You are not just part of my life,<br>
        you are the reason my life smiles 😊✨<br><br>

        In every chaos 🌪️ and calm 🌈,<br>
        I choose you — again & again ♾️💖<br><br>

        Thank you for these beautiful 3 months 💕<br>
        And many more to come 🌸🥰
    </p>

    <h2>I Love You 😘❤️</h2>
</div>

</body>
</html>
