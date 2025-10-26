
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


## Case Lists
- [Case 01: Detection](#case-01-detection)
- [Case 02: Pseudo Healthy Reconstruction ](#case-02-status-transformation)
- [Case 03: Add Annotations](#case-03-add-only-annotations)
- [Case 04: Annotation and Marker Removal](#case-04-annotation-and-marker-removal)
- [Case 05: Modaility Transformation](#case-05-pseudo-healthy-reconstruction)
- [Case 06: Modify Lesions](#case-06-modify-lesions)
- [Case 07: Remove Artifacts](#case-07-remove-artifacts)

--- 
## Use Cases 🏥

### Case 01: Detection

**Prompt**
<details>
<summary>Show prompt</summary>

```
Detect and localize abnormal regions in this MRI slice. 
Detect and localize abnormal regions in this [image modality]. Highlight abnormal areas with bounding boxes.
```
</details>

| MRI Original | MRI Gemini | CT Original | CT Gemini |
|--------------|------------|-------------|-----------|
| <img src="./images/case_17946.png" alt="MRI Input Image" width="200"> | <img src="./images/case_17946_gemini.png" alt="MRI Gemini Output" width="200"> | <img src="./images/case_19205.png" alt="CT Input Image" width="200"> | <img src="./images/case_19205_gemini.png" alt="CT Gemini Output" width="200"> |

---

### Case 02: Pseudo Healthy Reconstruction
<details>
<summary>Show prompt</summary>

```
Remove the unhealthy or abnormal areas in the images and generate a healthy version of the image.
```
</details>

| MRI (a) Original | MRI (a) Gemini | MRI (b) Original | MRI (b) Gemini |
|------------------|----------------|------------------|----------------|
| <img src="./images/case_18826.png" alt="MRI (a) Input Image" width="200"> | <img src="./images/case_18826_gemini.png" alt="MRI (a) Gemini Output" width="200"> | <img src="./images/case_19195.png" alt="MRI (b) Input Image" width="200"> | <img src="./images/case_19195_gemini.png" alt="MRI (b) Gemini Output" width="200"> |

### Case 03: Add Annotations
<details>
<summary>Show prompt</summary>

```
Annotate this [image modality] without altering the original pixels. Add overlays/annotations only.
```
</details>

| MRI Original | MRI Gemini | Surgical Original | Surgical Gemini |
|--------------|------------|-------------------|-----------------|
| <img src="./images/case_7941.png" alt="MRI Input Image" width="200"> | <img src="./images/case_7941_gemini.png" alt="MRI Gemini Output" width="200"> | <img src="./images/case18515.png" alt="Surgical Input Image" width="200"> | <img src="./images/case18515_gemini.png" alt="Surgical Gemini Output" width="200"> |

| MRI Original | MRI Gemini | 
|--------------|------------|
| <img src="./images/case_17344_2.png" alt="MRI Input Image" width="200"> | <img src="./images/case_17344_2_gemini.png" alt="MRI Gemini Output" width="200"> | <img src="./images/case18515.png" alt="Surgical Input Image" width="200"> | 

### Case 04: Annotation and Marker Removal
<details>
<summary>Show prompt</summary>

```
Remove all annotations, arrows, labels, text, and markers from this scan image. Reconstruct the underlying anatomy naturally and seamlessly, keeping the original texture, contrast, and medical details intact. Do not alter or blur anatomical structures.
```
</details>

| MRI Original | MRI Gemini | Surgical Original | Surgical Gemini |
|--------------|------------|-------------------|-----------------|
| <img src="./images/case_18515.png" alt="MRI Input Image" width="200"> | <img src="./images/case_18515_gemini.png" alt="MRI Gemini Output" width="200"> | <img src="./images/case_18816.png" alt="Surgical Input Image" width="200"> | <img src="./images/case_18816_gemini.png" alt="Surgical Gemini Output" width="200"> |
```
Please remove the skull from the image. It appears as the outermost bright white border.
```

```
Remove the skull from the image and retain only show the brain region in the final output. 
yes correct, but you change the brain, you should not change the brain
My apologies! I understand now. You want the skull removed, but the brain itself should remain untouched, just as it was in the original image. Let me correct that for you: 
```

| MRI Original | MRI Gemini | 
|--------------|------------|
| <img src="./images/case_19196.png" alt="MRI Input Image" width="200"> | <img src="./images/case_19196_gemini.png" alt="MRI Gemini Output" width="200"> | <img src="./images/case_18816.png" alt="Surgical Input Image" width="200"> | 

### Case 05: Modaility Transformation
<details>
<summary>Show prompt</summary>

```
Generate a realistic transthoracic echocardiographic (ultrasound) image of the human heart in a similar view and orientation as the provided cardiac MRI image. The image should depict the left ventricle, left atrium, and mitral valve region with clear grayscale ultrasound texture, realistic speckle noise, and anatomical detail. The mitral valve leaflets should be visible with slight curvature consistent with systole. Use appropriate ultrasound shading, acoustic shadowing, and tissue echogenicity. The overall appearance must resemble a real clinical echocardiogram, not a diagram or illustration.

Generate a realistic 3D anatomical model of the human spine based on the provided sagittal MRI image. The 3D reconstruction must precisely match the curvature, alignment, and proportions of the vertebrae as seen in the MRI. Include detailed vertebral bodies, intervertebral discs, spinal canal, and surrounding soft tissue outlines. Maintain anatomical accuracy of thoracic and lumbar segments, preserving the same posture and sagittal orientation as the original MRI. Render the 3D model in a semi-transparent medical visualization style with realistic bone texture and soft lighting. The result should look like a 3D version of this MRI slice, without any change in direction or angle.
Emphasize: same sagittal view, same curvature, anatomically correct spine model reconstructed from MRI data.
```
</details>

| Original | Gemini | Surgical Original | Surgical Gemini |
|--------------|------------|-------------------|-----------------|
| <img src="./images/case_13950.png" alt="MRI Input Image" width="200"> | <img src="./images/case_13950_gemini.png" alt="MRI Gemini Output" width="200"> | <img src="./images/case_14834.png" alt="Surgical Input Image" width="200"> | <img src="./images/case_14834_gemini.png" alt="Surgical Gemini Output" width="200"> |

### Case 06: Modify Lesions
<details>
<summary>Show prompt</summary>

```
The red box indicates the tumor region for reference only — do not display the box in the output.
Simulate advanced-stage tumor progression in that region: enlarge the lesion by approximately 50% relative to the original size.
Keep all other brain anatomy, alignment, and texture identical to the original image, with no artifacts or hallucinated structures.

The red box indicates the lesion region to be removed — do not show the box in the output.
Generate a version of the scan with that lesion completely removed, restoring normal tissue appearance and continuity in that region.
Preserve all surrounding brain anatomy, alignment, intensity patterns, and MR noise exactly as in the original image.
The result must look anatomically realistic and artifact-free.
```
</details>

| Original | Gemini | Surgical Original | Surgical Gemini |
|--------------|------------|-------------------|-----------------|
| <img src="./images/17344.png" alt="MRI Input Image" width="200"> | <img src="./images/17344_gemini.png" alt="MRI Gemini Output" width="200"> | <img src="./images/17344.png" alt="Surgical Input Image" width="200"> | <img src="./images/17344_gemini_2.png" alt="Surgical Gemini Output" width="200"> |

### Case 07: Remove Artifacts
<details>
<summary>Show prompt</summary>

```
Use the provided scan as the anatomical reference.
Remove imaging artifacts or acquisition noise while keeping all brain structures, intensity gradients, and MR texture identical to the original.
Do not alter anatomy, contrast, or alignment.

Remove the imaging artifacts and restore normal brain tissue appearance while preserving all anatomical structures, symmetry, and MR intensity patterns.
Keep the ventricles, cortex, and white matter boundaries identical to the original scan.
Produce a clean, artifact-free, anatomically faithful version that looks realistic and consistent with standard T1 MRI.
```
</details>

| Original | Gemini | Original | Gemini |
|--------------|------------|-------------------|-----------------|
| <img src="./images/artefect.png" alt="MRI Input Image with Artifact" width="200"> | <img src="./images/artefect_gemini.png" alt="MRI Gemini Output (Artifact Removed)" width="200"> |  <img src="./images/artefect2.png" alt="MRI Input Image with Artifact" width="200"> | <img src="./images/artefect_gemini2.png" alt="MRI Gemini Output (Artifact Removed)" width="200">|



### Case 08: Segmentation (分割)


<details>
<summary>Show prompt</summary>

```
Segment all visible organs in the image..
```
</details>

| Original | Ground Truth Mask | Gemini Overlay | Gemini Mask |
|----------|-------------------|----------------|-------------|
| <img src="./images/case_15782.png" alt="Original Image" width="200"> | <img src="./images/case_15782_gemini.png" alt="Ground Truth Mask" width="200"> | <img src="./images/case_15782_2.png" alt="Gemini Overlay" width="200"> | <img src="./images/case_15782_2_gemini.png" alt="Gemini Mask" width="200"> |




## Datasets 📊
Source: EURORAD (https://eurorad.org).  
License: Please refer to the source. This repository does not redistribute original datasets; respect the original licensing and usage terms.

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
