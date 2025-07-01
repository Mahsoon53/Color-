# Color-
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>اشعار حسین سبزواری </title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #1a2a6c);
            padding: 20px;
        }
        
        .container {
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            padding: 40px;
            width: 100%;
            max-width: 800px;
            text-align: center;
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.8rem;
        }
        
        .subtitle {
            color: #7f8c8d;
            margin-bottom: 40px;
            font-size: 1.2rem;
        }
        
        .buttons-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 25px;
            margin: 40px 0;
        }
        
        .color-button {
            width: 150px;
            height: 150px;
            border: none;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            font-weight: bold;
            font-size: 1.3rem;
        }
        
        .color-button:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 15px 20px rgba(0, 0, 0, 0.25);
        }
        
        .color-button i {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }
        
        #blue-btn {
            background: linear-gradient(135deg, #3498db, #2980b9);
        }
        
        #red-btn {
            background: linear-gradient(135deg, #e74c3c, #c0392b);
        }
        
        #yellow-btn {
            background: linear-gradient(135deg, #f1c40f, #f39c12);
            color: #2c3e50;
        }
        
        #green-btn {
            background: linear-gradient(135deg, #2ecc71, #27ae60);
        }
        
        .display-box {
            background-color: #ecf0f1;
            border-radius: 15px;
            padding: 30px;
            margin: 30px 0;
            min-height: 150px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.1);
        }
        
        .color-name {
            font-size: 3.5rem;
            font-weight: 800;
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
        }
        
        .instructions {
            background-color: #e3f2fd;
            border-left: 5px solid #2196f3;
            padding: 20px;
            border-radius: 10px;
            margin-top: 30px;
            text-align: right;
            color: #2c3e50;
        }
        
        .instructions h3 {
            margin-bottom: 10px;
            color: #0d47a1;
        }
        
        .footer {
            margin-top: 30px;
            color: #7f8c8d;
            font-size: 0.9rem;
        }
        
        @media (max-width: 600px) {
            .container {
                padding: 20px;
            }
            
            .color-button {
                width: 120px;
                height: 120px;
                font-size: 1.1rem;
            }
            
            .color-name {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1><i class="fas fa-palette"></i> نمایش رنگ با دکمه‌ها</h1>
        <p class="subtitle">روی هر دکمه کلیک کنید تا نام رنگ آن نمایش داده شود</p>
        
        <div class="buttons-container">
            <button id="blue-btn" class="color-button" onclick="showColor('آبی')">
                <i class="fas fa-water"></i>
                آبی
            </button>
            <button id="red-btn" class="color-button" onclick="showColor('قرمز')">
                <i class="fas fa-fire"></i>
                قرمز
            </button>
            <button id="yellow-btn" class="color-button" onclick="showColor('زرد')">
                <i class="fas fa-sun"></i>
                زرد
            </button>
            <button id="green-btn" class="color-button" onclick="showColor('سبز')">
                <i class="fas fa-leaf"></i>
                سبز
            </button>
        </div>
        
        <div class="display-box">
            <div id="color-display" class="color-name">رنگ انتخاب شده را اینجا مشاهده می‌کنید</div>
        </div>
        
        <div class="instructions">
            <h3><i class="fas fa-info-circle"></i> راهنما</h3>
            <p>برای مشاهده نام هر رنگ، کافیست روی دکمه مربوطه کلیک کنید. نام رنگ در کادر بالا به نمایش درخواهد آمد.</p>
        </div>
        
        <div class="footer">
            این برنامه توسط حسین سبزواری با HTML، CSS و JavaScript ساخته شده و در مرورگر کروم قابل اجرا است
        </div>
    </div>

    <script>
        function showColor(colorName) {
            const colorDisplay = document.getElementById('color-display');
            colorDisplay.textContent = colorName;
            
            // Add animation effect
            colorDisplay.style.transform = 'scale(1.2)';
            colorDisplay.style.opacity = '0.7';
            
            setTimeout(() => {
                colorDisplay.style.transform = 'scale(1)';
                colorDisplay.style.opacity = '1';
            }, 300);
            
            // Change text color based on the selected color
            if(colorName === 'زرد') {
                colorDisplay.style.color = '#d35400';
            } else {
                colorDisplay.style.color = colorName;
            }
        }
    </script>
</body>
</html>
