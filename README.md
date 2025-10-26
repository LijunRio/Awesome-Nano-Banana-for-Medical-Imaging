
# 🩻 Awesome Nano Banana for Medical Imaging 🍌

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> A curated collection of **resources, prompts, examples, and projects** exploring the **Nano Banana (Gemini-2.5-Flash-Image)** framework for **medical imaging research**.

---

## 👋 Welcome

Awesome Nano Banana for Medical Imaging is a community-driven exploratory repository that investigates the potential applications of the Gemini-2.5-Flash-Image (“Nano Banana”) model — a general-purpose vision–language generation model — in medical imaging tasks.

This project aims to collect, explore, and characterize the capabilities of general AGI-oriented generative models within the context of medical imaging. The repository seeks to uncover emerging capabilities of such models and to inspire further research at the intersection of generative AI and medical imaging. Potential applications include data augmentation, cross-modal understanding in clinical and educational settings, and the use of generative models for medical education, simulation, and visual communication.

⚠️ **Important Notices**

* All example images are **publicly available** and **anonymized**.
* **No protected health information (PHI)** is included.
* Generated outputs are **synthetic**, **non-clinical**, and **for research and teaching only**.
* The examples **must not be used for diagnosis, treatment, or any clinical decision-making**.


## Example Lists
- [Example 1: Detection of abnormal regions in MRI slice](#example-1-detection-of-abnormal-regions-in-mri-slice)
- [Example 2: Detection of abnormal regions in CT image](#example-2-detection-of-abnormal-regions-in-ct-image)
- [Example 3: Remove unhealthy areas in MRI (a)](#example-3-remove-unhealthy-areas-in-mri-a)
- [Example 4: Remove unhealthy areas in MRI (b)](#example-4-remove-unhealthy-areas-in-mri-b)
- [Example 5: Generate healthy version of brain](#example-5-generate-healthy-version-of-brain)
- [Example 6: Annotate MRI without altering pixels](#example-6-annotate-mri-without-altering-pixels)
- [Example 7: Annotate surgical image without altering pixels](#example-7-annotate-surgical-image-without-altering-pixels)
- [Example 8: Identify imaging view and anatomical region in MRI](#example-8-identify-imaging-view-and-anatomical-region-in-mri)
- [Example 9: Remove annotations from MRI scan](#example-9-remove-annotations-from-mri-scan)
- [Example 10: Remove annotations from surgical scan](#example-10-remove-annotations-from-surgical-scan)
- [Example 11: Remove skull from MRI image](#example-11-remove-skull-from-mri-image)
- [Example 12: Remove skull from MRI image (alternative)](#example-12-remove-skull-from-mri-image-alternative)
- [Example 13: Generate ultrasound from cardiac MRI](#example-13-generate-ultrasound-from-cardiac-mri)
- [Example 14: Generate 3D spine model from sagittal MRI](#example-14-generate-3d-spine-model-from-sagittal-mri)
- [Example 15: Generate abdominal CT from 3D abdomen reconstruction](#example-15-generate-abdominal-ct-from-3d-abdomen-reconstruction)
- [Example 16: Generate 3D mesh of brain](#example-16-generate-3d-mesh-of-brain)
- [Example 17: Generate 3D mesh of teeth](#example-17-generate-3d-mesh-of-teeth)
- [Example 18: Simulate tumor progression in brain](#example-18-simulate-tumor-progression-in-brain)
- [Example 19: Remove lesion from brain scan](#example-19-remove-lesion-from-brain-scan)
- [Example 20: Remove artifacts from MRI scan (1)](#example-20-remove-artifacts-from-mri-scan-1)
- [Example 21: Remove artifacts from MRI scan (2)](#example-21-remove-artifacts-from-mri-scan-2)
- [Example 22: Segment all visible organs in image](#example-22-segment-all-visible-organs-in-image)
- [Example 23: Segment all visible organs in image (overlay)](#example-23-segment-all-visible-organs-in-image-overlay)
- [Example 24: Generate pixel-level segmentation of cardiac chambers](#example-24-generate-pixel-level-segmentation-of-cardiac-chambers)
- [Example 25: Generate pixel-level segmentation of brain glioma](#example-25-generate-pixel-level-segmentation-of-brain-glioma)
- [Example 26: Generate brain segmentation](#example-26-generate-brain-segmentation)

## 🍌 What is Nano Banana
Nano Banana is the most advanced image generation and editing model developed by the Google Gemini team (officially known as **Gemini-2.5-Flash-Image**). It marks a major shift from being an “AI drawing tool” to becoming an **AI creative partner**.

🔍 **Key Features**

* **Context-aware editing:** Understands the relationship between people and their environments, automatically adjusting lighting and reflections when replacing backgrounds.
* **Precision manipulation:** Can accurately add or replace image elements, handling occlusion and lighting with exceptional clarity.
* **Deep 3D understanding:** “Sees” three-dimensional structures within 2D images, enabling spatially coherent editing.
* **Style consistency:** Builds a unified visual world based on a single reference image.
* **Creative collaboration:** Shifts from “command execution” to “inspirational dialogue,” supporting iterative creativity.

 
## Examples

### Example 1: Detection of abnormal regions in MRI slice

**Prompt**
<details>
<summary>Show prompt</summary>

```
Detect and localize abnormal regions in this MRI slice. 
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_17946.png" alt="MRI Input Image" width="200"> | <img src="./images/case_17946_gemini.png" alt="MRI Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/17946)

### Example 2: Detection of abnormal regions in CT image

<details>
<summary>Show prompt</summary>

```
Detect and localize abnormal regions in this CT image. Highlight abnormal areas with bounding boxes.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_19205.png" alt="CT Input Image" width="200"> | <img src="./images/case_19205_gemini.png" alt="CT Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/19205)

---

### Example 3: Remove unhealthy areas in MRI (a)

<details>
<summary>Show prompt</summary>

```
Remove the unhealthy or abnormal areas in the images and generate a healthy version of the image.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_18826.png" alt="MRI (a) Input Image" width="200"> | <img src="./images/case_18826_gemini.png" alt="MRI (a) Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/18826)

### Example 4: Remove unhealthy areas in MRI (b)

<details>
<summary>Show prompt</summary>

```
Remove the unhealthy or abnormal areas in the images and generate a healthy version of the image.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_19195.png" alt="MRI (b) Input Image" width="200"> | <img src="./images/case_19195_gemini.png" alt="MRI (b) Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/19195)

### Example 5: Generate healthy version of brain

<details>
<summary>Show prompt</summary>

```
Generate a healthy version of this brain.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_13910_b.png" alt="Brain Input Image" width="200"> | <img src="./images/gemini_case_13910_b.png" alt="Healthy Brain Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/13910)

### Example 6: Annotate MRI without altering pixels

<details>
<summary>Show prompt</summary>

```
Annotate this MRI without altering the original pixels. Add overlays/annotations only.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_7941.png" alt="MRI Input Image" width="200"> | <img src="./images/case_7941_gemini.png" alt="MRI Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/7941)

### Example 7: Annotate surgical image without altering pixels

<details>
<summary>Show prompt</summary>

```
Annotate this surgical image without altering the original pixels. Add overlays/annotations only.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case18515.png" alt="Surgical Input Image" width="200"> | <img src="./images/case18515_gemini.png" alt="Surgical Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/18515)

### Example 8: Identify imaging view and anatomical region in MRI

<details>
<summary>Show prompt</summary>

```
Identify the imaging view (axial, sagittal, or coronal) and anatomical region shown in this scan.
Overlay a small text label in the corner with the view and body region.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_17344_2.png" alt="MRI Input Image" width="200"> | <img src="./images/case_17344_2_gemini.png" alt="MRI Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/17344) 

### Example 9: Remove annotations from MRI scan

<details>
<summary>Show prompt</summary>

```
Remove all annotations, arrows, labels, text, and markers from this scan image. Reconstruct the underlying anatomy naturally and seamlessly, keeping the original texture, contrast, and medical details intact. Do not alter or blur anatomical structures.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_18515.png" alt="MRI Input Image" width="200"> | <img src="./images/case_18515_gemini.png" alt="MRI Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/18515)

### Example 10: Remove annotations from surgical scan

<details>
<summary>Show prompt</summary>

```
Remove all annotations, arrows, labels, text, and markers from this scan image. Reconstruct the underlying anatomy naturally and seamlessly, keeping the original texture, contrast, and medical details intact. Do not alter or blur anatomical structures.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_18816.png" alt="Surgical Input Image" width="200"> | <img src="./images/case_18816_gemini.png" alt="Surgical Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/18816)

### Example 11: Remove skull from MRI image

<details>
<summary>Show prompt</summary>

```
Please remove the skull from the image. It appears as the outermost bright white border.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_19196.png" alt="MRI Input Image" width="200"> | <img src="./images/case_19196_gemini.png" alt="MRI Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/19196)

### Example 12: Remove skull from MRI image (alternative)

<details>
<summary>Show prompt</summary>

```
1. Remove the skull from the image and retain only show the brain region in the final output. 
2. yes correct, but you change the brain, you should not change the brain
```
</details>

| Input | Output1 |Output2 |
|-------|--------|--------|
| <img src="./images/case_17504.png" alt="MRI Input Image" width="200"> | <img src="./images/case_17504_gemini1.png" alt="MRI Gemini Output" width="200"> |  <img src="./images/case_17504_gemini2.png" alt="MRI Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/17504) 


### Example 13: Generate ultrasound from cardiac MRI

<details>
<summary>Show prompt</summary>

```
Generate a realistic transthoracic echocardiographic (ultrasound) image of the human heart in a similar view and orientation as the provided cardiac MRI image. The image should depict the left ventricle, left atrium, and mitral valve region with clear grayscale ultrasound texture, realistic speckle noise, and anatomical detail. The mitral valve leaflets should be visible with slight curvature consistent with systole. Use appropriate ultrasound shading, acoustic shadowing, and tissue echogenicity. The overall appearance must resemble a real clinical echocardiogram, not a diagram or illustration.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_13950.png" alt="MRI Input Image" width="200"> | <img src="./images/case_13950_gemini.png" alt="MRI Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/13950)

### Example 14: Generate 3D spine model from sagittal MRI

<details>
<summary>Show prompt</summary>

```
Generate a realistic 3D anatomical model of the human spine based on the provided sagittal MRI image. The 3D reconstruction must precisely match the curvature, alignment, and proportions of the vertebrae as seen in the MRI. Include detailed vertebral bodies, intervertebral discs, spinal canal, and surrounding soft tissue outlines. Maintain anatomical accuracy of thoracic and lumbar segments, preserving the same posture and sagittal orientation as the original MRI. Render the 3D model in a semi-transparent medical visualization style with realistic bone texture and soft lighting. The result should look like a 3D version of this MRI slice, without any change in direction or angle.
Emphasize: same sagittal view, same curvature, anatomically correct spine model reconstructed from MRI data.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_14834.png" alt="Surgical Input Image" width="200"> | <img src="./images/case_14834_gemini.png" alt="Surgical Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/14834)

### Example 15: Generate abdominal CT from 3D abdomen reconstruction

<details>
<summary>Show prompt</summary>

```
Generate abdominal CT image from the 3D abdomen volume reconstruction.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_19173.png" alt="Abdomen Input Image" width="200"> | <img src="./images/gemini_case_19173.png" alt="CT Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/19173)

### Example 16: Generate 3D mesh of brain

<details>
<summary>Show prompt</summary>

```
Generate a 3D mesh of this brain.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_18099.png" alt="Brain Input Image" width="200"> | <img src="./images/gemini_case_18099.png" alt="3D Mesh Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/18099)

### Example 17: Generate 3D mesh of teeth

<details>
<summary>Show prompt</summary>

```
Generate a 3D mesh of the teeth.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_17181.png" alt="Teeth Input Image" width="200"> | <img src="./images/gemini_case_17181.png" alt="3D Mesh Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/17181)

### Example 18: Simulate tumor progression in brain

<details>
<summary>Show prompt</summary>

```
The red box indicates the tumor region for reference only — do not display the box in the output.
Simulate advanced-stage tumor progression in that region: enlarge the lesion by approximately 50% relative to the original size.
Keep all other brain anatomy, alignment, and texture identical to the original image, with no artifacts or hallucinated structures.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/17344.png" alt="MRI Input Image" width="200"> | <img src="./images/17344_gemini.png" alt="MRI Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/17344)

### Example 19: Remove lesion from brain scan

<details>
<summary>Show prompt</summary>

```
The red box indicates the lesion region to be removed — do not show the box in the output.
Generate a version of the scan with that lesion completely removed, restoring normal tissue appearance and continuity in that region.
Preserve all surrounding brain anatomy, alignment, intensity patterns, and MR noise exactly as in the original image.
The result must look anatomically realistic and artifact-free.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/17344.png" alt="Surgical Input Image" width="200"> | <img src="./images/17344_gemini_2.png" alt="Surgical Gemini Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/17344)

### Example 20: Remove artifacts from MRI scan (1)
[Data Resource](https://www.auntminnieeurope.com/clinical-news/article/15648693/know-your-artifacts-to-optimize-mri-scans)
<details>
<summary>Show prompt</summary>
```
Use the provided scan as the anatomical reference.
Remove imaging artifacts or acquisition noise while keeping all brain structures, intensity gradients, and MR texture identical to the original.
Do not alter anatomy, contrast, or alignment.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/artefect.png" alt="MRI Input Image with Artifact" width="200"> | <img src="./images/artefect_gemini.png" alt="MRI Gemini Output (Artifact Removed)" width="200"> |

### Example 21: Remove artifacts from MRI scan (2)
[Data Resource](https://link.springer.com/article/10.1007/s00330-006-0470-4)

<details>
<summary>Show prompt</summary>

```
Remove the imaging artifacts and restore normal brain tissue appearance while preserving all anatomical structures, symmetry, and MR intensity patterns.
Keep the ventricles, cortex, and white matter boundaries identical to the original scan.
Produce a clean, artifact-free, anatomically faithful version that looks realistic and consistent with standard T1 MRI.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/artefect2.png" alt="MRI Input Image with Artifact" width="200"> | <img src="./images/artefect_gemini2.png" alt="MRI Gemini Output (Artifact Removed)" width="200"> |



### Example 22: Segment all visible organs in image

<details>
<summary>Show prompt</summary>

```
Segment all visible organs in the image..
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_15782.png" alt="Original Image" width="200"> | <img src="./images/case_15782_gemini.png" alt="Ground Truth Mask" width="200"> |

[Data Resource](https://www.eurorad.org/case/15782)

### Example 23: Segment all visible organs in image (overlay)

<details>
<summary>Show prompt</summary>

```
Segment all visible organs in the image..
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_15782_2.png" alt="Gemini Overlay" width="200"> | <img src="./images/case_15782_2_gemini.png" alt="Gemini Mask" width="200"> |

[Data Resource](https://www.eurorad.org/case/15782)

### Example 24: Generate pixel-level segmentation of cardiac chambers

<details>
<summary>Show prompt</summary>

```
Generate pixel-level segmentation of the cardiac chambers.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_17698.png" alt="Cardiac Input Image" width="200"> | <img src="./images/gemini_case_17698.png" alt="Segmentation Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/17698)

### Example 25: Generate pixel-level segmentation of brain glioma

<details>
<summary>Show prompt</summary>

```
Generate a pixel-level segmentation of the brain glioma.
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_13910.png" alt="Brain Input Image" width="200"> | <img src="./images/gemini_case_13910.png" alt="Glioma Segmentation Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/13910)

### Example 26: Generate brain segmentation

<details>
<summary>Show prompt</summary>

```
Generate the brain segmentation
```
</details>

| Input | Output |
|-------|--------|
| <img src="./images/case_17773.png" alt="Brain Input Image" width="200"> | <img src="./images/gemini_case_17773.png" alt="Brain Segmentation Output" width="200"> |

[Data Resource](https://www.eurorad.org/case/17773)


## Datasets 📊
Source: EURORAD (https://eurorad.org).  
License: Please refer to the source. This repository does not redistribute original datasets; respect the original licensing and usage terms.

## Tools

All examples were generated using [Google AI Studio](https://aistudio.google.com/) with the Gemini-2.5-Flash-Image model. Default parameters were used for temperature and top_p.

Please note that due to the inherent variability in generative AI models, slight differences may occur in outputs across multiple runs.

## Contributing 🤝
See contribution.md

## Citation 📖
If you use this resource in your research, please cite:

```bibtex
@misc{awesome_nano_banana_medical,
  title={Awesome Nano Banana for Medical Imaging},
  author={Your Name},
  year={2025},
  publisher={GitHub},
  howpublished={\url{https://github.com/yourusername/awesome-nanobannan-for-medical-imaging}}
}
```
