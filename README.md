<div align="center">
  <h2>📊 3D Contributions & Radar Chart 📊</h2>

  <!-- 3D Contributions Chart -->
  <div id="contributionsChart" style="width: 80%; height: 400px;"></div>

  <!-- Radar Chart -->
  <canvas id="radarChart" width="400" height="400"></canvas>
</div>

<!-- Include Plotly.js and Chart.js Libraries -->
<script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<script>
  // 3D Contributions Chart (Plotly)
  var contributionsData = {
      x: ["Jan", "Feb", "Mar", "Apr", "May", "Jun"],
      y: ["2024", "2025"],
      z: [[10, 20, 30, 40, 50, 60], [15, 25, 35, 45, 55, 65]],
      type: "surface"
  };

  var layout3D = {
      title: "GitHub Contributions",
      scene: { xaxis: { title: "Month" }, yaxis: { title: "Year" }, zaxis: { title: "Commits" } }
  };

  Plotly.newPlot("contributionsChart", [contributionsData], layout3D);

  // Radar Chart (Chart.js)
  var ctx = document.getElementById("radarChart").getContext("2d");

  new Chart(ctx, {
      type: "radar",
      data: {
          labels: ["Coding", "Issues", "Pull Requests", "Reviews", "Commits"],
          datasets: [{
              label: "Activity",
              data: [85, 65, 90, 75, 95],
              backgroundColor: "rgba(0, 128, 255, 0.2)",
              borderColor: "rgba(0, 128, 255, 1)",
              borderWidth: 2
          }]
      },
      options: {
          scale: { ticks: { beginAtZero: true } }
      }
  });
</script>
