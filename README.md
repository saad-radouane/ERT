# ERT

# ETR – Emergency Trail Rescue

**ETR** is an integrated outdoor safety and ecosystem management platform. It helps hikers and trail runners move safely, even without cellular coverage, and gives park managers and rescue organizations a real-time view of trail conditions.

> **Project status:** this repository contains a **frontend prototype**. GPS, sensors, the offline mesh, AI analysis and notifications are **simulated** for demonstration purposes. Do not rely on the app as your only safety tool in the mountains.

## The Problem

People on remote trails often run into dangerous situations: a collapsed bridge, a landslide, a wasp nest, or unmarked snow and ice. Existing apps show static maps or unverified, often outdated user comments. Without signal, there is no way to call for help. Park managers, meanwhile, rely on slow, expensive, reactive manual inspections.

## The Solution

ETR combines three technologies:

- **Automated validation via Computer Vision.** A hiker photographs a hazard; the AI model classifies its type and severity and pins the GPS coordinates. If subsequent hikers pass the spot without re-flagging it, the report expires and is removed automatically.
- **Offline mesh and passive safety.** Hazard updates sync device-to-device when hikers pass each other, with no network needed. A clip-on wearable sensor detects falls and starts a countdown with a high-frequency alert and a voice check-in ("Are you okay?"). If there is no response, an SOS is sent with the GPS coordinates.
- **B2B/B2G dashboard for public bodies.** National parks, local councils and organizations such as the CAI receive a real-time heatmap of verified trail damage. They can post official status updates and prioritize repairs, cutting unnecessary physical patrols.

The project is aligned with **SDG 13 (Climate Action)**: it eliminates paper maps, helps prevent soil erosion and optimizes park maintenance while keeping visitors safe in real time.

## Target Users

- **Hikers:** route planning with predictive risk scores, offline hazard sync and hands-free safety checks.
- **Trail runners:** warnings about ice, rockfalls and solo falls, without stopping to check a phone.
- **Environmental protection personnel:** trail management based on verified data, with fewer inspections and more targeted interventions.

## Prototype Features

| Screen | Description |
|---|---|
| **Home** | Greeting, weather, mesh network status (nearby devices and synced reports), and routes rated low or high risk. |
| **Map** | Trail map showing reported hazards. |
| **Report** | Hazard reporting: choose a type, take a photo, and run a simulated AI analysis with GPS coordinates. |
| **Safety** | Safety status, clip sensor settings, emergency contacts, and a simulated fall with voice check-in and SOS. |
| **Dashboard** | Public-body view: heatmap of critical issues, active hiker count and official updates. |

## Repository Structure

```
.
├── index.html   # Complete prototype (HTML, CSS and JavaScript in one file)
└── README.md
```

## Running the Prototype

No dependencies or build step are required:

1. Download or clone the repository.
2. Open `index.html` in a modern browser.
3. To test on a smartphone, serve the folder with a local server (for example `npx serve .`) and open the address on the device, or use your browser's mobile device emulation.

The prototype loads **Inter** (Google Fonts) and **Font Awesome 6.5.1** from CDNs, so an internet connection is needed for the full styling.

## Known Limitations

- No backend: reports and data are stored only in the browser's `localStorage`.
- AI analysis, fall detection, offline mesh and GPS positioning are simulated.
- Values such as AI confidence, device counts and active hikers are randomly generated.

## Roadmap

- Integration of a real Computer Vision model for hazard classification.
- Device-to-device mesh synchronization protocol (BLE or similar).
- Predictive risk engine based on weather, slope and terrain data.
- Backend with authentication for the public-body dashboard.
- Integration with existing apps (Strava, Komoot, AllTrails, Wikiloc) or standalone use.
- Development of the wearable clip and real-world testing with experienced hikers and trail runners.

## License

To be defined.

## Team

Developed as part of a university course (Group04). Add names and contacts.
