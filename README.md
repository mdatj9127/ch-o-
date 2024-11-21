<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Trang Web Tương Tác</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
      background-color: #f0f8ff;
    }
    .container {
      max-width: 600px;
      margin: auto;
      padding: 20px;
      background: #fff;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      border-radius: 8px;
    }
    button {
      background-color: #4CAF50;
      color: white;
      border: none;
      padding: 10px 20px;
      font-size: 16px;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #45a049;
    }
    .result {
      margin-top: 20px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Trang Web Tương Tác</h1>
    <p>Nhập tên của bạn và nhấn nút để hiển thị lời chào:</p>
    <form id="interactiveForm">
      <label for="name">Tên của bạn:</label>
      <input type="text" id="name" name="name" placeholder="Nhập tên của bạn" required style="width: 100%; padding: 10px; margin-top: 10px; margin-bottom: 20px; font-size: 16px;">
      <button type="submit">Hiển thị lời chào</button>
    </form>
    <div class="result" id="result"></div>
  </div>

  <script>
    document.getElementById('interactiveForm').addEventListener('submit', function(event) {
      event.preventDefault(); // Ngăn không tải lại trang
      const name = document.getElementById('name').value;
      const resultDiv = document.getElementById('result');
      if (name.trim()) {
        resultDiv.textContent = `Xin chào, ${name}! Chúc bạn một ngày vui vẻ!`;
      } else {
        resultDiv.textContent = 'Vui lòng nhập tên của bạn!';
      }
    });
  </script>
</body>
</html>
