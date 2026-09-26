<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Filsafat Pikiran dan Tradisi</title>
  <style>
    body {
      margin: 0;
      background-color: #000;
      color: #eee;
      font-family: 'Georgia', serif;
      text-align: center;
      overflow-x: hidden;
    }
    h1 {
      color: #d4af37;
      margin-top: 60px;
      font-size: 30px;
      letter-spacing: 1px;
    }
    .filsafat {
      font-size: 20px;
      line-height: 1.8;
      opacity: 0;
      transition: opacity 2s ease-in-out;
      margin: 20px auto;
      width: 80%;
    }
    .filsafat.show {
      opacity: 1;
    }
    canvas {
      position: fixed;
      top: 0;
      left: 0;
      z-index: -1;
    }
  </style>
</head>
<body>
  <h1>Filsafat Pikiran dan Tradisi</h1>
  <div id="filsafat-container">
    <p class="filsafat"><span class="highlight">Hanya ada sedikit orang yang mampu berpikir,</span></p>
    <p class="filsafat">sisanya mengikuti tradisi.</p>
    <p class="filsafat">Berpikir berarti berani mempertanyakan,</p>
    <p class="filsafat">sementara tradisi memberi rasa aman.</p>
    <p class="filsafat">Namun, tanpa refleksi, tradisi bisa menjadi belenggu.</p>
    <p class="filsafat">Tradisi memberi akar, pikiran memberi sayap.</p>
  </div>

  <!-- Three.js CDN -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
  <script>
    // Planet 3D
    const scene = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera(75, window.innerWidth/window.innerHeight, 0.1, 1000);
    const renderer = new THREE.WebGLRenderer({antialias:true});
    renderer.setSize(window.innerWidth, window.innerHeight);
    document.body.appendChild(renderer.domElement);

    const geometry = new THREE.SphereGeometry(2, 64, 64);
    const texture = new THREE.TextureLoader().load('https://threejsfundamentals.org/threejs/resources/images/earth.jpg');
    const material = new THREE.MeshStandardMaterial({map: texture});
    const planet = new THREE.Mesh(geometry, material);
    scene.add(planet);

    const light = new THREE.PointLight(0xffffff, 1, 100);
    light.position.set(10, 10, 10);
    scene.add(light);

    camera.position.z = 5;

    function animate() {
      requestAnimationFrame(animate);
      planet.rotation.y += 0.002; // rotasi planet
      renderer.render(scene, camera);
    }
    animate();

    // Efek scroll: planet bergerak sesuai scroll
    window.addEventListener('scroll', () => {
      const scrollY = window.scrollY;
      planet.rotation.x = scrollY * 0.001;
      planet.rotation.y = scrollY * 0.001;
    });

    // Efek teks fade-in
    const lines = document.querySelectorAll('.filsafat');
    lines.forEach((line, index) => {
      setTimeout(() => {
        line.classList.add('show');
      }, index * 2500);
    });
  </script>
</body>
</html>
