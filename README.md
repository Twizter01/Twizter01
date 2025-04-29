<!-- Visitor Badge -->
<p align="right">
  <img src="https://visitor-badge.laobi.icu/badge?page_id=Twizter01.Twizter01" alt="visitor badge" />
</p>

<!-- Header -->
<h1 align="center">
  <img src="https://readme-typing-svg.herokuapp.com/?font=Righteous&size=35&center=true&vCenter=true&width=500&height=70&duration=4000&lines=Hey,+I'm+Twizter!+👋" alt="Typing SVG" />
</h1>

<h3 align="center" color="purple">A passionate software developer from Colombia</h3>

<br/>

<!-- About Me Section -->
<div align="center">

  <h2>🌟 A little About Me</h2>

  🔭 I’m currently working as a Sales Executive.<br/>
  🌱 I’m currently learning Data Science and Systems Engineering.<br/>
  🎨 I’m a CSS Lover.<br/>
  👯 I’m looking to collaborate on front-end or back-end projects. My focus is to build profitable and scalable solutions.<br/>
  📫 How to reach me: <a href="https://www.linkedin.com/in/gabriel-jimenez-a28b73316" target="_blank">LinkedIn</a><br/>
  😄 Pronouns: He/Him.<br/>
  🚀 I'm a first-year Computer Science student who absolutely adores nature.<br/>

</div>

<br/>

<!-- Contact Badges -->
<div align="center"> 
  <a href="mailto:Gabrielandrejimenez11@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-333333?style=for-the-badge&logo=gmail&logoColor=purple" alt="gmail" />
  </a>
  <a href="https://www.linkedin.com/in/gabriel-jimenez-a28b73316" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="linkedin" />
  </a>
  <a href="https://Twizter01.github.io" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=todoist&logoColor=black" alt="portfolio" />
  </a>
</div>

<br/>
<hr/>

<!-- Languages, Frameworks, Tools Section -->
<h2 align="center">⚒️ Languages - Frameworks - Tools ⚒️</h2>

<div align="center">
  <img src="https://skillicons.dev/icons?i=html,css,vscode,github,figma,tailwind,git,linux,nodejs,python,javascript,typescript,firebase,mongodb,sqlite" alt="skills" />
</div>

<br/>
<hr/>

<!-- Snake Contributions -->
<div align="center">
  <h2>🐍 My Contributions 🐍</h2>
  <br/>
  <img alt="Snake animation" src="https://github.com/Twizter01/Twizter01/blob/output/github-contribution-grid-snake.svg?raw=true" />
</div>

<br/>
<hr/>

<!-- Stats Section -->
<h2 align="center">⚡ Stats ⚡</h2>

<div align="center">
  <img width="390" src="https://github-readme-streak-stats.herokuapp.com/?user=Twizter01&count_private=true&theme=react&border_radius=10" alt="GitHub Streak Stats" />
  
  <img width="390" src="https://github-readme-stats.vercel.app/api?username=Twizter01&count_private=true&show_icons=true&theme=react&rank_icon=github&border_radius=10" alt="GitHub Stats" />
  
  <br/><br/>
  
  <img width="325" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Twizter01&hide=html&langs_count=8&layout=compact&theme=react&border_radius=10" alt="Top Languages" />
</div>

<br/><br/>
<hr/>



<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>GitHub Snake Animation</title>
  <style>
    body { margin: 0; background: #0d1117; display: flex; justify-content: center; align-items: center; height: 100vh; }
    canvas { background: #0d1117; }
  </style>
</head>
<body>
<canvas id="snakeCanvas" width="840" height="120"></canvas>

<script>
// Configuration
const username = "YOUR_GITHUB_USERNAME";  // Replace with your username
const canvas = document.getElementById("snakeCanvas");
const ctx = canvas.getContext("2d");
const gridSize = 10;
const cellSize = 12;
let snake = [{x: 0, y: 0}];
let direction = {x: 1, y: 0};

// Simulated contributions (fill in with real data)
let contributions = Array(52 * 7).fill(0).map(() => Math.floor(Math.random() * 5)); // fake levels

function drawGrid() {
  for (let i = 0; i < 52; i++) {
    for (let j = 0; j < 7; j++) {
      const index = i * 7 + j;
      const level = contributions[index];
      ctx.fillStyle = ["#161b22", "#0e4429", "#006d32", "#26a641", "#39d353"][level];
      ctx.fillRect(i * cellSize, j * cellSize, cellSize - 1, cellSize - 1);
    }
  }
}

function drawSnake() {
  for (const segment of snake) {
    ctx.fillStyle = "orange";
    ctx.fillRect(segment.x * cellSize, segment.y * cellSize, cellSize - 1, cellSize - 1);
  }
}

function moveSnake() {
  const head = {...snake[0]};
  head.x += direction.x;
  head.y += direction.y;

  if (head.x >= 52) {
    head.x = 0;
    head.y = (head.y + 1) % 7;
  }

  snake.unshift(head);
  snake = snake.slice(0, 10); // keep snake length
}

function animate() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);
  drawGrid();
  moveSnake();
  drawSnake();
  requestAnimationFrame(animate);
}

drawGrid();
animate();
</script>
</body>
</html>
