<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>色語 - AI色彩鑒定</title>
    <style>
        body { font-family: 'Helvetica', sans-serif; background: #fdf9f5; color: #333; margin: 0; padding: 0; }
        .header { background: #fff; padding: 20px; text-align: center; border-bottom: 1px solid #eee; }
        .container { max-width: 500px; margin: 0 auto; padding: 20px; }
        .btn { background: #D4A59A; color: white; padding: 15px 30px; border: none; border-radius: 50px; font-size: 18px; margin: 20px 0; cursor: pointer; width: 100%; }
        .btn:hover { background: #C08A80; }
        .result-card { background: white; padding: 20px; border-radius: 15px; margin: 20px 0; box-shadow: 0 4px 10px rgba(0,0,0,0.1); text-align: center; }
        .season { font-size: 24px; font-weight: bold; color: #D4A59A; margin: 10px 0; }
        .upload-area { border: 2px dashed #D4A59A; padding: 40px; text-align: center; border-radius: 10px; margin: 20px 0; }
    </style>
</head>
<body>
    <div class="header">
        <h1>色語 ColorWhisper</h1>
        <p>找到專屬於你的和諧色彩</p>
    </div>

    <div class="container" id="app">
        <!-- 步驟 1: 首頁 -->
        <div id="home">
            <h2>AI 一鍵色彩鑒定</h2>
            <p>上傳一張清晰的自拍照，讓 AI 幫你找到最顯白的色盤。</p>
            <button class="btn" onclick="showUpload()">開始測試</button>
        </div>

        <!-- 步驟 2: 上傳頁 -->
        <div id="upload" style="display:none;">
            <h2>上傳照片</h2>
            <div class="upload-area">
                <p>📸 點擊下方按鈕模擬上傳</p>
                <button class="btn" onclick="showResult()">選擇照片 (模擬)</button>
            </div>
            <p><small>建議：請在自然光下拍攝，勿化濃妝</small></p>
        </div>

        <!-- 步驟 3: 結果頁 -->
        <div id="result" style="display:none;">
            <h2>鑒定結果</h2>
            <p>根據分析，你是屬於以下色彩季型：</p>
            
            <div class="result-card">
                <h3>春季型 (Warm & Bright)</h3>
                <p class="season">暖調 · 明亮</p>
                <p><strong>推薦色系：</strong>珊瑚粉、檸檬黃、淺鵝黃</p>
                <p><strong>避雷色系：</strong>深灰色、冷調的螢光色</p>
            </div>

            <button class="btn" onclick="showUpload()">重新測試</button>
        </div>
    </div>

    <script>
        // 簡單的頁面切換模擬
        function showUpload() {
            document.getElementById('home').style.display = 'none';
            document.getElementById('upload').style.display = 'block';
            document.getElementById('result').style.display = 'none';
        }
        function showResult() {
            document.getElementById('upload').style.display = 'none';
            document.getElementById('result').style.display = 'block';
        }
    </script>
</body>
</html>
