<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Akash K N - Digital Business Card</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap');

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Inter', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: #fff;
        }

        /* Card Container */
        .card-container {
            width: 350px;
            height: 500px;
            perspective: 1000px;
            cursor: pointer;
        }

        /* Flip Animation */
        .card-inner {
            width: 100%;
            height: 100%;
            position: relative;
            transition: transform 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            transform-style: preserve-3d;
        }

        .card-container:hover .card-inner {
            transform: rotateY(180deg);
        }

        /* Front and Back Shared Styles */
        .card-front, .card-back {
            width: 100%;
            height: 100%;
            position: absolute;
            backface-visibility: hidden;
            border-radius: 20px;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 30px 20px;
            overflow: hidden;
        }

        /* --- FRONT OF CARD --- */
        .profile-img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 3px solid #3b82f6;
            margin-bottom: 20px;
            object-fit: cover;
            box-shadow: 0 0 20px rgba(59, 130, 246, 0.5);
        }

        .name {
            font-size: 24px;
            font-weight: 800;
            margin-bottom: 5px;
            background: linear-gradient(90deg, #60a5fa, #a78bfa);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .title {
            font-size: 14px;
            color: #cbd5e1;
            margin-bottom: 20px;
            text-align: center;
        }

        .badges {
            display: flex;
            gap: 10px;
            margin-bottom: 25px;
        }

        .badge {
            background: rgba(59, 130, 246, 0.2);
            color: #60a5fa;
            padding: 5px 10px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 600;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: auto;
        }

        .social-links a {
            color: #fff;
            text-decoration: none;
            padding: 10px 15px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            transition: 0.3s;
            font-size: 14px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .social-links a:hover {
            background: #3b82f6;
            transform: translateY(-3px);
        }

        .hint {
            font-size: 11px;
            color: #94a3b8;
            margin-top: 20px;
            opacity: 0.7;
        }

        /* --- BACK OF CARD --- */
        .card-back {
            transform: rotateY(180deg);
            align-items: flex-start;
            justify-content: center;
        }

        .section-title {
            font-size: 18px;
            font-weight: 600;
            color: #a78bfa;
            margin-bottom: 15px;
            width: 100%;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            padding-bottom: 5px;
        }

        .skills-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 25px;
        }

        .skill-tag {
            background: rgba(255, 255, 255, 0.1);
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 12px;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .stats {
            width: 100%;
            margin-bottom: 20px;
        }

        .stat-item {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
            font-size: 13px;
            color: #cbd5e1;
        }

        .stat-item span {
            color: #4ade80;
            font-weight: bold;
            margin-right: 8px;
        }

        .btn-hire {
            width: 100%;
            padding: 12px;
            background: linear-gradient(90deg, #3b82f6, #8b5cf6);
            color: white;
            border: none;
            border-radius: 10px;
            font-weight: 600;
            cursor: pointer;
            text-align: center;
            text-decoration: none;
            transition: 0.3s;
        }

        .btn-hire:hover {
            box-shadow: 0 0 15px rgba(139, 92, 246, 0.5);
        }
    </style>
</head>
<body>

    <div class="card-container">
        <div class="card-inner">
            
            <div class="card-front">
                <img src="https://github.com/vhghgfdhgfjhg.png" alt="Akash K N" class="profile-img">
                <h1 class="name">Akash K N</h1>
                <p class="title">Frontend / MERN Stack Developer</p>
                
                <div class="badges">
                    <span class="badge">React.js</span>
                    <span class="badge">Next.js</span>
                    <span class="badge">UI/UX</span>
                </div>

                <div class="social-links">
                    <a href="https://akashknportfolio.netlify.app/" target="_blank">🌐 Portfolio</a>
                    <a href="https://linkedin.com/in/akash-k-n-6b4212282" target="_blank">in LinkedIn</a>
                    <a href="https://github.com/vhghgfdhgfjhg" target="_blank">💻 GitHub</a>
                </div>
                
                <p class="hint">Hover or tap to view details ⤵</p>
            </div>

            <div class="card-back">
                <h2 class="section-title">Top Skills</h2>
                <div class="skills-grid">
                    <span class="skill-tag">JavaScript</span>
                    <span class="skill-tag">TypeScript</span>
                    <span class="skill-tag">React</span>
                    <span class="skill-tag">Node.js</span>
                    <span class="skill-tag">TailwindCSS</span>
                    <span class="skill-tag">MongoDB</span>
                </div>

                <h2 class="section-title">Highlights</h2>
                <div class="stats">
                    <div class="stat-item"><span>🚀</span> 95+ Lighthouse Scores</div>
                    <div class="stat-item"><span>⚡</span> 60% App Performance Boost</div>
                    <div class="stat-item"><span>🏆</span> Open to Immediate Joining</div>
                </div>

                <a href="mailto:akashkn5140@gmail.com" class="btn-hire">Contact Me</a>
            </div>

        </div>
    </div>

</body>
</html>
