# meoSphere Constellation Simulator

Interactive Three.js visualization of a MEO satellite constellation with orbital planes, inter-satellite links (ISL), ground-to-satellite links (GSL), and coverage metrics.

**Live demo:** https://enriko-kroj.github.io/meosphere-constellation-demo/

## Run locally

**Option A — open directly:** open `index.html` in Chrome. Earth textures are embedded in `earth-day-jpg-b64.js` and `earth-clouds-png-b64.js` (works offline; Three.js loads from CDN).

**Option B — local server:**

```bash
git clone https://github.com/enriko-kroj/meosphere-constellation-demo.git
cd meosphere-constellation-demo
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## Controls

| Control | Description |
|---------|-------------|
| **Orbital planes** | Number of orbital planes (2–6) |
| **Sats per plane** | Satellites in each plane (4–10) |
| **Orbit altitude** | 400–36,000 km (LEO / MEO / GEO) |
| **ISL link range** | Max satellite-to-satellite link distance (km) |
| **Simulation speed** | Time multiplier |
| **Show inter-satellite links** | Toggle ISL lines between satellites |
| **Ground-to-sat links** | Toggle GSL lines from ground stations |
| **Pause / Resume** | Freeze or continue simulation |
| **Reset view** | Reset camera orbit |
| **Rebuild constellation** | Rebuild with current settings and reset sim time |

**Mouse:** drag to orbit the camera · scroll to zoom · click a satellite or ground station to inspect links.

## Project structure

```
index.html              Main app (Three.js scene + UI)
earth-day-jpg-b64.js    Embedded Earth day texture
earth-clouds-png-b64.js Embedded cloud texture
assets/                 Source texture files
```

## Stack

- [Three.js](https://threejs.org/) r128 (CDN)
- Vanilla JavaScript, no build step
