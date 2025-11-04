<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="AI Image Upscaler — Enhance your images instantly using AI. Upload your photo and get high-resolution results in seconds.">
  <title>AI Image Upscaler</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Poppins", sans-serif;
    }

    body {
      background: #f4f6f8;
      color: #333;
      line-height: 1.6;
      overflow-x: hidden;
    }

    header {
      background: linear-gradient(135deg, #0072ff, #00c6ff);
      color: #fff;
      text-align: center;
      padding: 4rem 1rem;
    }

    header h1 {
      font-size: 2.8rem;
      margin-bottom: 1rem;
    }

    header p {
      font-size: 1.2rem;
      max-width: 600px;
      margin: 0 auto;
    }

    .container {
      max-width: 1000px;
      margin: 3rem auto;
      padding: 0 1rem;
      text-align: center;
    }

    .upload-box {
      background: #fff;
      border: 2px dashed #00a8ff;
      padding: 3rem 1rem;
      border-radius: 15px;
      transition: 0.3s;
    }

    .upload-box:hover {
      background: #e6f7ff;
    }

    input[type="file"] {
      margin-top: 1rem;
    }

    button {
      background: #0072ff;
      color: #fff;
      border: none;
      padding: 0.8rem 1.5rem;
      margin-top: 1.5rem;
      font-size: 1rem;
      border-radius: 30px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background: #005fcc;
    }

    section.features {
      margin-top: 4rem;
      text-align: left;
    }

    .feature-list {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
      margin-top: 2rem;
    }

    .feature {
      background: #fff;
      border-radius: 15px;
      padding: 2rem;
      box-shadow: 0 3px 8px rgba(0, 0, 0, 0.05);
      transition: transform 0.3s;
    }

    .feature:hover {
      transform: translateY(-5px);
    }

    .feature h3 {
      color: #0072ff;
      margin-bottom: 0.5rem;
    }

    footer {
      text-align: center;
      padding: 2rem 0;
      background: #111;
      color: #fff;
      margin-top: 4rem;
    }

    footer p {
      font-size: 0.9rem;
    }
  </style>
</head>
<body>
  <header>
    <h1>AI Image Upscaler</h1>
    <p>Enhance your images instantly using advanced AI. Upload your photo and get HD quality in just seconds.</p>
  </header>

  <div class="container">
    <div class="upload-box">
      <h2>Upload Your Image</h2>
      <input type="file" id="imageUpload" accept="image/*" />
      <br />
      <button id="upscaleBtn">Upscale Image</button>
      <p id="status"></p>
    </div>

    <section class="features">
      <h2>💡 Key Features</h2>
      <div class="feature-list">
        <div class="feature">
          <h3>🔍 AI Super Resolution</h3>
          <p>Increase image size up to 8× while preserving sharpness and details.</p>
        </div>
        <div class="feature">
          <h3>🎨 Smart Detail Enhancement</h3>
          <p>Automatically improves textures, colors, and edges for a more realistic look.</p>
        </div>
        <div class="feature">
          <h3>⚡ Fast & Secure</h3>
          <p>Process your images instantly with cloud-based AI technology.</p>
        </div>
        <div class="feature">
          <h3>🧠 User-Friendly</h3>
          <p>No technical skills needed — just upload, upscale, and download.</p>
        </div>
      </div>
    </section>
  </div>

  <footer>
    <p>© 2025 AI Image Upscaler | All Rights Reserved</p>
  </footer>

  <script>
    const uploadInput = document.getElementById("imageUpload");
    const upscaleBtn = document.getElementById("upscaleBtn");
    const status = document.getElementById("status");

    upscaleBtn.addEventListener("click", () => {
      if (!uploadInput.files.length) {
        status.textContent = "Please upload an image first.";
        status.style.color = "red";
        return;
      }
      status.textContent = "Upscaling your image... (Demo Mode)";
      status.style.color = "black";

      setTimeout(() => {
        status.textContent = "✅ Image upscaled successfully! (Demo Result)";
        status.style.color = "green";
      }, 2000);
    });
  </script>
</body>
</html>
