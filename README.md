# Designer’s Side Chick (DSC)

Designer’s Side Chick (DSC) is a companion application for designers, printers, and makers who already use a primary design tool but need precise control over dithering, palettes, dots, and color-constrained output.

DSC is not meant to replace your main design software. It is designed to support existing workflows, especially print-focused and fabrication workflows where color accuracy, repeatability, and strict color rules matter.

I’m currently offering 1,000 free trial keys valid until February 1st.  
You can try DSC via the project links or join the WhatsApp group for downloads, discussion, and feedback.

---

## Why DSC Exists

Many powerful design tools offer limited control over:
- Dithering behavior
- Palette enforcement
- Print-ready color constraints
- Repeatable dot-based output

DSC was built specifically to solve those problems.

One important distinction:

**DSC does not blend or compare images.**  
You extract a palette once (from a CMYK chart, brand colors, or swatches), then apply those color rules to other images. Every dot is generated using only the allowed colors.

This makes DSC especially useful for print, textile, and fabrication workflows.

---

## Current Status

DSC is currently in beta.  
I’m actively shipping updates and refining features based on real user feedback.

I’m also developing a companion tool called **The Other Chick**, which will generate dithering algorithms and palettes using mathematical rules and integrate directly with DSC.

Feedback is welcome — good or bad.

---

## Demo Video

