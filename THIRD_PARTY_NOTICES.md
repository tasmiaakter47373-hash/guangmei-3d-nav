# Third-party notices

## MediaPipe Tasks Vision

- Package: `@mediapipe/tasks-vision@1.1.1`
- Upstream: Google AI Edge MediaPipe, <https://github.com/google-ai-edge/mediapipe>
- Distribution used: npm package `@mediapipe/tasks-vision`
- License: Apache License 2.0 (declared in the package's `package.json`)
- Full license text: [`LICENSES/Apache-2.0.txt`](LICENSES/Apache-2.0.txt)
- Reused pieces:
  - `vision_bundle.mjs` JavaScript runtime through the npm import
  - `wasm/*` runtime files in `public/wasm/`
  - `HandLandmarker` API, `FilesetResolver`, `DrawingUtils`
  - type declarations / README from the package for API reference
- The package README includes Google's MediaPipe Tasks privacy notice. Inference runs
  locally in the browser; camera frames are not uploaded by this prototype.

## Hand Landmarker model

- File: `public/models/hand_landmarker.task`
- Size: 7,819,105 bytes
- SHA-256: `FBC2A30080C3C557093B5DDFC334698132EB341044CCEE322CCF8BCF3607CDE1`
- Official distribution URL:
  <https://storage.googleapis.com/mediapipe-models/hand_landmarker/hand_landmarker/float16/1/hand_landmarker.task>
- License: Apache License 2.0, as part of the MediaPipe model distribution.
- Provenance note: the official Google storage host and GitHub were unreachable from
  this development environment. The local copy was obtained from the npm package
  `gesturev@1.4.1`, which bundles this MediaPipe model file. It has not been
  independently checksum-verified against Google's server. Replace it with a copy
  downloaded from the official URL and re-check the hash before any external release.

## Existing rendering dependencies

- `three@0.180.0` (MIT) — 3D rendering and OrbitControls.
- `vite@8.3.4` (MIT) — development/build tooling; not needed at runtime.

## Test media

The standalone verification used a crop of the project's own field-research photograph
(`research-24.png`) as a fake-camera test frame. That file is not part of the mall
application bundle.
