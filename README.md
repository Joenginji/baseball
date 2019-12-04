<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>

<body>

    <script>

        document.write("<br> 신나는 야구게임!" + "<br> 첫 번째 타자가 타석에 입장했습니다.");

        var strike = 0;
        var ball = 0;
        var hit = 0;
        var out = 0;

        while (out != 3) {

            var random = Math.floor(Math.random() * 4);

            if (0 === random) {
                document.write("<br><br>스트라이크!");
                strike += 1;
                if (strike === 3) {
                    out = 1;
                }
            }
            else if (1 === random) {

                document.write("<br><br>볼!");
                ball += 1;
                if (ball === 4) {
                    hit = 1;
                }
            }

            else if (2 === random) {

                document.write("<br><br>안타! 다음 타자가 타석에 입장했습니다.");
                hit += 1;
                strike = 0;
                ball = 0;
            }

            else if (3 === random) {
                document.write("<br><br>아웃! 다음 타자가 타석에 입장했습니다.")
                out += 1;
                strike = 0;
                ball = 0;
            }
            document.write("<br>" + strike + "S " + ball + "B " + out + "O ");
        }
        document.write("<br><br>아웃!" + "<br>" + strike + "S " + ball + "B " + out + "O ");
        document.write("<br><br> 최종 안타수:" + hit + "<br> GAME OVER");


    </script>

</body>

</html>
