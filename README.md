<!DOCTYPE html>
<html>
<head>
    <title>Hello with Glow</title>
    <style>
        #text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-family: sans-serif;
            color: #fff;
            font-size: 5em;
            animation: glow 1s infinite alternate;
        }

        @keyframes glow {
            from {
                opacity: 0;
            }

            to {
                opacity: 1;
            }
        }
    </style>
</head>
<body>
    <div id="text">Hello</div>
</body>
</html>
