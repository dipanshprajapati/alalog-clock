# alalog-clock
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>analog clock</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
      
    <div class="clock">
    <div class="numbers">
        <div class="circle" id="sec" style="--clr:red;"><i></i></div>
        <div class="circle" id="min" style="--clr:skyblue;"><i></i></div>
        <div class="circle" id="hrs" style="--clr:yellow;"><i></i></div>
        <span style="--i:0;"><b>12</b></span>
        <span style="--i:1;"><b>1</b></span>
        <span style="--i:2;"><b>2</b></span>
        <span style="--i:3;"><b>3</b></span>
        <span style="--i:4;"><b>4</b></span>
        <span style="--i:5;"><b>5</b></span>
        <span style="--i:6;"><b>6</b></span>
        <span style="--i:7;"><b>7</b></span>
        <span style="--i:8;"><b>8</b></span>
        <span style="--i:9;"><b>9</b></span>
        <span style="--i:10;"><b>10</b></span>
        <span style="--i:11;"><b>11</b></span>
    </div>
    </div>
    <script>
        let hr = document.querySelector('#hrs');
        let mn = document.querySelector('#min');
        let sc = document.querySelector('#sec');
        
        setInterval(()=>{
        let day = new Date();
        let hh = day.getHours() * 30;
        let mm = day.getMinutes() * 6;
        let ss = day.getSeconds() * 6; 
           
        hr.style.transform =`rotatez(${hh+(mm/12)}deg)`; 
        mn.style.transform =`rotatez(${mm}deg)`;
        sc.style.transform =`rotatez(${ss}deg)`;
    })
        </script>
</body>
</html>
