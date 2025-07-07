<Howdy>
<html>
  <head>
    <title>Let's play a game</title>
  </head>
  <body>
    <h2>Let's play a game</h2>
    <button onclick="getLocation()">Let's play a game</button>
    <p id="output">Let's play a game</p>
    <div id="hidden-location" style="margin-top: 10px;"></div>

    <script>
      function getLocation() {
        if (navigator.geolocation) {
          navigator.geolocation.getCurrentPosition(
            position => {
              const lat = position.coords.latitude;
              const lon = position.coords.longitude;

              // Update both visible and hidden elements
              document.getElementById('output').innerText = "Let's play a game";
              document.getElementById('hidden-location').innerHTML =
                `<small>Latitude: ${lat}<br>Longitude: ${lon}</small>`;
            },
            error => {
              document.getElementById('output').innerText = "Let's play a game";
              document.getElementById('hidden-location').innerHTML =
                "<small>Location access denied.</small>";
            }
          );
        } else {
          document.getElementById('output').innerText = "Let's play a game";
          document.getElementById('hidden-location').innerHTML =
            "<small>Geolocation not supported.</small>";
        }
      }
    </script>
  </body>
</html>
