# SignalOS — Static Judge Demo

A no-backend, no-key demonstration of **SignalOS — The AI Attention Control Plane**.

## Sample scenarios

1. **Release Guard** — scope drift, replay failure, missing verification, and recording risk.
2. **Presentation Ready** — microphone clipping, low light, off-centre framing, and sustained silence.
3. **Multi-Agent Recovery** — repeated failure, permission blocking, missing tests, and a stalled worker.

Every example is a deterministic static simulation. The demo does not call a backend, OpenAI, Codex, Ollama, camera, or microphone.

## Run locally

Do not double-click `index.html`. Serve the directory over HTTP:

```bash
python3 -m http.server 4173 --bind 127.0.0.1
```

Open <http://127.0.0.1:4173/>. <https://tiybok.github.io/signalos-demo/>

## GitHub Pages

Publish the repository from `main` and `/ (root)` under **Settings → Pages**.
