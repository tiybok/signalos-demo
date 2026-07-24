# SignalOS — Static Judge Demo

A no-backend, no-key demonstration of **SignalOS — The AI Attention Control Plane**.

## Sample scenarios

1. **Release Guard** — detects scope drift, replay failure, missing verification, and recording risk.
2. **Presentation Ready** — identifies microphone clipping, low light, off-centre framing, and sustained silence.
3. **Multi-Agent Recovery** — highlights repeated failures, permission blocking, missing tests, and stalled workers.

Every example is a deterministic static simulation. This demo does not call a backend, OpenAI, Codex, Ollama, camera, or microphone.

## Run locally

Do not double-click `index.html`. Serve the directory over HTTP:

```bash
python3 -m http.server 4173 --bind 127.0.0.1
```

Then open:

http://127.0.0.1:4173/

## Explore SignalOS

**Live Demo:**
https://tiybok.github.io/signalos-demo/

**Request Full Code Access:**
https://github.com/tiybok/signalos

**Connect on LinkedIn:**
https://www.linkedin.com/in/rutvik-bhalerao/

## GitHub Pages

Publish the repository from the `main` branch and `/ (root)` under **Settings → Pages**.
