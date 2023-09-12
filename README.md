# Earth
#the earth, sun and moon
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body{
            margin: 0px;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: black;
            overflow: hidden;
            font-family: sans-serif;
            color: white;
        }
        .cantanier{
            font-size: 10px;
            width: 40em;
            height: 40em;
            position: relative;
        }
        .sun{
            position: absolute;
            top: 15em;
            left: 15em;
            width: 10em;
            height: 10em;
            background-color: rgb(255, 170, 0);
            border-radius: 50%;
            box-shadow: 0 0 3em white;
        }
        .earth,
        .moon {
            position: absolute;
            border-style: solid;
            border-color: white transparent transparent transparent;
            border-width: 0.1em 0.1em 0 0;
            border-radius: 50%;
        }

        .earth{
            top: 5em;
            left: 5em;
            width: 30em;
            height: 30em;
            animation: orbit 36.5s linear infinite;
            /* display: flex; */
        }
        .moon{
            top: 0;
            right: 0;
            width: 8em;
            height: 8em;
            animation: orbit 3s linear infinite;
        }
        .earth::before,
        .moon::before{
            content: "";
            position: absolute;
            border-radius: 50%;

        }

        .earth::before {
            top: 2.8em;
            right: 2.8em;
            width: 3em;
            height: 3em;
            box-shadow: 0 0 5px white;
            /* background-color: rgb(0, 255, 30); */
            background: linear-gradient(100deg, #00c3ff, #33ff00);

        }
        .moon::before{
            top: 0.8em;
            right: 0.2em;
            width: 1,2em;
            height: 1.2em;
            background-color: silver;
        }
        @keyframes orbit {
            to {
                transform: rotate(360deg);
            }
        }
    </style>
    <title>Document</title>
</head>
<body>
    <div class="cantanier">
        <div class="sun"></div>
        <div class="earth">
            <div class="moon"></div>
        </div>
    </div>
</body>
</html>
