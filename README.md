<html>
<head>
    <title>Punktevergabe</title>
</head>
<body>
    <h1>Leons Statistiken</h1>
    <p>Du hast <span id="punkte">0</span> Punkte.</p>

    <script>
        // Funktion, um die Punkte zu erhöhen
        function punkteErhoehen() {
            // Versuche, die aktuellen Punkte aus dem lokalen Speicher abzurufen
            let aktuellePunkte = parseInt(localStorage.getItem('punkte')) || 0;
            
            // Erhöhe die Punkte um 10
            aktuellePunkte += 10;

            // Speichere die aktualisierten Punkte im lokalen Speicher
            localStorage.setItem('punkte', aktuellePunkte);

            // Aktualisiere die Anzeige der Punkte auf der Seite
            document.getElementById('punkte').textContent = aktuellePunkte;
        }

        // Prüfe, ob der Benutzer bereits Punkte hat (beim Seitenaufruf)
        let startPunkte = parseInt(localStorage.getItem('punkte')) || 0;
        document.getElementById('punkte').textContent = startPunkte;
        
        // Rufe die Funktion punkteErhoehen auf, um beim Laden der Seite Punkte zu vergeben
        punkteErhoehen();
    </script>
</body>
</html>
