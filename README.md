<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Twizter01 - GitHub Profile</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/3.9.1/chart.min.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #0c1427 0%, #1a1f2e 100%);
            color: #e1e8ef;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .visitor-badge {
            text-align: right;
            margin-bottom: 20px;
        }

        .visitor-badge img {
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 123, 255, 0.3);
        }

        .hero-section {
            text-align: center;
            margin: 40px 0;
        }

        .typing-animation {
            font-size: 3.5rem;
            font-weight: bold;
            background: linear-gradient(45deg, #007bff, #28a745, #ffc107, #dc3545);
            background-size: 400% 400%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradient-shift 3s ease-in-out infinite;
            margin: 20px 0;
        }

        @keyframes gradient-shift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .subtitle {
            font-size: 1.5rem;
            color: #a855f7;
            margin-bottom: 40px;
        }

        .about-section {
            background: rgba(22, 27, 34, 0.8);
            border: 1px solid #30363d;
            border-radius: 16px;
            padding: 30px;
            margin: 30px 0;
            backdrop-filter: blur(10px);
        }

        .section-title {
            font-size: 2rem;
            text-align: center;
            margin-bottom: 20px;
            color: #58a6ff;
        }

        .about-content {
            text-align: left;
            line-height: 1.8;
            font-size: 1.1rem;
        }

        .about-content a {
            color: #58a6ff;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .about-content a:hover {
            color: #79c0ff;
        }

        .skills-section {
            text-align: center;
            margin: 40px 0;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(60px, 1fr));
            gap: 15px;
            max-width: 800px;
            margin: 0 auto;
        }

        .skill-icon {
            width: 60px;
            height: 60px;
            border-radius: 12px;
            background: rgba(88, 166, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .skill-icon:hover {
            transform: translateY(-5px) scale(1.1);
            background: rgba(88, 166, 255, 0.2);
            box-shadow: 0 8px 25px rgba(88, 166, 255, 0.3);
        }

        .visualization-section {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin: 40px 0;
        }

        .chart-container {
            background: rgba(22, 27, 34, 0.8);
            border: 1px solid #30363d;
            border-radius: 16px;
            padding: 20px;
            backdrop-filter: blur(10px);
        }

        .contributions-3d {
            grid-column: 1 / -1;
            height: 400px;
            position: relative;
            background: rgba(22, 27, 34, 0.8);
            border: 1px solid #30363d;
            border-radius: 16px;
            overflow: hidden;
        }

        .stats-overview {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin: 30px 0;
            flex-wrap: wrap;
        }

        .stat-item {
            text-align: center;
            background: rgba(22, 27, 34, 0.8);
            border: 1px solid #30363d;
            border-radius: 12px;
            padding: 20px;
            min-width: 120px;
        }

        .stat-number {
            font-size: 2rem;
            font-weight: bold;
            color: #58a6ff;
        }

        .stat-label {
            color: #8b949e;
            margin-top: 5px;
        }

        .snake-section {
            text-align: center;
            margin: 40px 0;
            background: rgba(22, 27, 34, 0.8);
            border: 1px solid #30363d;
            border-radius: 16px;
            padding: 30px;
        }

        .date-range {
            position: absolute;
            top: 20px;
            right: 20px;
            color: #8b949e;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .typing-animation {
                font-size: 2.5rem;
            }
            
            .visualization-section {
                grid-template-columns: 1fr;
            }
            
            .stats-overview {
                gap: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Visitor Badge -->
        <div class="visitor-badge">
            <img src="https://visitor-badge.laobi.icu/badge?page_id=Twizter01.Twizter01" alt="visitor badge" />
        </div>

        <!-- Hero Section -->
        <div class="hero-section">
            <div class="typing-animation">Hey, I'm Twizter! 👋</div>
            <div class="subtitle">A passionate software developer from Colombia</div>
        </div>

        <!-- About Section -->
        <div class="about-section">
            <h2 class="section-title">🌟 A little About Me</h2>
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
            <h2 class="section-title">⚒️ Languages - Frameworks - Tools ⚒️</h2>
            <div class="skills-grid">
                <div class="skill-icon" title="HTML">🌐</div>
                <div class="skill-icon" title="CSS">🎨</div>
                <div class="skill-icon" title="JavaScript">⚡</div>
                <div class="skill-icon" title="TypeScript">📘</div>
                <div class="skill-icon" title="C++">⚙️</div>
                <div class="skill-icon" title="Python">🐍</div>
                <div class="skill-icon" title="Bash">💻</div>
                <div class="skill-icon" title="React">⚛️</div>
                <div class="skill-icon" title="Tailwind">🎭</div>
                <div class="skill-icon" title="Node.js">📗</div>
                <div class="skill-icon" title="Django">🎯</div>
                <div class="skill-icon" title="Firebase">🔥</div>
                <div class="skill-icon" title="MongoDB">🍃</div>
                <div class="skill-icon" title="SQLite">📊</div>
                <div class="skill-icon" title="VS Code">👨‍💻</div>
                <div class="skill-icon" title="Git">📝</div>
                <div class="skill-icon" title="GitHub">🐙</div>
                <div class="skill-icon" title="Linux">🐧</div>
                <div class="skill-icon" title="Figma">🎨</div>
            </div>
        </div>

        <!-- 3D Contributions Visualization -->
        <div class="contributions-3d">
            <div class="date-range">2024-06-09 / 2025-06-12</div>
            <div id="threejs-container"></div>
        </div>

        <!-- Stats Overview -->
        <div class="stats-overview">
            <div class="stat-item">
                <div class="stat-number">4123</div>
                <div class="stat-label">contributions</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">⭐ 112</div>
                <div class="stat-label">stars</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">🍴 12</div>
                <div class="stat-label">forks</div>
            </div>
        </div>

        <!-- Visualization Section -->
        <div class="visualization-section">
            <!-- Radar Chart -->
            <div class="chart-container">
                <h3 style="text-align: center; margin-bottom: 20px; color: #58a6ff;">Activity Overview</h3>
                <canvas id="radarChart" width="300" height="300"></canvas>
            </div>

            <!-- Language Distribution -->
            <div class="chart-container">
                <h3 style="text-align: center; margin-bottom: 20px; color: #58a6ff;">Language Distribution</h3>
                <canvas id="languageChart" width="300" height="300"></canvas>
            </div>
        </div>

        <!-- Snake Animation Section -->
        <div class="snake-section">
            <h2 class="section-title">🐍 My Contributions 🐍</h2>
            <div style="background: #0d1117; padding: 20px; border-radius: 12px; margin-top: 20px;">
                <svg width="100%" height="200" style="background: #0d1117;">
                    <!-- Animated snake-like path -->
                    <path id="snake-path" d="M 50 100 Q 200 50 350 100 T 650 100 Q 800 150 950 100" 
                          stroke="#39d353" stroke-width="8" fill="none" opacity="0.8">
                        <animate attributeName="stroke-dasharray" values="0,1000;1000,0;0,1000" dur="3s" repeatCount="indefinite"/>
                    </path>
                    <!-- Contribution squares -->
                    <g id="contribution-squares"></g>
                </svg>
            </div>
        </div>

        <!-- GitHub Stats -->
        <div style="text-align: center; margin: 40px 0;">
            <h2 class="section-title">⚡ Stats ⚡</h2>
            <div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 20px 0;">
                <img width="390" src="https://github-readme-streak-stats.herokuapp.com/?user=Twizter01&count_private=true&theme=react&border_radius=10" alt="GitHub Streak Stats" style="border-radius: 10px;" />
                <img width="390" src="https://github-readme-stats.vercel.app/api?username=Twizter01&count_private=true&show_icons=true&theme=react&rank_icon=github&border_radius=10" alt="GitHub Stats" style="border-radius: 10px;" />
            </div>
            <img width="325" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Twizter01&hide=HTML&langs_count=8&layout=compact&theme=react&border_radius=10&size_weight=0.5&count_weight=0.5&exclude_repo=github-readme-stats" alt="Top Languages" style="border-radius: 10px;" />
        </div>
    </div>

    <script>
        // 3D Contributions Visualization with Three.js
        function init3DContributions() {
            const container = document.getElementById('threejs-container');
            const scene = new THREE.Scene();
            const camera = new THREE.PerspectiveCamera(75, container.offsetWidth / container.offsetHeight, 0.1, 1000);
            const renderer = new THREE.WebGLRenderer({ alpha: true, antialias: true });
            
            renderer.setSize(container.offsetWidth, container.offsetHeight);
            renderer.setClearColor(0x000000, 0);
            container.appendChild(renderer.domElement);

            // Create isometric contribution grid
            const geometry = new THREE.BoxGeometry(0.8, 0.1, 0.8);
            const contributions = [];
            
            for (let x = 0; x < 53; x++) {
                for (let z = 0; z < 7; z++) {
                    const intensity = Math.random();
                    const height = 0.1 + intensity * 2;
                    
                    const boxGeometry = new THREE.BoxGeometry(0.8, height, 0.8);
                    const material = new THREE.MeshBasicMaterial({
                        color: intensity > 0.7 ? 0x39d353 : 
                               intensity > 0.5 ? 0x26a641 : 
                               intensity > 0.3 ? 0x006d32 : 
                               intensity > 0.1 ? 0x0e4429 : 0x161b22
                    });
                    
                    const cube = new THREE.Mesh(boxGeometry, material);
                    cube.position.set(x - 26, height / 2, z - 3);
                    scene.add(cube);
                    contributions.push(cube);
                }
            }

            // Position camera for isometric view
            camera.position.set(30, 20, 30);
            camera.lookAt(0, 0, 0);

            // Animation loop
            function animate() {
                requestAnimationFrame(animate);
                
                // Subtle rotation
                scene.rotation.y += 0.002;
                
                renderer.render(scene, camera);
            }
            
            animate();

            // Handle window resize
            window.addEventListener('resize', () => {
                if (container.offsetWidth > 0) {
                    camera.aspect = container.offsetWidth / container.offsetHeight;
                    camera.updateProjectionMatrix();
                    renderer.setSize(container.offsetWidth, container.offsetHeight);
                }
            });
        }

        // Radar Chart
        function createRadarChart() {
            const ctx = document.getElementById('radarChart').getContext('2d');
            new Chart(ctx, {
                type: 'radar',
                data: {
                    labels: ['Commit', 'Issue', 'PullReq', 'Review', 'Repo'],
                    datasets: [{
                        data: [8, 3, 6, 4, 7],
                        backgroundColor: 'rgba(57, 211, 83, 0.3)',
                        borderColor: '#39d353',
                        borderWidth: 2,
                        pointBackgroundColor: '#39d353',
                        pointBorderColor: '#39d353',
                        pointRadius: 6
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: { display: false }
                    },
                    scales: {
                        r: {
                            beginAtZero: true,
                            max: 10,
                            grid: { color: '#30363d' },
                            pointLabels: { color: '#58a6ff', font: { size: 12 } },
                            ticks: { display: false }
                        }
                    }
                }
            });
        }

        // Language Distribution Chart
        function createLanguageChart() {
            const ctx = document.getElementById('languageChart').getContext('2d');
            new Chart(ctx, {
                type: 'doughnut',
                data: {
                    labels: ['TypeScript', 'Python', 'SCSS', 'HTML', 'C#', 'Other'],
                    datasets: [{
                        data: [45, 20, 15, 8, 7, 5],
                        backgroundColor: [
                            '#3178c6',
                            '#3776ab',
                            '#cf649a',
                            '#e34c26',
                            '#239120',
                            '#6c757d'
                        ],
                        borderWidth: 0
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            position: 'right',
                            labels: { color: '#e1e8ef', usePointStyle: true }
                        }
                    }
                }
            });
        }

        // Generate contribution squares for snake animation
        function generateContributionSquares() {
            const svg = document.getElementById('contribution-squares');
            const colors = ['#161b22', '#0e4429', '#006d32', '#26a641', '#39d353'];
            
            for (let i = 0; i < 100; i++) {
                const rect = document.createElementNS('http://www.w3.org/2000/svg', 'rect');
                rect.setAttribute('x', (i * 10) % 980);
                rect.setAttribute('y', Math.floor(i / 98) * 12 + 150);
                rect.setAttribute('width', '8');
                rect.setAttribute('height', '8');
                rect.setAttribute('rx', '2');
                rect.setAttribute('fill', colors[Math.floor(Math.random() * colors.length)]);
                
                // Add animation delay
                rect.style.animationDelay = `${i * 0.05}s`;
                svg.appendChild(rect);
            }
        }

        // Initialize everything when page loads
        document.addEventListener('DOMContentLoaded', function() {
            setTimeout(() => {
                init3DContributions();
                createRadarChart();
                createLanguageChart();
                generateContributionSquares();
            }, 100);
        });
    </script>
</body>
</html>
