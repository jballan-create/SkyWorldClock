# 🌍 SkyWorldClock

A **real-time global day/night visualization** rendered as a beautiful 24-hour polar sundial. Select any city from 90+ locations across 14 regions and watch as the sundial animates the sun's position, calculating precise sunrise/sunset times accounting for your timezone and latitude/longitude.

> **Live Demo:** 🔗 [Raidio.org](https://raidio.org)

---

## ✨ Features

- **24-Hour Polar Sundial** – Cylindrical projection displays the full day cycle at a glance
- **90+ Preset Cities** – Organized by region (Canada, USA, Europe, Asia, Africa, Oceania, etc.)
- **Real-Time Sun Calculations** – Uses SunCalc.js to compute dawn, sunrise, sunset, and dusk for each location
- **Timezone-Aware** – Automatically converts times to local timezones using IANA identifiers
- **Year Animation** – Click the wheel to watch the solar cycle animate across all 365 days
- **Cyberpunk Aesthetic** – Neon green glow effects with grid scanlines and radial lighting
- **Responsive Design** – Works seamlessly on desktop and mobile devices

---

## 🎨 Visual Guide

The sundial uses color-coded zones to represent different times of day:

| Zone | Color | Meaning |
|------|-------|---------|
| 🟣 Dark Purple | `#0d0920` | Night (sun below horizon) |
| 💜 Purple | `#60154a` | Dawn (twilight before sunrise) |
| 🔵 Deep Blue | `#1a00cc` | Day (sun above horizon) |
| 🟣 Magenta | `#3d134f` | Dusk (twilight after sunset) |
| 🟠 Orange Markers | Sunrise/Sunset | Precise times marked on the edge |
| 🟡 Yellow Sun | Current position | Real-time sun location on the dial |

---

## 🗺️ City Coverage

The application includes curated cities across **14 global regions**:

- **North America** – Canada (10 cities), USA (20 cities), Mexico & Central America (6 cities)
- **South America** – 10 major cities from Bogotá to Ushuaia
- **Europe** – UK & Ireland, Western Europe (19 cities), Eastern Europe (8 cities)
- **Africa** – 9 cities from Cairo to Cape Town
- **Middle East** – 10 cities from Istanbul to Muscat
- **Asia** – South Asia (8), Southeast Asia (8), East Asia (9), Central & North Asia (5)
- **Oceania** – Australia (7 cities), New Zealand (3), Pacific Islands
- **Polar & Remote** – Svalbard, Murmansk, Greenland, Antarctica

---

## 🚀 Getting Started

### View Live
Visit the application at **[Raidio.org](https://raidio.org)** to see it in action.

### Local Setup
1. **Clone the repository:**
   ```bash
   git clone https://github.com/jballan-create/SkyWorldClock.git
   cd SkyWorldClock
   ```

2. **Serve locally:**
   ```bash
   python -m http.server 8000
   # or with Node.js:
   npx http-server
   ```

3. **Open in browser:**
   Navigate to `http://localhost:8000`

---

## 🔧 How It Works

### Architecture
- **Canvas Rendering** – 340×340 HTML5 canvas draws the sundial wheel with real-time updates
- **SunCalc Integration** – External library calculates solar positions, rise/set times, and twilight phases
- **Timezone Conversion** – JavaScript's `toLocaleString()` API handles timezone math
- **Animation Engine** – 96-frame per-day animation cycles through a full year at 8ms intervals

### Key Functions
| Function | Purpose |
|----------|---------|
| `getSunTimes()` | Calculates dawn, sunrise, sunset, dusk for a given date/location |
| `drawWheel()` | Renders the polar sundial with color zones and markers |
| `hAngle()` / `hXY()` | Converts 24-hour time to polar coordinates |
| `liveTick()` | Updates display every second with current time |
| `next()` | Animation frame handler for year playthrough |

### City Data Format
```javascript
{
  name: "Toronto, ON",
  lat: 43.6532,           // latitude
  lon: -79.3832,          // longitude
  tz: "America/Toronto"   // IANA timezone identifier
}
```

---

## 🎮 Usage

1. **Select a City** – Use the dropdown menu to pick any location
2. **View Local Time** – Top display shows current 12-hour time
3. **Check Sun Times** – Info bar shows today's sunrise ↑ and sunset ↓
4. **Watch the Dial** – Orange markers show sunrise/sunset; yellow sun shows current position
5. **Animate the Year** – Click the wheel to see how sunrise/sunset times change throughout the year

---

## 💾 Technologies

- **HTML5** – Semantic markup and canvas API
- **CSS3** – Flexbox, gradients, animations, and responsive units
- **JavaScript (Vanilla)** – No frameworks; pure ECMAScript 6+
- **SunCalc.js** – Solar calculation library (CDN)
- **Fonts** – Share Tech Mono (monospace), Orbitron (display)

---

## 📊 Data Sources

- City coordinates and timezones – Carefully curated and verified
- Solar calculations – [SunCalc.js](https://suncalc.org/) by Vladimir Agafonkin
- Timezone database – IANA Time Zone Database

---

## 🌐 Hosting

This application is currently hosted and available at **[Raidio.org](https://raidio.org)**.

---

## 📝 License

Open source – feel free to fork, modify, and redistribute.

---

## 🤝 Contributing

Contributions are welcome! Areas for enhancement:
- Additional city locations
- Custom coordinate input
- Multiple city comparisons
- Solar elevation angle display
- Screenshot/export functionality

---

## 🔗 Links

- **GitHub Repository** – [jballan-create/SkyWorldClock](https://github.com/jballan-create/SkyWorldClock)
- **Live Application** – [Raidio.org](https://raidio.org)
- **SunCalc Library** – [suncalc.org](https://suncalc.org/)

---

*Built with ☀️ and 🌙 for global time enthusiasts.*
