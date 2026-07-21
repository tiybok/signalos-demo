# Planned Third-Party Components

This baseline contains no installed runtime packages. The following components are planned and must be reverified against the exact locked versions before acceptance.

| Component | Role | Expected open-source status | Acceptance requirement |
|---|---|---|---|
| React | User interface | Permissive | Verify version, licence, and security advisories |
| Vite | Frontend build | Permissive | Verify ARM64 development workflow and lockfile |
| TypeScript | Static typing | Permissive | Verify exact version and licence |
| FastAPI | Local API | Permissive | Verify exact version and advisories |
| Pydantic | Schema validation | Permissive | Verify exact version and advisories |
| Uvicorn | ASGI server | Permissive | Bind locally by default |
| OpenAI Python SDK | GPT-5.6 API client | Open-source client; proprietary service | Keep key server-side and pin version |
| MediaPipe Tasks Vision | Optional local camera metrics | Permissive | Verify browser distribution and privacy behaviour |
| Ollama | Local inference service | Open-source | Bind locally and do not treat output as production authority |
| Pytest | Python tests | Permissive | Development only |
| Ruff | Python lint/format | Permissive | Development only |
| basedpyright | Python typing | Permissive | Development only |
| ESLint | TypeScript linting | Permissive | Development only |
| Prettier | Formatting | Permissive | Development only |
| Gitleaks | Secret scanning | Permissive | Required before push |
| pip-audit | Python dependency audit | Permissive | Required before release |

The GPT-5.6 and Codex services are required external proprietary services. Their client libraries may be open-source, but the services themselves are not part of the project's open-source runtime.


## Approved VS Code development extensions

These tools are not redistributed as SignalOS runtime dependencies. Exact installed versions must be recorded before submission.

| Extension ID | Purpose | Policy |
|---|---|---|
| `OpenAI.chatgpt` | Official Codex integration | Required proprietary-service exception |
| `ms-python.python` | Python environment and debugging | Open-source development tool |
| `charliermarsh.ruff` | Python linting and formatting | Open-source development tool |
| `detachhead.basedpyright` | Python language server and type checking | Open-source development tool |
| `dbaeumer.vscode-eslint` | TypeScript lint integration | Open-source development tool |
| `esbenp.prettier-vscode` | TypeScript, JSON, and Markdown formatting | Open-source development tool |
| `EditorConfig.EditorConfig` | Cross-editor formatting | Open-source development tool |
| `asispts.neo-git-graph` | Visual Git history | MIT-licensed open-source fork |


## Implemented optional browser dependency

| Component | Exact version | Capability | Licence / source | Security and removal boundary |
|---|---:|---|---|---|
| `@mediapipe/tasks-vision` | `0.10.35` | Browser-local BlazeFace face presence and framing measurements | Apache-2.0 MediaPipe package; official Google MediaPipe short-range model asset | Loaded only after explicit camera permission; frames and detections remain in browser memory; remove `frontend/src/face.ts` and this package to revert. The model is not used for identity, demographics, emotion, landmarks, or surveillance. |
