# Nasarvaji.cha.raja.github.io
<!DOCTYPE html>
<html>
<head>
    <title>Mountain Group Festive Introduction</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            margin: 0;
            padding: 0;
            min-height: 100vh;
            background: linear-gradient(120deg, #ffe3e3 0%, #fffbe8 100%);
            background-image:
                url('https://www.transparenttextures.com/patterns/confetti.png'),
                radial-gradient(circle at 20% 30%, #ffd54f 0%, transparent 60%),
                radial-gradient(circle at 80% 70%, #ff7043 0%, transparent 60%),
                radial-gradient(circle at 50% 90%, #ad1457 0%, transparent 70%);
            background-blend-mode: lighten, normal;
            animation: bgmove 12s linear infinite alternate;
        }
        @keyframes bgmove {
            0% { background-position: 0 0, 0 0, 0 0, 0 0; }
            100% { background-position: 100px 100px, 40px 60px, 80px 120px, 60px 80px; }
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 0 16px;
        }
        .group-header {
            text-align: center;
            margin-top: 40px;
            color: #d84315;
            font-size: 2.7em;
            font-weight: 800;
            letter-spacing: 2px;
            text-shadow: 0 2px 12px rgba(216,67,21,0.18);
            position: relative;
            animation: fadeInDown 1.2s;
        }
        .group-header::after {
            content: "🎉";
            font-size: 1.2em;
            margin-left: 12px;
            vertical-align: middle;
            animation: bounce 1s infinite alternate;
        }
        @keyframes bounce {
            to { transform: translateY(-8px);}
        }
        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-40px);}
            to { opacity: 1; transform: translateY(0);}
        }
        .ganpati-img {
            display: block;
            margin: 32px auto 24px auto;
            border-radius: 18px;
            box-shadow: 0 4px 24px rgba(216,67,21,0.18);
            max-width: 340px;
            width: 100%;
            border: 4px solid #ffd54f;
            transition: transform 0.3s;
            animation: fadeIn 1.5s;
        }
        .ganpati-img:hover {
            transform: scale(1.06) rotate(-2deg);
            box-shadow: 0 8px 32px rgba(216,67,21,0.22);
        }
        @keyframes fadeIn {
            from { opacity: 0;}
            to { opacity: 1;}
        }
        .glimpse-section {
            margin-top: 48px;
            animation: fadeInUp 1.2s;
        }
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(40px);}
            to { opacity: 1; transform: translateY(0);}
        }
        .glimpse-title {
            font-size: 2em;
            color: #ad1457;
            text-align: center;
            margin-bottom: 24px;
            font-weight: 700;
            letter-spacing: 1px;
            position: relative;
            animation: pulse 2s infinite;
        }
        .glimpse-title::before,
        .glimpse-title::after {
            content: "✨";
            font-size: 1.2em;
            margin: 0 8px;
        }
        @keyframes pulse {
            0% { text-shadow: 0 0 0 #ffd54f;}
            50% { text-shadow: 0 0 16px #ffd54f;}
            100% { text-shadow: 0 0 0 #ffd54f;}
        }
        .glimpse-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 22px;
        }
        .glimpse-item {
            background: #fff8e1;
            border-radius: 14px;
            box-shadow: 0 2px 16px rgba(216,67,21,0.10);
            overflow: hidden;
            transition: transform 0.18s, box-shadow 0.18s;
            border: 2.5px solid #ffd54f;
            position: relative;
            animation: fadeIn 1.2s;
        }
        .glimpse-item::before {
            content: "🎊";
            position: absolute;
            top: 8px;
            left: 8px;
            font-size: 1.1em;
            opacity: 0.7;
        }
        .glimpse-item:hover {
            transform: scale(1.07) rotate(-2deg);
            box-shadow: 0 8px 32px rgba(216,67,21,0.18);
            border-color: #ff7043;
        }
        .glimpse-item img,
        .glimpse-item video {
            width: 100%;
            display: block;
            border-bottom: 1.5px solid #ffe082;
            transition: filter 0.3s;
        }
        .glimpse-item img:hover,
        .glimpse-item video:hover {
            filter: brightness(1.08) saturate(1.2);
        }
        .glimpse-caption {
            padding: 12px 10px;
            font-size: 1em;
            color: #d84315;
            text-align: center;
            font-weight: 600;
            background: linear-gradient(90deg,#fffde7 60%,#ffe0b2 100%);
            border-radius: 0 0 12px 12px;
            letter-spacing: 0.5px;
        }
        .cta-section {
            width:100%;
            text-align:center;
            margin:48px 0 32px 0;
            animation: fadeInUp 1.5s;
        }
        .cta-btn {
            display:inline-block;
            background: linear-gradient(90deg,#ffd54f 40%,#ff7043 100%);
            color: #ad1457;
            font-size: 1.35em;
            font-weight: bold;
            padding: 18px 38px;
            border-radius: 32px;
            box-shadow: 0 4px 18px rgba(216,67,21,0.13);
            text-decoration: none;
            letter-spacing: 1px;
            transition: transform 0.18s, box-shadow 0.18s;
            position: relative;
            border: none;
            cursor: pointer;
        }
        .cta-btn:hover {
            transform: scale(1.07) rotate(-2deg);
            box-shadow: 0 8px 32px rgba(216,67,21,0.18);
            background: linear-gradient(90deg,#ffd54f 10%,#ff7043 90%);
        }
        .cta-btn span {
            vertical-align: middle;
        }
        /* Floating confetti animation */
        .confetti {
            position: fixed;
            pointer-events: none;
            z-index: 9999;
            top: 0; left: 0; width: 100vw; height: 100vh;
        }
        @media (max-width: 600px) {
            .group-header { font-size: 2em; }
            .glimpse-title { font-size: 1.3em; }
            .cta-btn { font-size: 1em; padding: 12px 18px;}
        }
    </style>
</head>
<body>
    <canvas class="confetti"></canvas>
    <div class="container">
        <div class="group-header">Mountain Group</div>
        <img class="ganpati-img" src="https://images.unsplash.com/photo-1502086223501-7ea6ecd79368?auto=format&fit=crop&w=600&q=80" alt="Ganpati">
        <div style="text-align:center;margin-bottom:24px;">
            <span style="font-size:1.2em;color:#ad1457;font-weight:600;">
                Welcome to our vibrant community! <span style="font-size:1.3em;">🌄</span>
            </span>
        </div>
        <div class="glimpse-section">
            <div class="glimpse-title">Glimpse of Festive Years</div>
            <div class="glimpse-gallery">
                <div class="glimpse-item">
                    <img src="https://images.unsplash.com/photo-1519125323398-675f0ddb6308?auto=format&fit=crop&w=400&q=80" alt="Event 1">
                    <div class="glimpse-caption">Ganpati Celebration 2024 🎈</div>
                </div>
                <div class="glimpse-item">
                    <video controls muted poster="https://images.unsplash.com/photo-1465101046530-73398c7f28ca?auto=format&fit=crop&w=400&q=80">
                        <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                    <div class="glimpse-caption">Best Festive Clicks 📸</div>
                </div>
                <div class="glimpse-item">
                    <img src="https://images.unsplash.com/photo-1508672019048-805c876b67e2?auto=format&fit=crop&w=400&q=80" alt="Event 2">
                    <div class="glimpse-caption">Mountain Magic 🏔️</div>
                </div>
                <div class="glimpse-item">
                    <video controls muted poster="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=400&q=80">
                        <source src="https://www.w3schools.com/html/movie.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                    <div class="glimpse-caption">Group Singing Night 🎶</div>
                </div>
                <div class="glimpse-item">
                    <img src="https://images.unsplash.com/photo-1465101178521-c1a4c8a0b3ec?auto=format&fit=crop&w=400&q=80" alt="Event 3">
                    <div class="glimpse-caption">Picnic Fun 2020 🥳</div>
                </div>
                <div class="glimpse-item">
                    <img src="https://images.unsplash.com/photo-1500534314209-a25ddb2bd429?auto=format&fit=crop&w=400&q=80" alt="Event 4">
                    <div class="glimpse-caption">Cultural Night Extravaganza 💃</div>
                </div>
                <div class="glimpse-item">
                    <img src="https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=400&q=80" alt="Event 5">
                    <div class="glimpse-caption">Dance Performance 2022 💃</div>
                </div>
                <div class="glimpse-item">
                    <img src="https://images.unsplash.com/photo-1529626455594-4ff0802cfb7e?auto=format&fit=crop&w=400&q=80" alt="Event 6">
                    <div class="glimpse-caption">Family Gathering 2023 👨‍👩‍👧‍👦</div>
                </div>
                <div class="glimpse-item">
                    <img src="https://images.unsplash.com/photo-1519125323398-675f0ddb6308?auto=format&fit=crop&w=400&q=80" alt="Event 7">
                    <div class="glimpse-caption">Memorable Moments 🌟</div>
                </div>
            </div>
        </div>
        <div class="cta-section">
            <a href="https://docs.google.com/forms/d/e/1FAIpQLSdl2KTyULymW6zRVk4Xv-ox8Sfe1R9bea6HzHxeh9FsABjt3g/viewform?usp=header"
               target="_blank"
               class="cta-btn"
            >
                <span style="font-size:1.2em;">📝</span>
                <span style="margin:0 10px;">Fill Our Festive Feedback Form!</span>
                <span style="font-size:1.2em;">✨</span>
            </a>
        </div>
    </div>
    <script>
    // Simple confetti animation
    const canvas = document.querySelector('.confetti');
    const ctx = canvas.getContext('2d');
    let W = window.innerWidth, H = window.innerHeight;
    canvas.width = W; canvas.height = H;
    let confetti = [];
    for(let i=0;i<60;i++){
        confetti.push({
            x: Math.random()*W,
            y: Math.random()*H,
            r: Math.random()*8+4,
            d: Math.random()*W/2,
            color: ['#ffd54f','#ff7043','#ad1457','#fffbe8'][Math.floor(Math.random()*4)],
            tilt: Math.random()*10-5,
            tiltAngle: Math.random()*Math.PI*2
        });
    }
    function drawConfetti(){
        ctx.clearRect(0,0,W,H);
        confetti.forEach(c=>{
            ctx.beginPath();
            ctx.arc(c.x, c.y, c.r, 0, Math.PI*2);
            ctx.fillStyle = c.color;
            ctx.fill();
        });
        updateConfetti();
    }
    function updateConfetti(){
        confetti.forEach(c=>{
            c.y += Math.cos(c.d)+2+c.r/2;
            c.x += Math.sin(c.d);
            c.tiltAngle += 0.05;
            c.x += Math.sin(c.tiltAngle)*2;
            if(c.y > H){
                c.y = -10; c.x = Math.random()*W;
            }
        });
    }
    setInterval(drawConfetti, 33);
    window.addEventListener('resize',()=>{
        W = window.innerWidth; H = window.innerHeight;
        canvas.width = W; canvas.height = H;
    });
    </script>
</body>
</html>
