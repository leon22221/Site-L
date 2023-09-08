<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Punkte anzeigen</title>
</head>
<body>
    <h1>Leons Statistiken</h1>
    <p>Deine Punkte sind: <span id="gesammeltePunkte">0</span></p>
    <p>Erledigte Aufgaben: <span id="ErledigteAufgaben">0</span></p>

    <script>
        // JavaScript-Code, um Punkte aus dem Local Storage abzurufen und anzuzeigen
        const gespeichertePunkte = localStorage.getItem("punkte");
        if (gespeichertePunkte) {
            document.getElementById("gesammeltePunkte").textContent = gespeichertePunkte;
        }
                const ErledigteAufgaben = localStorage.getItem("ErlAuf");
        if (ErledigteAufgaben) {
            document.getElementById("ErledigteAufgaben").textContent = ErledigteAufgaben;
        }
    </script>
</body>
</html>

