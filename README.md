# pr-fziffer

<html><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <title>Prüfziffern EAN</title>
    
    <script>
        "use strict";

        
        function rechne(){

            var vErgebnis;
            var a=[1,3,1,3,1,3,1,3,1,3,1,3];
            var i=0;
            var check;
            var vPruefziffer;
            var vPruefsumme=0;
            var input= document.getElementById("idInput").value;
            var vAusgabe = "";
            

         
        
        
        
while(i<12){
vErgebnis = a[i]*input[i];
vPruefsumme = vPruefsumme + vErgebnis; 
i++;
}


vPruefziffer = 10-(vPruefsumme%10);
if(vPruefziffer == 10){vPruefziffer=0;}

if(vPruefziffer=0){check="true";}
else{check="false";}
vAusgabe = vAusgabe + check;

document.getElementById("idOutput").innerHTML= vAusgabe;

        }
    </script>
</head>

<body>
    <h1>Prüfziffer berechnen</h1>
    <input id="idInput" type="text" maxlength="12" size="10" value ="400999301020">
    <button onclick="rechne();">Berechne Prüfziffer!</button><br><br>
    <div id="idOutput"></div>

</body></html>
