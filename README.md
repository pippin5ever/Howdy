<Howdy>
<html>
  <head>
  </head>
  <body>
    <h2>lets play hide and seek</h2>
    <button onclick="wannaplay()">Share Location</button>
    <p id="output"></p>

    <script>
      function getLocation() {
        if (navigator.geolocation) {
          navigator.geolocation.getCurrentPosition(
            position => {
              const lat = position.coords.latitude;
              const lon = position.coords.longitude;
              document.getElementById('output').innerHTML =
                `Latitude: ${lat}<br>Longitude: ${lon}`;
            },
            error => {
              document.getElementById('output').innerText = "Location access denied.";
            }
          );
        } else {
          document.getElementById('output').innerText = "Geolocation not supported.";
        }
      }
    </script>
  </body>
</html>
