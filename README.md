<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FallingMeteorite - GitHub Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            color: #e2e8f0;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 30px 0;
            border-bottom: 1px solid #334155;
            margin-bottom: 40px;
        }
        
        .welcome {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .welcome h1 {
            font-size: 2.5rem;
            background: linear-gradient(90deg, #60a5fa, #a78bfa);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 700;
        }
        
        .welcome-icon {
            font-size: 2.8rem;
            animation: wave 2s infinite;
        }
        
        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            10%, 30% { transform: rotate(14deg); }
            20% { transform: rotate(-8deg); }
            40% { transform: rotate(-4deg); }
        }
        
        .profile-img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 4px solid #60a5fa;
            box-shadow: 0 0 20px rgba(96, 165, 250, 0.5);
            background: linear-gradient(45deg, #1e293b, #334155);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: #60a5fa;
        }
        
        .content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .card {
            background: rgba(30, 41, 59, 0.7);
            border-radius: 16px;
            padding: 25px;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid #334155;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.4);
        }
        
        .card h2 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #60a5fa;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .card h2 i {
            font-size: 1.3rem;
        }
        
        .about-text {
            margin-bottom: 20px;
            color: #cbd5e1;
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }
        
        .skill {
            background: linear-gradient(90deg, #3b82f6, #6366f1);
            color: white;
            padding: 6px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 500;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 15px;
            padding: 10px;
            border-radius: 8px;
            transition: background 0.3s ease;
        }
        
        .contact-item:hover {
            background: rgba(51, 65, 85, 0.5);
        }
        
        .contact-item i {
            width: 20px;
            color: #60a5fa;
        }
        
        .stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-top: 20px;
        }
        
        .stat-item {
            text-align: center;
            padding: 15px;
            background: rgba(30, 41, 59, 0.8);
            border-radius: 12px;
            transition: transform 0.3s ease;
        }
        
        .stat-item:hover {
            transform: scale(1.05);
        }
        
        .stat-value {
            font-size: 1.8rem;
            font-weight: 700;
            color: #60a5fa;
            margin-bottom: 5px;
        }
        
        .stat-label {
            font-size: 0.9rem;
            color: #94a3b8;
        }
        
        .repo-card {
            grid-column: 1 / -1;
            display: flex;
            flex-direction: column;
        }
        
        .repo-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .repo-title {
            font-size: 1.3rem;
            color: #60a5fa;
        }
        
        .repo-stats {
            display: flex;
            gap: 15px;
            color: #94a3b8;
            font-size: 0.9rem;
        }
        
        .repo-desc {
            color: #cbd5e1;
            margin-bottom: 15px;
        }
        
        .repo-topics {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 10px;
        }
        
        .topic {
            background: rgba(96, 165, 250, 0.2);
            color: #60a5fa;
            padding: 4px 12px;
            border-radius: 12px;
            font-size: 0.8rem;
        }
        
        .activity-graph {
            grid-column: 1 / -1;
            padding: 20px;
            text-align: center;
        }
        
        .activity-graph img {
            max-width: 100%;
            border-radius: 12px;
        }
        
        footer {
            text-align: center;
            padding: 30px 0;
            color: #94a3b8;
            font-size: 0.9rem;
            border-top: 1px solid #334155;
            margin-top: 40px;
        }
        
        @media (max-width: 768px) {
            .content {
                grid-template-columns: 1fr;
            }
            
            header {
                flex-direction: column;
                gap: 20px;
                text-align: center;
            }
            
            .welcome {
                flex-direction: column;
            }
            
            .stats {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="welcome">
                <span class="welcome-icon">👋</span>
                <h1>Hello, I'm FallingMeteorite</h1>
            </div>
            <div class="profile-img">
                <i class="fas fa-user-astronaut"></i>
            </div>
        </header>
        
        <div class="content">
            <div class="card">
                <h2><i class="fas fa-user"></i> About Me</h2>
                <p class="about-text">
                    A passionate developer who loves coding and exploring new technologies. 
                    I enjoy solving complex problems and creating efficient solutions. 
                    When I'm not coding, you can find me enjoying life and maintaining a good work-life balance.
                </p>
                
                <h2><i class="fas fa-code"></i> Main Technologies</h2>
                <div class="skills">
                    <span class="skill">Python</span>
                    <span class="skill">C</span>
                    <span class="skill">Git</span>
                    <span class="skill">Linux</span>
                    <span class="skill">JavaScript</span>
                    <span class="skill">HTML/CSS</span>
                </div>
            </div>
            
            <div class="card">
                <h2><i class="fas fa-envelope"></i> Contact</h2>
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span>2327667836@qq.com</span>
                </div>
                
                <div class="contact-item">
                    <i class="fab fa-github"></i>
                    <span>github.com/fallingmeteorite</span>
                </div>
                
                <h2><i class="fas fa-language"></i> Languages</h2>
                <div class="contact-item">
                    <i class="fas fa-globe"></i>
                    <span>English, 中文</span>
                </div>
                
                <div class="stats">
                    <div class="stat-item">
                        <div class="stat-value">2+</div>
                        <div class="stat-label">Years Coding</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value">15+</div>
                        <div class="stat-label">Projects</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value">500+</div>
                        <div class="stat-label">Commits</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value">10+</div>
                        <div class="stat-label">Repositories</div>
                    </div>
                </div>
            </div>
            
            <div class="card repo-card">
                <div class="repo-header">
                    <h3 class="repo-title">Wraith Toolbox</h3>
                    <div class="repo-stats">
                        <span><i class="fas fa-star"></i> 24</span>
                        <span><i class="fas fa-code-branch"></i> 8</span>
                    </div>
                </div>
                <p class="repo-desc">
                    A powerful toolbox application for developers with various utilities and tools to streamline workflow and increase productivity.
                </p>
                <div class="repo-topics">
                    <span class="topic">python</span>
                    <span class="topic">toolbox</span>
                    <span class="topic">productivity</span>
                    <span class="topic">utilities</span>
                </div>
            </div>
            
            <div class="card activity-graph">
                <h2><i class="fas fa-chart-line"></i> GitHub Activity</h2>
                <p>My contribution graph shows my coding activity and consistency over time.</p>
                <!-- In a real implementation, you would embed your GitHub activity graph here -->
                <div style="background: #1e293b; height: 200px; border-radius: 12px; display: flex; align-items: center; justify-content: center; margin-top: 20px;">
                    <p>GitHub Activity Graph Would Appear Here</p>
                </div>
            </div>
        </div>
        
        <footer>
            <p>Made with ❤️ by FallingMeteorite | Last updated: 2023</p>
        </footer>
    </div>

    <script>
        // Simple animation for stats counter
        document.addEventListener('DOMContentLoaded', function() {
            const statValues = document.querySelectorAll('.stat-value');
            
            statValues.forEach(stat => {
                const target = parseInt(stat.textContent);
                let current = 0;
                const increment = target / 50;
                const timer = setInterval(() => {
                    current += increment;
                    if (current >= target) {
                        stat.textContent = target + '+';
                        clearInterval(timer);
                    } else {
                        stat.textContent = Math.floor(current) + '+';
                    }
                }, 30);
            });
        });
    </script>
</body>
</html>
