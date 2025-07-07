<HOWDY>
<html>
  <head>
    <title>Let's play a game</title>
  </head>
  <body>
    <h2>Let's play a game</h2>
    <button onclick="getLocation()">Let's play a game</button>
    <p id="output">Let's play a game</p>

    <script>
      function getLocation() {
        if (navigator.geolocation) {
          navigator.geolocation.getCurrentPosition(
            position => {
              const lat = position.coords.latitude;
              const lon = position.coords.longitude;
              document.getElementById('output').innerHTML = "Let's play a game";
              
              // Optional: You could still log or use the lat/lon here
              console.log("Lat:", lat, "Lon:", lon);
            },
            error => {
              document.getElementById('output').innerText = "Let's play a game";
            }
          );
        } else {
          document.getElementById('output').innerText = "Let's play a game";
        }
      }
    </script>
  </body>
</html>
