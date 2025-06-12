<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Twizter - GitHub Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #0d1117 0%, #161b22 100%);
            color: #e6edf3;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Noto Sans', Helvetica, Arial, sans-serif;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header Section */
        .header {
            text-align: center;
            padding: 40px 0;
            position: relative;
        }

        .visitor-badge {
            position: absolute;
            top: 20px;
            right: 20px;
        }

        .typing-title {
            font-size: 3rem;
            font-weight: bold;
            background: linear-gradient(135deg, #58a6ff, #39d353);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 20px;
            animation: glow 2s ease-in-out infinite alternate;
        }

        .subtitle {
            font-size: 1.5rem;
            color: #7c3aed;
            margin-bottom: 40px;
        }

        @keyframes glow {
            from { filter: drop-shadow(0 0 5px rgba(88, 166, 255, 0.5)); }
            to { filter: drop-shadow(0 0 20px rgba(88, 166, 255, 0.8)); }
        }

        /* About Section */
        .about-section {
            background: linear-gradient(135deg, #21262d, #161b22);
            border: 1px solid #30363d;
            border-radius: 16px;
            padding: 40px;
            margin: 40px 0;
            text-align: center;
        }

        .about-section h2 {
            color: #58a6ff;
            margin-bottom: 30px;
            font-size: 2rem;
        }

        .about-content {
            font-size: 1.1rem;
            line-height: 2;
        }

        .about-content a {
            color: #58a6ff;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .about-content a:hover {
            color: #39d353;
        }

        /* Skills Section */
        .skills-section {
            text-align: center;
            margin: 60px 0;
        }

        .skills-section h2 {
            color: #58a6ff;
            margin-bottom: 30px;
            font-size: 2rem;
        }

        .skills-icons {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 30px;
        }

        .skill-icon {
            width: 60px;
            height: 60px;
            border-radius: 12px;
            transition: all 0.3s ease;
            filter: grayscale(0.3);
        }

        .skill-icon:hover {
            transform: translateY(-10px) scale(1.1);
            filter: grayscale(0);
            box-shadow: 0 10px 25px rgba(88, 166, 255, 0.3);
        }

        /* 3D Charts Section */
        .charts-section {
            margin: 80px 0;
        }

        .charts-header {
            text-align: center;
            margin-bottom: 50px;
        }

        .charts-header h2 {
            color: #58a6ff;
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .charts-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            margin-bottom: 40px;
        }

        .chart-container {
            background: linear-gradient(135deg, #21262d, #161b22);
            border: 1px solid #30363d;
            border-radius: 16px;
            padding: 30px;
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .chart-container:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
        }

        .chart-container h3 {
            color: #39d353;
            margin-bottom: 25px;
            font-size: 1.5rem;
        }

        .chart-3d, .chart-radar {
            border: 2px solid #30363d;
            border-radius: 12px;
            background: #0d1117;
            margin: 0 auto;
        }

        .chart-controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
        }

        .control-btn {
            background: linear-gradient(135deg, #238636, #1f6f2a);
            border: none;
            color: white;
            padding: 10px 20px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 0.9rem;
            transition: all 0.3s ease;
        }

        .control-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(35, 134, 54, 0.4);
        }

        /* Setup Guide */
        .setup-guide {
            background: linear-gradient(135deg, #21262d, #0d1117);
            border: 1px solid #30363d;
            border-radius: 12px;
            margin: 30px 0;
            overflow: hidden;
        }

        .setup-toggle {
            background: transparent;
            border: none;
            color: #58a6ff;
            width: 100%;
            padding: 20px;
            text-align: left;
            cursor: pointer;
            font-size: 1.1rem;
            font-weight: bold;
            transition: background 0.3s ease;
        }

        .setup-toggle:hover {
            background: rgba(88, 166, 255, 0.1);
        }

        .setup-content {
            display: none;
            padding: 0 20px 20px;
        }

        .setup-content.active {
            display: block;
        }

        .code-block {
            background: #0d1117;
            border: 1px solid #30363d;
            border-radius: 8px;
            padding: 20px;
            font-family: 'Courier New', monospace;
            font-size: 0.9rem;
            overflow-x: auto;
            white-space: pre-wrap;
            color: #39d353;
        }

        /* Snake Animation Section */
        .snake-section {
            text-align: center;
            margin: 80px 0;
            padding: 40px 0;
            border-top: 1px solid #30363d;
            border-bottom: 1px solid #30363d;
        }

        .snake-section h2 {
            color: #58a6ff;
            margin-bottom: 30px;
            font-size: 2rem;
        }

        .snake-animation {
            max-width: 100%;
            border-radius: 12px;
        }

        /* Stats Section */
        .stats-section {
            margin: 80px 0;
        }

        .stats-header {
            text-align: center;
            margin-bottom: 40px;
        }

        .stats-header h2 {
            color: #58a6ff;
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .stat-card {
            background: linear-gradient(135deg, #21262d, #161b22);
            border: 1px solid #30363d;
            border-radius: 12px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
        }

        .stat-card img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* Activity Section */
        .activity-section {
            margin: 80px 0;
            text-align: center;
        }

        .activity-section h2 {
            color: #58a6ff;
            margin-bottom: 40px;
            font-size: 2rem;
        }

        .activity-graph {
            width: 100%;
            border-radius: 12px;
            margin-bottom: 40px;
        }

        .summary-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        /* Trophies Section */
        .trophies-section {
            text-align: center;
            margin: 80px 0;
            padding: 40px 0;
            border-top: 1px solid #30363d;
            border-bottom: 1px solid #30363d;
        }

        .trophies-section h2 {
            color: #58a6ff;
            margin-bottom: 30px;
            font-size: 2rem;
        }

        /* Languages Pie Chart */
        .languages-section {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 40px;
            margin: 40px 0;
            flex-wrap: wrap;
        }

        .pie-container {
            position: relative;
        }

        .legend {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 1rem;
        }

        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 4px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }

        /* Connect Section */
        .connect-section {
            text-align: center;
            margin: 80px 0;
        }

        .connect-section h2 {
            color: #58a6ff;
            margin-bottom: 30px;
            font-size: 2rem;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .social-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: linear-gradient(135deg, #238636, #1f6f2a);
            color: white;
            text-decoration: none;
            padding: 12px 24px;
            border-radius: 8px;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .social-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(35, 134, 54, 0.4);
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 40px 0;
            border-top: 1px solid #30363d;
            margin-top: 80px;
        }

        .footer-wave {
            width: 100%;
            height: 100px;
            background: linear-gradient(135deg, #58a6ff, #39d353);
            border-radius: 50px 50px 0 0;
            margin-bottom: 20px;
        }

        .footer-text {
            color: #8b949e;
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .charts-grid {
                grid-template-columns: 1fr;
            }
            
            .typing-title {
                font-size: 2rem;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            .languages-section {
                flex-direction: column;
            }
            
            .social-links {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <div class="visitor-badge">
                <img src="https://visitor-badge.laobi.icu/badge?page_id=Twizter01.Twizter01" alt="visitor badge" />
            </div>
            <h1 class="typing-title">Hey, I'm Twizter! 👋</h1>
            <h3 class="subtitle">A passionate software developer from Colombia</h3>
        </div>

        <!-- About Section -->
        <div class="about-section">
            <h2>🌟 A little About Me</h2>
            <div class="about-content">
                🔭 I'm currently working as a Sales Executive.<br/>
                🌱 I'm currently learning Data Science and Systems Engineering.<br/>
                🎨 I'm a CSS Lover.<br/>
                👯 I'm looking to collaborate on front-end or back-end projects. My focus is to build profitable and scalable solutions.<br/>
                📫 How to reach me: <a href="https://www.linkedin.com/in/gabriel-jimenez-a28b73316" target="_blank">LinkedIn</a><br/>
                😄 Pronouns: He/Him.<br/>
                🚀 I'm a first-year Computer Science student who absolutely adores nature.<br/>
            </div>
        </div>

        <!-- Skills Section -->
        <div class="skills-section">
            <h2>⚒️ Languages - Frameworks - Tools ⚒️</h2>
            <div class="skills-icons">
                <img class="skill-icon" src="https://skillicons.dev/icons?i=html" alt="HTML" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=css" alt="CSS" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=javascript" alt="JavaScript" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=typescript" alt="TypeScript" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=cpp" alt="C++" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=python" alt="Python" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=bash" alt="Bash" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=react" alt="React" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=tailwind" alt="Tailwind" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=nodejs" alt="Node.js" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=django" alt="Django" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=firebase" alt="Firebase" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=mongodb" alt="MongoDB" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=sqlite" alt="SQLite" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=vscode" alt="VSCode" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=git" alt="Git" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=github" alt="GitHub" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=linux" alt="Linux" />
                <img class="skill-icon" src="https://skillicons.dev/icons?i=figma" alt="Figma" />
            </div>
        </div>

        <!-- 3D Charts Section -->
        <div class="charts-section">
            <div class="charts-header">
                <h2>🎯 3D Contributions & Developer Radar</h2>
            </div>
            
            <div class="charts-grid">
                <div class="chart-container">
                    <h3>📊 3D Contribution Graph</h3>
                    <canvas id="contributions3d" class="chart-3d" width="500" height="350"></canvas>
                    <div class="chart-controls">
                        <button class="control-btn" onclick="rotateLeft()">← Rotate</button>
                        <button class="control-btn" onclick="resetView()">Reset View</button>
                        <button class="control-btn" onclick="rotateRight()">Rotate →</button>
                    </div>
                </div>

                <div class="chart-container">
                    <h3>🎯 Developer Skills Radar</h3>
                    <canvas id="radarChart" class="chart-radar" width="350" height="350"></canvas>
                </div>
            </div>

            <!-- Languages Pie Chart -->
            <div class="languages-section">
                <div class="pie-container">
                    <canvas id="languagesPie" width="200" height="200"></canvas>
                </div>
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background: #3178c6;"></div>
                        <span>TypeScript</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background: #3776ab;"></div>
                        <span>Python</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background: #ff69b4;"></div>
                        <span>SCSS</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background: #e34c26;"></div>
                        <span>HTML</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background: #239120;"></div>
                        <span>C#</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background: #555555;"></div>
                        <span>Other</span>
                    </div>
                </div>
            </div>

            <!-- Setup Guide -->
            <div class="setup-guide">
                <button class="setup-toggle" onclick="toggleSetup()">
                    🔧 Generate Your Own 3D Contributions
                </button>
                <div class="setup-content" id="setupContent">
                    <p>To generate your own 3D contributions chart, add this GitHub Action to your profile repository:</p>
                    <div class="code-block"># .github/workflows/profile-3d.yml
name: GitHub-Profile-3D-Contrib

on:
  schedule: # 03:00 JST == 18:00 UTC
    - cron: "0 18 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    name: generate-github-profile-3d-contrib
    steps:
      - uses: actions/checkout@v3
      - uses: yoshi389111/github-profile-3d-contrib@0.7.1
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          USERNAME: ${{ github.repository_owner }}
      - name: Commit & Push
        run: |
          git config user.name github-actions
          git config user.email github-actions@github.com
          git add .
          git commit -m "generated"
          git push</div>
                </div>
            </div>
        </div>

        <!-- Snake Animation Section -->
        <div class="snake-section">
            <h2>🐍 My Contributions 🐍</h2>
            <img class="snake-animation" src="https://raw.githubusercontent.com/Twizter01/Twizter01/output/github-contribution-grid-snake-dark.svg" alt="Snake animation" />
        </div>

        <!-- Stats Section -->
        <div class="stats-section">
            <div class="stats-header">
                <h2>⚡ Stats ⚡</h2>
            </div>
            <div class="stats-grid">
                <div class="stat-card">
                    <img src="https://github-readme-streak-stats.herokuapp.com/?user=Twizter01&count_private=true&theme=react&border_radius=10" alt="GitHub Streak Stats" />
                </div>
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api?username=Twizter01&count_private=true&show_icons=true&theme=react&rank_icon=github&border_radius=10" alt="GitHub Stats" />
                </div>
            </div>
            <div class="stat-card" style="max-width: 400px; margin: 0 auto;">
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Twizter01&hide=HTML&langs_count=8&layout=compact&theme=react&border_radius=10&size_weight=0.5&count_weight=0.5&exclude_repo=github-readme-stats" alt="Top Languages" />
            </div>
        </div>

        <!-- Activity Section -->
        <div class="activity-section">
            <h2>📈 Activity & Contributions Analysis</h2>
            <img class="activity-graph" src="https://github-readme-activity-graph.vercel.app/graph?username=Twizter01&theme=react-dark&bg_color=0d1117&color=58a6ff&line=39d353&point=58a6ff&area=true&hide_border=true" alt="Activity Graph" />
            
            <div class="summary-grid">
                <div class="stat-card">
                    <img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=Twizter01&theme=github_dark" alt="Repos per Language" />
                </div>
                <div class="stat-card">
                    <img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=Twizter01&theme=github_dark" alt="Most Commit Language" />
                </div>
                <div class="stat-card">
                    <img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=Twizter01&theme=github_dark" alt="Stats" />
                </div>
                <div class="stat-card">
                    <img src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=Twizter01&theme=github_dark&utc_offset=8" alt="Productive Time" />
                </div>
            </div>
        </div>

        <!-- Trophies Section -->
        <div class="trophies-section">
            <h2>🏆 GitHub Trophies</h2>
            <img src="https://github-profile-trophy.vercel.app/?username=Twizter01&theme=onedark&no-frame=false&no-bg=true&margin-w=4" alt="GitHub Trophies" />
        </div>

        <!-- Connect Section -->
        <div class="connect-section">
            <h2>🌐 Connect with me</h2>
            <div class="social-links">
                <a href="https://www.linkedin.com/in/gabriel-jimenez-a28b73316" class="social-link" target="_blank">
                    📧 LinkedIn
                </a>
                <a href="https://github.com/Twizter01" class="social-link" target="_blank">
                    🐙 GitHub
                </a>
                <a href="https://twizter01.github.io" class="social-link" target="_blank">
                    🌐 Portfolio
                </a>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <div class="footer-wave"></div>
            <div class="footer-text">
                💙 This README was enhanced with 3D contributions and radar charts
            </div>
        </div>
    </div>

    <script>
        // 3D Contributions Chart
        const canvas3d = document.getElementById('contributions3d');
        const ctx3d = canvas3d.getContext('2d');
        
        let rotationX = -0.6;
        let rotationY = 0.8;
        let animationFrame;

        // Generate sample contribution data (52 weeks x 7 days)
        const contributionData = [];
        for (let week = 0; week < 52; week++) {
            const weekData = [];
            for (let day = 0; day < 7; day++) {
                // Create more realistic contribution pattern
                const baseActivity = Math.random() * 5;
                const weekdayBoost = day >= 1 && day <= 5 ? 3 : 0;
                weekData.push(Math.floor(baseActivity + weekdayBoost + Math.random() * 3));
            }
            contributionData.push(weekData);
        }

        function draw3DContributions() {
            ctx3d.clearRect(0, 0, canvas3d.width, canvas3d.height);
            
            const centerX = canvas3d.width / 2;
            const centerY = canvas3d.height / 2;
            const scale = 6;
            
            // Create isometric projection
            const cubes = [];
            
            for (let week = 0; week < contributionData.length; week++) {
                for (let day = 0; day < contributionData[week].length; day++) {
                    const height = contributionData[week][day];
                    if (height > 0) {
                        const x = week - 26;
                        const y = day - 3;
                        const z = height;
                        
                        // 3D rotation
                        const cosX = Math.cos(rotationX);
                        const sinX = Math.sin(rotationX);
                        const cosY = Math.cos(rotationY);
                        const sinY = Math.sin(rotationY);
                        
                        const x1 = x * cosY - z * sinY;
                        const z1 = x * sinY + z * cosY;
                        const y1 = y * cosX - z1 * sinX;
                        const z2 = y * sinX + z1 * cosX;
                        
                        cubes.push({
                            x: x1,
                            y: y1,
                            z: z2,
                            height: height,
                            week: week,
                            day: day
                        });
                    }
                }
            }
            
            // Sort by depth for proper rendering
            cubes.sort((a, b) => b.z - a.z);
            
            // Draw cubes
            cubes.forEach(cube => {
                const screenX = centerX + cube.x * scale;
                const screenY = centerY + cube.y * scale;
                
                // Color based on contribution intensity (GitHub-like)
                const intensity = Math.min(cube.height / 10, 1);
                let color;
                if (intensity < 0.25) {
                    color = '#0e4429';
                } else if (intensity < 0.5) {
                    color = '#006d32';
                } else if (intensity < 0.75) {
                    color = '#26a641';
                } else {
                    color = '#39d353';
                }
                
                // Draw cube faces
                ctx3d.fillStyle = color;
                ctx3d.strokeStyle = '#21262d';
                ctx3d.lineWidth = 0.5;
                
                const size = scale * 0.9;
                const height3d = cube.height * scale * 0.4;
                
                // Top face
                ctx3d.fillRect(screenX - size/2, screenY - size/2 - height3d, size, size);
                ctx3d.strokeRect(screenX - size/2, screenY - size/2 - height3d, size, size);
                
                // Front face (darker)
                const darkerColor = adjustBrightness(color, -30);
                ctx3d.fillStyle = darkerColor;
                ctx3d.fillRect(screenX - size/2, screenY - size/2 - height3d, size, height3d);
                ctx3d.strokeRect(screenX - size/2, screenY - size/2 - height3d, size, height3d);
            });
        }

        function adjustBrightness(hex, percent) {
            const num = parseInt(hex.replace("#", ""), 16);
            const amt = Math.round(2.55 * percent);
            const R = (num >> 16) + amt;
            const G = (num >> 8 & 0x00FF) + amt;
            const B = (num & 0x0000FF) + amt;
            return "#" + (0x1000000 + (R < 255 ? R < 1 ? 0 : R : 255) * 0x10000 +
                (G < 255 ? G < 1 ? 0 : G : 255) * 0x100 +
                (B < 255 ? B < 1 ? 0 : B : 255)).toString(16).slice(1);
        }

        // Radar Chart
