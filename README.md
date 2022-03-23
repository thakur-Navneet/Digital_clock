<!--
√√√√√••••⏲️Led Digital Clock⏲️••••√√√√√√√


√      ----------------------------     √


√√√√√√√√√••••••• Navneet Thakur •••••••√√√√√√√√√
-->
<!DOCTYPE html>
<html>
    <head>
    <meat charset="UFT-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=Edge">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
    <link rel="stylesheet" media="screen" href="https://fontlibrary.org/face/segment7" type="text/css"/>
        <title>LED DIGITAL CLOCK🚨⏰</title>
    <style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400&display=swap');
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}
.container{
    width:100%;
    height:100vh;
    background:#252525 url(https://cdn.commaful.com/media/public/images/ead73399-92ad-5172-ed3f-aa04bfdac6d1-1608069382912.gif);
    background-position:center;
    background-size:cover;
}
.clock_container{
    width:100%;
    height:100%;
    display:flex;
    align-items:center;
    justify-content:center;
}
.clock{
    width:280px;
    height:auto;
    padding:20px;
    border:2px solid #7AD30C;
    border-radius:20px;
    box-shadow:5px 5px 15px #01D610, -5px -5px 15px #01D610, inset 3px 3px 5px #25FF1D, inset -3px -3px 5px #25FF1D;
    backdrop-filter:blur(5px);
}
.day{
    margin-top:15px;
    font-size:25px;
    font-family:'Orbitron', sans-serif;
    color:#000;
    font-weight:bolder;
    text-shadow:1px 1px 5px #25FF1D, -1px -1px 5px #76FF8C;
}
.time{
    font-size:55px;
    color:#76FF8C;
    text-shadow:0 0 4px #76FF8C,
                0 0px 0 #76FF8C,
                0 0 80px #76FF8C;
    font-family: 'Segment7Standard';
    margin:10px;
    margin-top:15px;
    margin-left:-50px;
}
.am_pm{
    float:right;
    position:relative;
    margin-top:-70px;
    font-size:15px;
    font-family:'Orbitron', sans-serif;
    color:#76FF8C;
    text-shadow:2px 2px 5px #25FF1D, -2px -2px 5px #76FF8C;
}
.timec{
    width:280px;
    height:auto;
    display:flex;
    align-items:center;
    justify-content:center;
}
.date{
    font-size:25px;
    color:#000;
    font-family:'Orbitron', sans-serif;
    font-weight:bolder;
    margin-top:5px;
    text-shadow:1px 1px 5px #25FF1D, -1px -1px 5px #76FF8C;
}
.seconds{
    float:right;
    position:relative;
    margin-top:-45px;
    font-size:20px;
    color:#76FF8C;
    text-shadow:2px 2px 5px #25FF1D, -2px -2px 5px #76FF8C;
    font-family: 'Segment7Standard';
}
.learnc{
    width:100%;
    position:absolute;
    bottom:0;
    height:80px;
    display:flex;
    align-items:center;
    justify-content:center;
}
.learnc button{
    padding:10px;
    border:2px solid #01D811;
    color:#fff;
    text-shadow:1px 1px 5px #25FF1D, -1px -1px 5px #76FF8C;
    border-radius:10px;
    background:transparent;
    width:200px;
    box-shadow:inset 3px 3px 5px #25FF1D, inset -3px -3px 5px #25FF1D;
}
.learnc button:active{
    box-shadow:inset 1px 1px 5px #25FF1D, inset -1px -1px 5px #25FF1D;
}
.battery{
    color:#76FF8C;
    float:right;
    margin-top:-10px;
    margin-right:-5px;
}
.nb{
    font-family:'Orbitron', sans-serif;
    font-size:11px;
    font-weight:bolder;
    padding:3px;
}
.fa-youtube{
    margin:0 5px;
}
	</style>
	<script>
function time(){
    var date = new Date();
    var HH = date.getHours();
    var MM = date.getMinutes();
    var SS = date.getSeconds();
    var dates = date.getDate();
    var year = date.getFullYear();
    if (HH>=12){
    $(".am_pm").html("PM");
    HH=HH-12;
    }else if (HH==0){
        $(".am_pm").html("AM");
        HH=HH+12;
    }else{
        $(".am_pm").html("AM");
        HH=HH;
    }
    HH = (HH < 10) ? "0" + HH : HH;
    MM = (MM < 10) ? "0" + MM : MM;
    SS = (SS < 10) ? "0" + SS : SS;
    var HM = HH+":"+MM;
    $(".time").html(HM);
    $(".seconds").html(SS);
    var monthList = [
    "JAN",
    "FEB",
    "MAR",
    "APR",
    "MAY",
    "JUN",
    "JUL",
    "AUG",
    "SEP",
    "OCT",
    "NOV",
    "DEC"
    ];
    var dayList = [
    "SUNDAY",
    "MONDAY",
    "TUESDAY",
    "WEDNESSDAY",
    "THURSDAY",
    "FRIDAY",
    "SATURDAY"
    ];
    var MN = monthList[date.getMonth()];
    var DYS = dayList[date.getDay()];
    $(".day").html(DYS);
    $(".date").html(dates+" "+MN+" "+year);
    MM=setTimeout(time, 1000);
    }
var audio = new Audio();

window.onclick=function(){
    audio.play();
    audio.loop=true;
}
var battery = navigator.getBattery();
battery.then(a);
function a(b){
    $(".nb").html(b.level*100+"%");
}	
	</script>
	
	</head>
<body onload="time()">
<div class="container">
	<div class="clock_container">
		<div class="clock">
		<div class="battery"><i class="fa fa-battery"></i><span class="nb">100%</span>
		</div>
		<center>
			<div class="day">SUNDAY</div>
			<div class="timec">
				<div class="time">05:00</div>
			</div>
		</center>
		<div class="am_pm">AM</div>
		<div class="seconds">01</div>
		<center>
			<div class="date">20 MARCH 2022</div>
		</center>
		</div>
	</div>
</div>
</body>
</html>
