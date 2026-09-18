# SatQuery X — Advanced Runnable Browser Prototype

## Run
1. Extract the ZIP.
2. Open `index.html` in Chrome, Edge, or Firefox.
3. Choose a mission type.
4. Upload one or two images, or click **Load demo imagery**.
5. Click **Run analysis**.
6. Inspect the input image, evidence overlay, metrics, quality gate, data summary, and execution trace.
7. Export a JSON mission report.

## What is genuinely functional
- Local image loading and preview
- Browser-side Canvas pixel inspection
- Heuristic candidate highlighting for water-like, vegetation-like, built-up-like and other pixels
- Image-to-image difference layer for change demonstration
- Mission-type routing
- Input/secondary-image checks
- Quality and guardrail reporting
- Observable execution trace
- JSON report export
- Responsive UI

## What is not yet operational
This is not a trained satellite VLM. It does not claim scientific remote-sensing accuracy. It is a functional prototype of the product and orchestration experience.

For the real SIH implementation, connect:
- GeoTIFF reader and CRS/metadata validation
- A remote-sensing-adapted VLM for VQA/captioning
- A grounding model for semantic regions
- A trained change-detection or change-VQA model
- Optical–SAR fusion model
- Backend endpoints such as `/validate`, `/plan`, `/execute`, `/report`
- Calibrated confidence and benchmark evaluation

## Recommended next step
Keep this interface as the front end and add a Python FastAPI or Node backend. Replace `analyzeCanvas()` with API calls while preserving the evidence, quality-gate, trace and report contracts.
