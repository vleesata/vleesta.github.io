<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>自由输入版-湿度计算器</title>
    <style>
        :root {
            --primary-color: #4a90e2;
            --bg-color: #f4f7f6;
        }

        body {
            font-family: 'PingFang SC', 'Microsoft YaHei', sans-serif;
            background-color: var(--bg-color);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
        }

        .container {
            background-color: #ffffff;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 8px 30px rgba(0,0,0,0.1);
            width: 90%;
            max-width: 380px;
        }

        h2 {
            text-align: center;
            color: #333;
            font-size: 1.4rem;
            margin-bottom: 25px;
        }

        .input-group {
            margin-bottom: 15px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #666;
            font-size: 0.9rem;
        }

        /* 改为 text 类型后，我们自定义样式 */
        input[type="text"] {
            width: 100%;
            padding: 12px;
            box-sizing: border-box;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 18px;
            outline: none;
            transition: border-color 0.3s;
        }

        input[type="text"]:focus {
            border-color: var(--primary-color);
        }

        .hint {
            font-size: 0.75rem;
            color: #999;
            margin-top: 4px;
        }

        button {
            background-color: var(--primary-color);
            color: white;
            border: none;
            padding: 14px;
            font-size: 1.1rem;
            border-radius: 8px;
            cursor: pointer;
            width: 100%;
            margin-top: 10px;
            font-weight: bold;
        }

        #result-area {
            margin-top: 20px;
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            background-color: #f8f9fa;
            display: none;
        }

        .rh-value {
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--primary-color);
            margin: 10px 0;
        }

        .status-msg {
            font-size: 0.85rem;
            color: #666;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>🌡️ 相对湿度计算器</h2>
    
    <div class="input-group">
        <label for="temp">当前温度 (°C)</label>
        <input type="text" id="temp" placeholder="支持负数，如 -5.2">
        <div class="hint">可输入负号和数字</div>
    </div>

    <div class="input-group">
        <label for="dew">露点温度 (°C)</label>
        <input type="text" id="dew" placeholder="支持负数，如 -10">
    </div>

    <button onclick="calculate()">点击计算</button>

    <div id="result-area">
        <div style="color: #888;">计算结果</div>
        <div class="rh-value" id="rh-output">--%</div>
        <div class="status-msg" id="status-msg"></div>
    </div>
</div>

<script>
    function calculate() {
        // 获取输入值
        let tempStr = document.getElementById('temp').value.trim();
        let dewStr = document.getElementById('dew').value.trim();

        // 转换为数字
        let T = parseFloat(tempStr);
        let Td = parseFloat(dewStr);

        // 验证输入是否合法
        if (isNaN(T) || isNaN(Td)) {
            alert("请输入正确的数字（例如：25 或 -10.5）");
            return;
        }

        // 计算逻辑
        let a, b, mode;
        if (T >= 0) {
            // 常温/高温环境（水面）
            a = 17.625;
            b = 243.04;
            mode = "💧 标准模式 (水面)";
        } else {
            // 零下环境（冰面）
            a = 21.875;
            b = 265.5;
            mode = "❄️ 低温模式 (冰面)";
        }

        let alphaT = (a * T) / (b + T);
        let alphaTd = (a * Td) / (b + Td);
        let rh = 100 * Math.exp(alphaTd - alphaT);

        // 逻辑处理：湿度不超100%
        if (Td > T) {
            rh = 100;
            mode = "⚠️ 露点高于温度（已饱和）";
        }
        if (rh > 100) rh = 100;

        // 显示结果
        const resultArea = document.getElementById('result-area');
        const output = document.getElementById('rh-output');
        const statusMsg = document.getElementById('status-msg');

        resultArea.style.display = 'block';
        output.innerText = rh.toFixed(1) + "%";
        statusMsg.innerText = mode;

        // 如果是零下，改变一下颜色提醒
        output.style.color = T < 0 ? "#00bcd4" : "#4a90e2";
    }
</script>

</body>
</html>
