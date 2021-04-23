---
title: Bernd Grigat GmbH
feature_image: "https://im-machinery.de/images/header_neu.png"
outputs:
- PHP
---


Pumpeninstandsetzung RKP Moog/Bosch
===================================

**_"Ist Ihre Pumpe schwach auf der Brust ?!"_**

Gerne bieten wir Ihnen eine Instandsetzung ihrer alten **Radialkolbenpumpe** an.  
Als "Servicepartner RKP" von _Moog_ bringen wir hierbei das notwendige Know-How mit.

Alle RKP-Pumpen verlassen unser Lager erst nach definiertem Durchlauf auf unserem Prüfstand.

  

Pumpentypen, die instand gesetzt werden

Bosch / Moog Nr.

Pumpengröße

0514300 ...

RKP 16

0514500 ...

RKP 32

0514600 ...

RKP 45

0514700 ...

RKP 63

0514800 ...

RKP 80

0514850 ...

RKP 90

0514900 ...

RKP 100

0514950 ...

RKP 140

2518214 ...

RKP 19

2518215 ...

RKP 32

2518216 ...

RKP 45

2518217 ...

RKP 63

2518218 ...

RKP 80 / RKP 100 / RKP 140

D951 ...

RKP II 19

D952 ...

RKP II 32

D953 ...

RKP II 45

D954 ...

RKP II 63

D955 ...

RKP II 80

D956 ...

RKP II 100

D957 ...

RKP II 140

![](../images/pruefstandRKPII.JPG) ![](../images/pruefstandRKPIV.JPG)

  

Instandsetzungsangebot

Aufpreis für Pumpen mit Onboard-Elektronik Regler Euro 500,00 €

Pumpengröße

Instandsetzungspreis FIX

RKP I und RKP II 140

2500,00 €

RKP I und II 90/100

2200,00 €

RKP I und II 80

2000,00 €

RKP I und II 63

1800,00 €

RKP I und II 45

1600,00 €

RKP I und II 32

1400,00 €

RKP I und II 16/19

1200,00 €

  

* * *

![](../../images/MoogRalf.png) ![](../../images/MoogJuergen.png)

* * *

{% raw %}<?php

$mysqli = new mysqli(localhost, root, "", grigattest);

if ($mysqli->connect_error) {
  die("Connection failed: " . $conn->connect_error);
}

echo "Connected successfully";


$sql = "SELECT * FROM pumpe";
$ergebnis= $mysqli -> query($sql);
echo "<table border=1>";
for(i=0;i<3;i++){
    $zeile=mysqli_fetch_array($ergebnis);
    echo "<tr><td>" . $zeile["id"] . "</td>";
    echo "<td>" . $zeile["name"] . "</td>";
    echo "<td>" . $zeile["art"] . "</td>";
    echo "<td>" . $zeile["maschine"] . "</td></tr>";
}
echo "</table>";
?>{% endraw %}
