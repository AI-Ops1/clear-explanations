# Choosing and producing an explanation format

Choose based on what the reader needs to understand, not on what the agent can generate.

## Diagrams and images

Use diagrams for sequences, decisions, relationships, and system boundaries. Use an image when appearance or spatial context matters.

- Give the visual one clear question to answer.
- Label actors, arrows, decisions, and units where needed.
- Show important exception paths; do not invent connections.
- Prefer Mermaid or SVG for precise, editable diagrams when supported.
- Use image generation for illustrative imagery when appropriate; do not rely on it for exact technical labels or quantitative charts.
- Include a short text explanation or accessible alternative. Do not convey meaning through color alone.

Example: show request -> impact estimate -> customer approval -> delivery -> invoice, with a rejected-change path that returns to the original scope.

## Interactive pages

Use interaction when changing inputs teaches a relationship or when the reader needs to explore several states.

- Prefer a self-contained HTML file with native controls for a small explanation.
- Show input labels, units, assumptions, formulas, and output meanings.
- Use synthetic data by default. Do not embed credentials or private client data.
- Handle empty, zero, invalid, and extreme inputs. Use keyboard-accessible controls and readable contrast.
- Check the actual interaction and calculations with available browser tools. State any verification limitation.
- Avoid unnecessary services, dependencies, tracking, or deployment. A local artifact is enough unless hosting is requested.

Example: fixed fee minus total hours multiplied by hourly cost equals illustrative project profit. Let the reader change extra hours and see the effect. Explain that this simplified model excludes other costs.

## Explainer videos

Use video when time, movement, or coordinated narration adds understanding. Do not make video the default for routine messages or social posts.

- Define the learning goal, audience, duration, and final takeaway.
- Build a short storyboard: scene, visual, narration, and timing.
- Keep narration and visuals aligned. Define jargon before using it.
- Provide captions or a transcript and readable labels.
- Use available production skills and tools. Check the final render for factual accuracy, synchronization, legibility, and audio quality.
- Do not use paid APIs or incur costs without authorization. If production tools are unavailable, provide a labeled storyboard or script and state that the video has not been rendered.
- Use original visual treatment and authorized assets. Credit inspiration without implying affiliation.

## Final format check

Would a shorter format explain this just as well? If yes, use it. If the user explicitly requested a format, honor it and keep the artifact focused.