[![DSC Demo Video](https://img.youtube.com/vi/zvRKAi1vU2o/hqdefault.jpg)](https://www.youtube.com/watch?v=zvRKAi1vU2o)

_Click the image to watch the demo on YouTube._


---
## Screenshots

### Featured Views

![Workspace Selector](media/screenshots/workspace-selector.png)
![Dithering Presets](media/screenshots/dithering-presets.png)
![Palette Extraction Exact](media/screenshots/palette-extraction-exact.png)
![Overlay / Dot System](media/screenshots/overlay.png)
![3D Overview](media/screenshots/3d-overview.png)

<details>
<summary><strong>Show more screenshots</strong></summary>

![3D Height Calculation Presets](media/screenshots/3d-height-calculation-presets.png)
![3MF Layer Mode Mapped Palette](media/screenshots/3mf-layer-mode-mapped-palette.png)
![Background Color Changer](media/screenshots/background-color-changer.png)
![Dithering Adjust](media/screenshots/dithering-adjust.png)
![Dithering Basic](media/screenshots/dithering-basic.png)
![Dithering Diffusion](media/screenshots/dithering-diffusion.png)
![Dithering Output Gray](media/screenshots/dithering-output-gray.png)
![Dithering Output Indexed](media/screenshots/dithering-output-indexed.png)
![Dot Edge Management](media/screenshots/dot-edge-management.png)
![Dot Inset Management](media/screenshots/dot-inset-management.png)
![Dot Outline Management](media/screenshots/dot-outline-management.png)
![Export Options](media/screenshots/export-options.png)
![Extract CMYK Calibration A](media/screenshots/extract-cmyk-for-calibration-a.png)
![Extract CMYK Calibration B](media/screenshots/extract-cmyk-for-calibration-b.png)
![Extract CMYK Calibration C](media/screenshots/extract-cmyk-for-calibration-c.png)
![Extract CMYK Calibration D](media/screenshots/extract-cmyk-for-calibration-d.png)
![Extracting Exact Unique Colors](media/screenshots/extracting-exact-unique-colors.png)
![ICC Profile Import](media/screenshots/icc-profile-import.png)
![Mapped CMYK Dotted](media/screenshots/mapped-cmyk-dotted.png)
![Original Dotted](media/screenshots/orginal-dotted.png)
![Overall Color Adjustment](media/screenshots/overall-color-adjustment.png)
![Override Individual Dot](media/screenshots/override-individual-dot-visibility-color-size.png)
![Palette Extraction Auto](media/screenshots/palette-extraction-auto.png)
![Palette Extraction Semi Auto](media/screenshots/palette-extraction-semi-auto.png)
![Palette View Families](media/screenshots/palette-view-families.png)
![Palette Viewer Pixel Editor](media/screenshots/palette-viewer-pixel-editor.png)
![Workspace Selector Alternate](media/screenshots/workspace-selector.png)

</details>


---

## What Designer’s Side Chick Can Do

### Image & Workflow
- Open and process raster images with fast live preview
- Switchable 2D and 3D workflows
- Non-destructive workflow
- Real-time preview updates
- Adjustable zoom, pan, and canvas background
- Optional inverted pan controls

---

## Dithering Engine (Core Feature)

- Toggle dithering on/off at any time
- Dithering modes:
  - Grayscale
  - RGB
  - Indexed (palette-based)
- Adjustable dithering strength (original vs dithered blend)
- Grayscale and color level control (2–256)

### Ordered Dithering Presets
- Bayer 4×4, Bayer 8×8
- Clustered matrices
- Halftone patterns

### Error Diffusion Presets
- Floyd–Steinberg (normal & serpentine)
- Atkinson
- Burkes
- Sierra (full, two-row, lite)
- Stucki
- Jarvis–Judice–Ninke
- Diffusion Row / Column / 2D / Grid
- Skip Neighbors (1–3)
- Fan, ShiauFan 1, ShiauFan 2

### Advanced Diffusion Controls
- Custom diffusion kernel weights
- Directional error spread control
- Experimental diffusion patterns
- Performance downscaling for fast previews (full-resolution export later)

---

## Dither-Only Image Adjustments

These adjustments affect only the dithering stage, not the original image:
- Sharpening
- Brightness
- Contrast
- Gamma
- Hue
- Saturation
- Individual RGB channel balance

---

## Overlay / Dot System

- Dot overlay rendering on top of the image
- True halftone black & white mode
- Optional original-image visibility under dots
- Adjustable dot grid size
- Dot opacity and size limits
- Diameter strength control

### Dot Shapes
- Circular
- Polygonal
- Star-like
- Adjustable edge count and inset
- Outline width and opacity control

### Per-Dot Editing
- Click individual dots
- Override color, size, and height per dot

---

## Palette Tools

- Extract palettes from images
- Editable palette grid
- Enable/disable individual colors
- Indexed palette-based dithering
- Palette mapping for dots and exports
- Palette reuse across projects

---

## 3D / Board Mode

- Convert dot data into height-based geometry
- Board-style 3D generation
- Adjustable board dimensions
- Height scaling controls
- Export formats:
  - STL
  - 3MF (multi-color capable)

Designed for CNC, laser, and 3D printing workflows.

---

## Export Options

- Export dithered images
- Export dot overlays (vector or raster)
- Export extracted palettes (JSON, CSV, ASE)
- Export 3D models (STL, 3MF, stacked 3MF)
- Preview or full-resolution export
- RGB and CMYK workflows supported
- Optional ICC profile handling

---

## Color Calibration & Palette Transfer (Key Concept)

One of the core ideas behind DSC is separating color decisions from image content.

### How It Works
1. Import an image that already contains the exact colors you want  
   (CMYK chart, brand palette, fabric test print, swatch sheet)
2. Extract a palette from that image
3. Lock that palette as a color rule
4. Import a completely different image
5. Apply the locked palette
6. Generate a dot overlay using only the allowed colors

No blending. No averaging. Each dot is mapped to the nearest allowed color.

---

## Real-World Example

- Extract four CMYK colors from a reference chart
- Import a full-color photograph
- Enable Indexed / Palette mode
- Generate a dot overlay using only those four colors

Result: a controlled, print-ready image that respects ink limits and produces repeatable output.

---

## Why This Matters

This workflow is especially useful for:
- CMYK print preparation
- Screen printing
- DTF / DTG printing
- Fabric and textile printing
- Brand color enforcement
- Ink usage control
- Consistent output across multiple images

Instead of guessing colors every time, DSC allows you to:
- Lock a palette once
- Reuse it across unlimited images
- Maintain identical dithering and dot behavior
- Achieve predictable, repeatable results

DSC doesn’t apply a filter — it forces images to obey your color rules.

---

## macOS Gatekeeper & Beta Notes

Designer’s Side Chick (DSC) is currently in **active beta**.

During beta, DSC is distributed directly so updates and improvements can ship quickly. Because of this, macOS may show a security message the **first time** you open the app. This is normal behavior for beta software on macOS.

### First launch (one-time step)
If macOS blocks the app on first launch:

1. Open **System Settings**
2. Go to **Privacy & Security**
3. Scroll down to **Security**
4. You’ll see a message that DSC was blocked
5. Click **Open Anyway**
6. Confirm when prompted

After this one-time approval, DSC will open normally.

### Why this happens
macOS applies extra checks to apps that are still in beta or distributed outside the App Store. DSC does not install background services, system extensions, or hidden processes.

This beta approach allows:
- Faster updates
- Direct user feedback
- Rapid iteration on experimental tools


---
###  Beta Tester Access (PS)

**PS:**  
If you’d like to help test **Designer’s Side Chick (DSC)**, feel free to message me on **Instagram**.

I’m sharing beta access with people who genuinely work with design, print, color, or fabrication workflows and are interested in giving real feedback. To keep things smooth and useful for everyone:

- Beta keys are shared with real, active accounts  
- Profiles with some history or creative/work-related context are preferred  
- This helps make sure DSC is tested by people who will actually use it  

If that sounds like you, I’d love to hear what you’re working on and how you’d like to use DSC.

Thanks for helping shape the project 
