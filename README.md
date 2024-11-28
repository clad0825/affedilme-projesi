<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Parlayan Buton Oyunu</title>
    <style>
        body {
            background-color: black;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0;
            overflow: hidden;
        }
        #myButton {
            background-color: white;
            color: black;
            border: none;
            padding: 20px;
            font-size: 20px;
            cursor: pointer;
            box-shadow: 0 0 20px white;
            transition: box-shadow 0.3s;
        }
        #message {
            display: none;
            color: white;
            font-size: 24px;
            font-weight: bold;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
        }
    </style>
</head>
<body>
    <button id="myButton">Tıkla ve Kazan!</button>
    <div id="message"></div>

    <script>
        const button = document.getElementById("myButton");
        const message = document.getElementById("message");

        let moving = false;

        button.addEventListener('click', function() {
            if (moving) {
                message.innerText = "Tebrikler hayatımın anlamı, oyunu kazandın...ama umarım bunun yanında beni affetmişsindir 😟";
                message.style.display = "block";
            }
        });

        setTimeout(function() {
            moving = true;
            moveButton();
        }, 2000);

        function moveButton() {
            const x = Math.random() * (window.innerWidth - button.offsetWidth);
            const y = Math.random() * (window.innerHeight - button.offsetHeight);
            button.style.position = 'absolute';
            button.style.left = x + 'px';
            button.style.top = y + 'px';

            if (moving) {
                requestAnimationFrame(moveButton);
            }
        }
    </script>
</body>
</html>


bu kod tamamen clad0825'e aittir discord hesabı clad0825 instagram hesabı hz.clad olarak geçmektedir eğer bu kodu izinsiz kullanan olursa sonuçları olucağı konusunda herkesi uyarırım...kodumu alıp kullanabilirsiniz ama sizin olduğunu söylemeyin lütfen...sevgilerle!
