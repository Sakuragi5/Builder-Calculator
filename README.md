<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Builder Calculator</title>
    <meta name="description" content="Enterprise plan quotation calculator with multi-plan PDF generation.">
    
    <!-- Favicon: calculator emoji (loaded from emojiapi.dev as PNG) -->
    <link rel="icon" type="image/png" href="https://emojiapi.dev/api/v1/1F9EE/512.png">
    <link rel="apple-touch-icon" href="https://emojiapi.dev/api/v1/1F9EE/512.png">
    
    <!-- Open Graph (link previews in WhatsApp, Telegram, iMessage, etc.) -->
    <meta property="og:title" content="Builder Calculator">
    <meta property="og:description" content="Enterprise plan quotation calculator with multi-plan PDF generation.">
    <meta property="og:type" content="website">
    <meta property="og:site_name" content="Builder Calculator">
    <meta property="og:image" content="https://emojiapi.dev/api/v1/1F9EE/512.png">
    <meta name="twitter:card" content="summary">
    <meta name="twitter:title" content="Builder Calculator">
    <meta name="twitter:description" content="Enterprise plan quotation calculator.">
    <meta name="twitter:image" content="https://emojiapi.dev/api/v1/1F9EE/512.png">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html, body { 
            width: 100%; 
            height: 100%; 
            overflow: hidden; 
            background: #ffffff;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
        }
        iframe {
            width: 100%;
            height: 100%;
            border: none;
            display: block;
            position: absolute;
            top: 0;
            left: 0;
        }
        #loader {
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background: #ffffff;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            gap: 18px;
            z-index: 9999;
            transition: opacity 0.4s ease;
        }
        #loader.hidden { opacity: 0; pointer-events: none; }
        .spinner {
            width: 48px;
            height: 48px;
            border: 4px solid rgba(255,107,0,0.2);
            border-top-color: #ff6b00;
            border-radius: 50%;
            animation: spin 0.8s linear infinite;
        }
        #loader-text {
            color: #ff6b00;
            font-size: 14px;
            font-weight: 600;
            letter-spacing: 0.5px;
        }
        #loader-subtext { color: #888; font-size: 11px; margin-top: 4px; }
        @keyframes spin { to { transform: rotate(360deg); } }
    </style>
</head>
<body>
    <div id="loader">
        <div class="spinner"></div>
        <div id="loader-text">Loading Builder Calculator...</div>
        <div id="loader-subtext">Enterprise Plan Quotation Builder</div>
    </div>
    <iframe 
        src="https://script.google.com/macros/s/AKfycbw4GYg5Slp6Ft6XmTXb5EmDz4v8yvjkR01BBvI6CWDrzw0hrSz8sp7bjif_wzSd3vmJeA/exec" 
        id="appFrame"
        allow="geolocation; camera; microphone; fullscreen; clipboard-read; clipboard-write"
        allowfullscreen
        allowusermedia
        onload="hideLoader()">
    </iframe>
    <script>
        function hideLoader() {
            var loader = document.getElementById('loader');
            if (loader) {
                loader.classList.add('hidden');
                setTimeout(function() { loader.style.display = 'none'; }, 400);
            }
        }
        setTimeout(hideLoader, 10000);
    </script>
</body>
</html>
