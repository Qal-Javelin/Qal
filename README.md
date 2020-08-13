# Qal
<!DOCTYPE html>
<html>
 
<head>
    <title>Calculator</title>
    <link rel="stylesheet" type="text/css" href="design.css">
</head>
<script type="text/javascript"> 
    function myclick(a) {
        myform.display.value += a;
    }
 
    function equal() {
        myform.display.value = eval(myform.display.value);
    }
 
    function ans() {
        var preans = myform.display.value;
        myform.display.value = preans.substr(0, preans.eval - 1);
    }
 
    function ac() {
        myform.display.value = '';
    }
 
    function backspace() {
        var prevalue = myform.display.value;
        myform.display.value = prevalue.substr(0, prevalue.length - 1);
    }
 
    function fsin() {
        myform.display.value = Math.sin(myform.display.value);
    }
 
    function fcos() {
        myform.display.value = Math.cos(myform.display.value);
    }
 
    function ftan() {
        myform.display.value = Math.tan(myform.display.value);
    }
 
    function fsqr() {
        myform.display.value = Math.pow(myform.display.value, 2);
    }
 
    function fsqrt() {
        myform.display.value = Math.pow(myform.display.value, 1 / 2);
    }
 
    function ffact() {
        var n = myform.display.value;
        if (n == 0 || n == 1) {
            myform.display.value = 1;
        } else {
            let total = 0,
                count = 1;
            while (count <= n) {
                total = (count - 1) * count;
                count += 1;
            }
            myform.display.value = total;
        }
    }
 
    function fabs() {
        var n = myform.display.value;
        if (n > 0) {
            myform.display.value = n;
        } else {
            myform.display.value = -n;
        }
    }
 
    function fp1() {
        var n = myform.display.value;
        myform.display.value = 1 / n;
    }
 
    function fcomb() {
        var x, y = myform.display.value;
        myform.display.value = x * y;
    }
 
    function fln() {
        myform.display.value = Math.log(myform.display.value);
    }
 
    function flog() {
        myform.display.value = Math.log(myform.display.value, exp);
    }
 
    function fexp() {
        myform.display.value = Math.exp(myform.display.value);
    }
 
    function pi() {
        var n = myform.display.value;
        myform.display.value = n * 22 / 7;
    }
    function facos() {
        myform.display.value = Math.acos(myform.display.value);
    }
    function fasin() {
        myform.display.value = Math.asin(myform.display.value);
    }
    function fatan() {
        myform.display.value = Math.atan(myform.display.value);
    }
</script>
 
<body>
    <div class="main">
        <form name="myform">
            <input type="text" name="display" class="textview"><br>
        </form>
        <table>
            <tr>
                <td><input type="button" class="btn symbol" value="x^-1" onclick="fp1()"></td>
                <td><input type="button" class="btn symbol" value="nCr" onclick="fcomb()"></td>
                <td><input type="button" class="btn symbol" value="ln" onclick="fln()"></td>
                <td><input type="button" class="btn symbol" value="log" onclick="flog()"></td>
                <td><input type="button" class="btn symbol" value="Abs" onclick="fabs()"></td>
            </tr>
            <tr>
                    <td><input type="button" class="btn symbol" value="tan'" onclick="fatan()"></td>
                    <td><input type="button" class="btn symbol" value="cos'" onclick="facos()"></td>
                    <td><input type="button" class="btn symbol" value="sin'" onclick="fasin"></td>
                    <td><input type="button" class="btn symbol" value="log" onclick="flog()"></td>
                    <td><input type="button" class="btn symbol" value="Abs" onclick="fabs()"></td>
                </tr>
            <tr>
                <td><input type="button" class="btn symbol" value="!" onclick="ffact()"></td>
                <td><input type="button" class="btn symbol" value="(" onclick="myclick('(')"></td>
                <td><input type="button" class="btn symbol" value=")" onclick="myclick(')')"></td>
                <td><input type="button" class="btn symbol" value="pi" onclick="pi()"></td>
                <td><input type="button" class="btn symbol" value="e" onclick="fexp()"></td>
            </tr>
            <tr>
                <td><input type="button" class="btn symbol" value="sin" onclick="fsin()"></td>
                <td><input type="button" class="btn symbol" value="cos" onclick="fcos()"></td>
                <td><input type="button" class="btn symbol" value="tan" onclick="ftan()"></td>
                <td><input type="button" class="btn symbol" value="x^2" onclick="fsqr()"></td>
                <td><input type="button" class="btn symbol" value="sqrt" onclick="fsqrt()"></td>
            </tr>
            <tr>
                <td><input type="button" class="btn number" value="9" onclick="myclick('9')"></td>
                <td><input type="button" class="btn number" value="8" onclick="myclick('8')"></td>
                <td><input type="button" class="btn number" value="7" onclick="myclick('7')"></td>
                <td><input type="button" class="btn symbol" value="Del" onclick="backspace()"></td>
                <td><input type="button" class="btn symbol" value="AC" onclick="ac()"></td>
            </tr>
            <tr>
                <td><input type="button" class="btn number" value="6" onclick="myclick('6')" </td>
                    <td><input type="button" class="btn number" value="5" onclick="myclick('5')"></td>
                    <td><input type="button" class="btn number" value="4" onclick="myclick('4')"></td>
                    <td><input type="button" class="btn symbol" value="-" onclick="myclick('-')"></td>
                    <td><input type="button" class="btn symbol" value="+" onclick="myclick('+')"></td>
            </tr>
            <tr>
                <td><input type="button" class="btn number" value="3" onclick="myclick('3')"></td>
                <td><input type="button" class="btn number" value="2" onclick="myclick('2')"></td>
                <td><input type="button" class="btn number" value="1" onclick="myclick('1')"></td>
                <td><input type="button" class="btn symbol" value="x" onclick="myclick('*')"></td>
                <td><input type="button" class="btn symbol" value="/" onclick="myclick('/')"></td>
            </tr>
            <tr>
                <td><input type="button" class="btn symbol" value="." onclick="myclick('.')"></td>
                <td><input type="button" class="btn number" value="0" onclick="myclick('0')"></td>
                <td><input type="button" class="btn symbol" value="," onclick="myclick(',')"></td>
                <td><input type="button" class="btn symbol" value="Ans" onclick="Ans()"></td>
                <td><input type="button" class="btn symbol" value="=" onclick="equal()"></td>
            </tr>
        </table>
    </div>
</body>
 
</html>

