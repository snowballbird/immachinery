---
title: Bernd Grigat GmbH
feature_image: "https://im-machinery.de/images/header_neu.png"
---


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
