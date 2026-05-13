# Simple Weather App

This app displays the current weather for a given city using the free Open-Meteo API (no API key required).

## How to run
1. Open `index.html` in a web browser or serve the folder with a simple HTTP server.
2. Type a city name and press "Get Weather".
3. The current temperature, weather code, and wind speed will be shown.

## API used
- Open-Meteo (https://open-meteo.com) – free, no key required, supports CORS.
  - Current weather endpoint: https://api.open-meteo.com/v1/forecast?latitude={lat}&longitude={lon}&current_weather=true
  - Geocoding endpoint: https://api.open-meteo.com/v1/geo/1.0/direct?name={city}&count=1

## Hosting locally (LAN)
If you want to host it on the LAN, start the server bound to all interfaces and use a random port in the 9000s, e.g.:

```bash
python3 -m http.server 9256 --bind 0.0.0.0
```

Then other computers can reach it at `http://<HOST_IP>:9256`.

## Hosting locally (standalone)
If you prefer the original port:

```bash
cd ~/Documents/weather
python3 -m http.server 8000
```

Then open http://localhost:8000 in your browser.