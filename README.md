<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<style>
    input{
        text-align: right;
        height: 40px;
        width: 20%;
    }

    #firstdiv{
        text-align: center;
    }

    #Clear{
        margin-left: 15.5%;
    }
    
    button{
        width: 50px;
        height: 40px;
        margin-bottom: 5px;
        background-color: white;
    }

    button:active{
        color: red;
    }



</style>

<body>

    <script src="calculator.js"></script>
    
    <div id="firstdiv">

        <h1>
        Calculator
        </h1>

        <div>
            <input type="text" name="" id="abc">
        </div><br>

        <div id="Clear">
            <button onclick="remove()">
                Clear
            </button>
        </div>

        <div>
            <button onclick="calculator(7)">
                7
            </button>
            <button onclick="calculator(8)">
                8
            </button>
            <button onclick="calculator(9)">
                9
            </button>
            <button onclick="calculator('*')">
                X
            </button>
        </div>

        <div>
            <button onclick="calculator(4)">
                4
            </button>
            <button onclick="calculator(5)">
                5
            </button>
            <button onclick="calculator(6)">
                6
            </button>
            <button onclick="calculator('-')">
                -
            </button>
        </div>

        <div>
            <button onclick="calculator(1)">
                1
            </button>
            <button onclick="calculator(2)">
                2
            </button>
            <button onclick="calculator(3)">
                3
            </button>
            <button onclick="calculator('+')">
                +
            </button>
        </div>

        <div>
            <button onclick="calculator('/')">
                /
            </button>
            <button onclick="calculator(0)">
                0
            </button>
            <button onclick="calculator('.')">
                .
            </button>
            <button onclick="equal()">
                =
            </button>
        </div>

    </div>

</body>
</html>







function calculator(a){
    var b = document.getElementById('abc')
    // = ye wale sighn se pehle jo mene + lagaya he iska matlab he concat karna matlab alaga karna aur duusra matlab shayad ye he ke jo sir ne bataya he ke pehli value ko to rehne dega aur duusri value ko concat karde ga
    b.value += a
}

function equal(){
    var c = document.getElementById('abc')
    // console.log(eval(c.value))
    c.value = eval(c.value)
}

function remove(){
    var d = document.getElementById('abc')
    d.value = ''
}

