x-fam/
├── index.html<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI16Z Hat</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>AI16Z Hat</h1>
        <p>Click the hat to become a partner!</p>
        <img id="hatImage" src="images/hat.png" alt="AI16Z Hat">
    </div>
    <script src="script.js"></script>
</body>
</html>
├── styles.cssbody {
    font-family: 'Arial', sans-serif;
    background-color: #f0f0f0;
    text-align: center;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.container {
    background: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
    max-width: 400px;
    width: 100%;
}

h1 {
    color: #333;
    margin-bottom: 10px;
}

p {
    color: #666;
    margin-bottom: 20px;
}

#hatImage {
    width: 150px;
    height: auto;
    cursor: pointer;
    transition: transform 0.3s ease;
}

#hatImage:hover {
    transform: scale(1.1);
}
├── script.jsdocument.addEventListener('DOMContentLoaded', (event) => {
    const hatImage = document.getElementById('hatImage');
    
    // 간단한 클릭 이벤트 추가
    hatImage.addEventListener('click', function() {
        alert('You are now an AI16Z partner!');
        
        // 이미지에 애니메이션 효과 추가
        this.style.transform = 'scale(1.2)';
        setTimeout(() => {
            this.style.transform = '';
        }, 500);
    });
});
└── images/
    └── hat.png
