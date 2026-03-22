# 🌤️ IoT Weather Monitoring Portal

A lightweight, browser-based IoT dashboard for real-time weather monitoring. Built with pure HTML, CSS, and JavaScript — no frameworks required.

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat&logo=chartdotjs&logoColor=white)

---

## ✨ Features

- **Live Weather Data** — Fetches real-time temperature and wind speed every 5 seconds via the [Open-Meteo API](https://open-meteo.com/)
- **Live Line Chart** — Scrolling temperature history chart powered by Chart.js (last 10 readings)
- **Device Status Panel** — Simulates 3 IoT device readings (temperature, wind speed, connection status)
- **Animated Sky Background** — CSS-animated clouds for a clean atmospheric UI
- **Dark/Light Theme Toggle** — Switch between sky-blue and dark backgrounds
- **Multi-page Navigation** — Dashboard, Devices, and Settings pages via sidebar

---

## 📸 Pages

| Page | Description |
|------|-------------|
| **Dashboard** | Live temperature & wind speed cards + scrolling chart |
| **Devices** | Simulated IoT device data feed |
| **Settings** | Theme toggle control |

---

## 🚀 Getting Started

No installation or build step needed.

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/iot-weather-portal.git
   cd iot-weather-portal
   ```

2. **Open in your browser**
   ```bash
   open index.html
   ```
   Or simply double-click `index.html`.

> ⚠️ If your browser blocks the API fetch due to CORS/mixed-content policies, serve the file via a local server:
> ```bash
> npx serve .
> # or
> python -m http.server 8080
> ```

---

## 🌐 API

Weather data is sourced from the free [Open-Meteo API](https://open-meteo.com/) — no API key required.

**Default location:** Thanjavur, Tamil Nadu, India (`lat: 10.79, lon: 79.13`)

To change the location, update the coordinates in `index.html`:

```javascript
const res = await fetch(
  "https://api.open-meteo.com/v1/forecast?latitude=YOUR_LAT&longitude=YOUR_LON&current_weather=true"
);
```

You can look up coordinates for any city at [latlong.net](https://www.latlong.net/).

---

## 📁 Project Structure

```
iot-weather-portal/
└── index.html      # All-in-one HTML, CSS, and JavaScript
```

---

## 🛠️ Built With

- **[Chart.js](https://www.chartjs.org/)** — Line chart for temperature history
- **[Open-Meteo API](https://open-meteo.com/)** — Free, no-auth weather data
- **Vanilla CSS** — Animated clouds, responsive layout, card components

---

## 🔧 Customization

| What | Where in `index.html` |
|------|----------------------|
| Change location | `latitude` and `longitude` in the fetch URL |
| Update interval | `setInterval(updateData, 5000)` — value is in milliseconds |
| Chart history length | `if (labels.length > 10)` — change `10` to keep more/fewer points |
| Cloud animation speed | `.cloud1`, `.cloud2`, `.cloud3` animation duration values |

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

