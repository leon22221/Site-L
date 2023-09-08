<html>
<head>
    <title>Punktezähler</title>
</head>
<body>
    <h1>Deine Statistiken</h1>
    <p>Du hast <span id="punkte">0</span> Punkte.</p>

    <script>
        // Überprüfen, ob es bereits gespeicherte Punkte gibt
        let gespeichertePunkte = localStorage.getItem("punkte");
        if (gespeichertePunkte === null) {
            gespeichertePunkte = 0;
        } else {
            gespeichertePunkte = parseInt(gespeichertePunkte);
        }

        // Funktion, um Punkte zu vergeben
        function vergebePunkte() {
            gespeichertePunkte += 10;
            // Die Punkte im HTML aktualisieren
            document.getElementById("punkte").textContent = gespeichertePunkte;
            // Die Punkte im localStorage speichern
            localStorage.setItem("punkte", gespeichertePunkte.toString());
        }

        // Die initialen Punkte im HTML anzeigen
        document.getElementById("punkte").textContent = gespeichertePunkte;
    </script>
</body>
</html>
