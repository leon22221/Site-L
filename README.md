<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Punkte anzeigen</title>
</head>
<body>
    <h1>Leons Statistiken</h1>
    <p>Deine Punkte sind: <span id="punkte">0</span></p>
    <p>Erledigte Aufgaben: <span id="ErlAuf">0</span></p>
    <p>Status: <span id="status">N/A</span></p> <!-- Hier wird der Status angezeigt -->
    <p>Free Tickets: <span id="freeTickets">0</span></p>

    <script>
        // JavaScript-Code, um Punkte aus dem Local Storage abzurufen und anzuzeigen
        const gespeichertePunkte = localStorage.getItem("punkte");
        if (gespeichertePunkte) {
            document.getElementById("punkte").textContent = gespeichertePunkte;
        }
        const ErledigteAufgaben = localStorage.getItem("ErlAuf");
        if (ErledigteAufgaben) {
            document.getElementById("ErlAuf").textContent = ErledigteAufgaben;
        }
        // JavaScript-Code, um den Status und Free Tickets aus der URL abzurufen und anzuzeigen
        const urlParams = new URLSearchParams(window.location.search);
        const status = urlParams.get('status');
        const freeTickets = urlParams.get('free_tickets');
        if (status) {
            document.getElementById("status").textContent = status === 'not_completed' ? 'Nicht erledigt' : 'Erledigt';
        }
        if (freeTickets) {
            document.getElementById("freeTickets").textContent = freeTickets;
        }
    </script>
</body>
</html>
