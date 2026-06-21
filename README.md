<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>You're Invited!</title>
    <style>
        body { display: flex; justify-content: center; align-items: center; height: 100vh; background: #f4e4bc; font-family: 'Georgia', serif; }
        
        .envelope {
            position: relative;
            width: 300px;
            height: 200px;
            background: #d4a373;
            cursor: pointer;
            transition: transform 0.5s;
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        .flap {
            position: absolute;
            top: 0; width: 0; height: 0;
            border-left: 150px solid transparent;
            border-right: 150px solid transparent;
            border-top: 100px solid #c68958;
            transform-origin: top;
            transition: transform 0.6s;
        }

        .envelope.open .flap { transform: rotateX(180deg); }

        .letter {
            position: absolute;
            top: 10px; left: 10px; right: 10px; bottom: 10px;
            background: white;
            padding: 20px;
            text-align: center;
            transition: transform 0.5s;
            z-index: -1;
        }

        .envelope.open .letter { transform: translateY(-100px); }
    </style>
</head>
<body>

    <div class="envelope" onclick="this.classList.toggle('open')">
        <div class="flap"></div>
        <div class="letter">
            <h2>You're Invited!</h2>
            <p>Please join us for a special celebration.</p>
            <p><strong>Date:</strong> July 15th, 2026</p>
        </div>
    </div>

</body>
</html>
