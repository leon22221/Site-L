<html>
<head>
    <title>Punktevergabe</title>
</head>
<body>
    <h1>Leons Statistiken</h1>
    <p>Du hast <span id="punkte">0</span> Punkte.</p>

    <script>
        // Prüfe, ob der Benutzer bereits Punkte hat (beim Seitenaufruf)
        let startPunkte = parseInt(localStorage.getItem('punkte')) || 0;
        document.getElementById('punkte').textContent = startPunkte;
        
         document.getElementById('punkte').textContent = aktuellePunkte;
         
        // Rufe die Funktion punkteErhoehen auf, um beim Laden der Seite Punkte zu vergeben
    </script>
</body>
</html>
