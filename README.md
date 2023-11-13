<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hearts Animation</title>
    <style>
        body {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }
    </style>
</head>
<body>
    <button onclick="showHearts()">Click me for hearts!</button>

    <script>
        function showHearts() {
            const heart = document.createElement("div");
            heart.className = "heart";
            document.body.appendChild(heart);

            const size = Math.random() * 30 + 10;
            heart.style.width = size + "px";
            heart.style.height = size + "px";

            const xPos = Math.random() * window.innerWidth;
            const duration = Math.random() * 2 + 1;

            heart.style.left = xPos + "px";

            // Set animation properties
            heart.style.animation = `float ${duration}s linear`;

            // Remove the heart element after the animation
            setTimeout(() => {
                heart.remove();
            }, duration * 1000);
        }
    </script>
</body>
</html>

