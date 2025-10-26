# 🩻 🍌  Awesome Nano Banana for Medical Imaging

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENCE)
[![English](https://img.shields.io/badge/English-README-blue)](./README.md)

> 一个精心整理的**提示、示例**集合，探索**Nano Banana (Gemini-2.5-Flash-Image)** 模型在**医学图像研究**中的应用。

---

## 👋 欢迎

Awesome Nano Banana for Medical Imaging 是一个社区驱动的探索性仓库，旨在调查 Gemini-2.5-Flash-Image（"Nano Banana"）模型——一种通用视觉-语言生成模型——在医学图像任务中的潜在应用。

该项目旨在收集、探索和表征通用 AGI 导向生成模型在医学成像背景下的能力。该仓库寻求揭示此类模型的新兴能力，并激发在生成 AI 和医学成像交叉领域的进一步研究。潜在应用包括数据增强、临床和教育环境中的跨模态理解，以及使用生成模型进行医学教育、模拟和视觉沟通。

⚠️ **重要通知**

* 所有示例图像都是**公开可用**且**匿名化**的。
* **不包含受保护的健康信息 (PHI)**。
* 生成输出是**合成**的、**非临床**的，仅用于**研究和教学**。
* 示例**不得用于诊断、治疗或任何临床决策**。


## 📋 示例列表
- [示例 1：MRI 切片中异常区域的检测](#示例-1mri-切片中异常区域的检测)
- [示例 2：CT 图像中异常区域的检测](#示例-2ct-图像中异常区域的检测)
- [示例 3：移除 MRI 中的不健康区域 (a)](#示例-3移除-mri-中的不健康区域-a)
- [示例 4：移除 MRI 中的不健康区域 (b)](#示例-4移除-mri-中的不健康区域-b)
- [示例 5：生成大脑的健康版本](#示例-5生成大脑的健康版本)
- [示例 6：注释 MRI 而不改变像素](#示例-6注释-mri-而不改变像素)
- [示例 7：注释手术图像而不改变像素](#示例-7注释手术图像而不改变像素)
- [示例 8：识别 MRI 中的成像视图和解剖区域](#示例-8识别-mri-中的成像视图和解剖区域)
- [示例 9：从 MRI 扫描中移除注释](#示例-9从-mri-扫描中移除注释)
- [示例 10：从手术扫描中移除注释](#示例-10从手术扫描中移除注释)
- [示例 11：从 MRI 图像中移除颅骨](#示例-11从-mri-图像中移除颅骨)
- [示例 12：从 MRI 图像中移除颅骨（替代方案）](#示例-12从-mri-图像中移除颅骨替代方案)
- [示例 13：从心脏 MRI 生成超声](#示例-13从心脏-mri-生成超声)
- [示例 14：从矢状 MRI 生成 3D 脊柱模型](#示例-14从矢状-mri-生成-3d-脊柱模型)
- [示例 15：从 3D 腹部重建生成腹部 CT](#示例-15从-3d-腹部重建生成腹部-ct)
- [示例 16：生成大脑的 3D 网格](#示例-16生成大脑的-3d-网格)
- [示例 17：生成牙齿的 3D 网格](#示例-17生成牙齿的-3d-网格)
- [示例 18：模拟大脑中肿瘤进展](#示例-18模拟大脑中肿瘤进展)
- [示例 19：从大脑扫描中移除病变](#示例-19从大脑扫描中移除病变)
- [示例 20：从 MRI 扫描中移除伪影 (1)](#示例-20从-mri-扫描中移除伪影-1)
- [示例 21：从 MRI 扫描中移除伪影 (2)](#示例-21从-mri-扫描中移除伪影-2)
- [示例 22：分割图像中所有可见器官](#示例-22分割图像中所有可见器官)
- [示例 23：分割图像中所有可见器官（叠加）](#示例-23分割图像中所有可见器官叠加)
- [示例 24：生成心脏室的像素级分割](#示例-24生成心脏室的像素级分割)
- [示例 25：生成大脑胶质瘤的像素级分割](#示例-25生成大脑胶质瘤的像素级分割)
- [示例 26：生成大脑分割](#示例-26生成大脑分割)

## 🍌 什么是 Nano Banana
Nano Banana 是由 Google Gemini 团队开发的最新图像生成和编辑模型（正式称为 **Gemini-2.5-Flash-Image**）。它标志着从"AI 绘图工具"向成为**AI 创意伙伴**的重大转变。

🔍 **关键特性**

* **上下文感知编辑：** 理解人与环境之间的关系，在替换背景时自动调整照明和反射。
* **精确操作：** 可以准确添加或替换图像元素，处理遮挡和照明时具有卓越的清晰度。
* **深度 3D 理解：** “看到”2D 图像中的三维结构，实现空间一致的编辑。
* **风格一致性：** 基于单个参考图像构建统一的视觉世界。
* **创意协作：** 从“命令执行”转向“灵感对话”，支持迭代创意。


## 🔍 示例

### 示例 1：MRI 切片中异常区域的检测

**提示**
<details>
<summary>显示提示</summary>

```
Detect and localize abnormal regions in this MRI slice.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_17946.png" alt="MRI 输入图像" width="200"> | <img src="./images/case_17946_gemini.png" alt="MRI Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/17946)

### 示例 2：CT 图像中异常区域的检测

<details>
<summary>显示提示</summary>

```
Detect and localize abnormal regions in this CT image. Highlight abnormal areas with bounding boxes.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_19205.png" alt="CT 输入图像" width="200"> | <img src="./images/case_19205_gemini.png" alt="CT Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/19205)

### 示例 3：移除 MRI 中的不健康区域 (a)

<details>
<summary>显示提示</summary>

```
Remove the unhealthy or abnormal areas in the images and generate a healthy version of the image.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_18826.png" alt="MRI (a) 输入图像" width="200"> | <img src="./images/case_18826_gemini.png" alt="MRI (a) Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/18826)

### 示例 4：移除 MRI 中的不健康区域 (b)

<details>
<summary>显示提示</summary>

```
Remove the unhealthy or abnormal areas in the images and generate a healthy version of the image.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_19195.png" alt="MRI (b) 输入图像" width="200"> | <img src="./images/case_19195_gemini.png" alt="MRI (b) Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/19195)

### 示例 5：生成大脑的健康版本

<details>
<summary>显示提示</summary>

```
Generate a healthy version of this brain.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_13910_b.png" alt="大脑输入图像" width="200"> | <img src="./images/gemini_case_13910_b.png" alt="健康大脑输出" width="200"> |

[数据资源](https://www.eurorad.org/case/13910)

### 示例 6：注释 MRI 而不改变像素

<details>
<summary>显示提示</summary>

```
Annotate this MRI without altering the original pixels. Add overlays/annotations only.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_7941.png" alt="MRI 输入图像" width="200"> | <img src="./images/case_7941_gemini.png" alt="MRI Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/7941)

### 示例 7：注释手术图像而不改变像素

<details>
<summary>显示提示</summary>

```
Annotate this surgical image without altering the original pixels. Add overlays/annotations only.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case18515.png" alt="手术输入图像" width="200"> | <img src="./images/case18515_gemini.png" alt="手术 Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/18515)

### 示例 8：识别 MRI 中的成像视图和解剖区域

<details>
<summary>显示提示</summary>

```
Identify the imaging view (axial, sagittal, or coronal) and anatomical region shown in this scan.
Overlay a small text label in the corner with the view and body region.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_17344_2.png" alt="MRI 输入图像" width="200"> | <img src="./images/case_17344_2_gemini.png" alt="MRI Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/17344)

### 示例 9：从 MRI 扫描中移除注释

<details>
<summary>显示提示</summary>

```
Remove all annotations, arrows, labels, text, and markers from this scan image. Reconstruct the underlying anatomy naturally and seamlessly, keeping the original texture, contrast, and medical details intact. Do not alter or blur anatomical structures.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_18515.png" alt="MRI 输入图像" width="200"> | <img src="./images/case_18515_gemini.png" alt="MRI Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/18515)

### 示例 10：从手术扫描中移除注释

<details>
<summary>显示提示</summary>

```
Remove all annotations, arrows, labels, text, and markers from this scan image. Reconstruct the underlying anatomy naturally and seamlessly, keeping the original texture, contrast, and medical details intact. Do not alter or blur anatomical structures.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_18816.png" alt="手术输入图像" width="200"> | <img src="./images/case_18816_gemini.png" alt="手术 Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/18816)

### 示例 11：从 MRI 图像中移除颅骨

<details>
<summary>显示提示</summary>

```
Please remove the skull from the image. It appears as the outermost bright white border.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_19196.png" alt="MRI 输入图像" width="200"> | <img src="./images/case_19196_gemini.png" alt="MRI Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/19196)

### 示例 12：从 MRI 图像中移除颅骨（替代方案）

<details>
<summary>显示提示</summary>

```
1. Remove the skull from the image and retain only show the brain region in the final output. 
2. yes correct, but you change the brain, you should not change the brain
```
</details>

| 输入 | 输出1 |输出2 |
|-------|--------|--------|
| <img src="./images/case_17504.png" alt="MRI 输入图像" width="200"> | <img src="./images/case_17504_gemini1.png" alt="MRI Gemini 输出" width="200"> |  <img src="./images/case_17504_gemini2.png" alt="MRI Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/17504)

### 示例 13：从心脏 MRI 生成超声

<details>
<summary>显示提示</summary>

```
Generate a realistic transthoracic echocardiographic (ultrasound) image of the human heart in a similar view and orientation as the provided cardiac MRI image. The image should depict the left ventricle, left atrium, and mitral valve region with clear grayscale ultrasound texture, realistic speckle noise, and anatomical detail. The mitral valve leaflets should be visible with slight curvature consistent with systole. Use appropriate ultrasound shading, acoustic shadowing, and tissue echogenicity. The overall appearance must resemble a real clinical echocardiogram, not a diagram or illustration.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_13950.png" alt="MRI 输入图像" width="200"> | <img src="./images/case_13950_gemini.png" alt="MRI Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/13950)

### 示例 14：从矢状 MRI 生成 3D 脊柱模型

<details>
<summary>显示提示</summary>

```
Generate a realistic 3D anatomical model of the human spine based on the provided sagittal MRI image. The 3D reconstruction must precisely match the curvature, alignment, and proportions of the vertebrae as seen in the MRI. Include detailed vertebral bodies, intervertebral discs, spinal canal, and surrounding soft tissue outlines. Maintain anatomical accuracy of thoracic and lumbar segments, preserving the same posture and sagittal orientation as the original MRI. Render the 3D model in a semi-transparent medical visualization style with realistic bone texture and soft lighting. The result should look like a 3D version of this MRI slice, without any change in direction or angle.
Emphasize: same sagittal view, same curvature, anatomically correct spine model reconstructed from MRI data.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_14834.png" alt="手术输入图像" width="200"> | <img src="./images/case_14834_gemini.png" alt="手术 Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/14834)

### 示例 15：从 3D 腹部重建生成腹部 CT

<details>
<summary>显示提示</summary>

```
Generate abdominal CT image from the 3D abdomen volume reconstruction.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_19173.png" alt="腹部输入图像" width="200"> | <img src="./images/gemini_case_19173.png" alt="CT 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/19173)

### 示例 16：生成大脑的 3D 网格

<details>
<summary>显示提示</summary>

```
Generate a 3D mesh of this brain.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_18099.png" alt="大脑输入图像" width="200"> | <img src="./images/gemini_case_18099.png" alt="3D 网格输出" width="200"> |

[数据资源](https://www.eurorad.org/case/18099)

### 示例 17：生成牙齿的 3D 网格

<details>
<summary>显示提示</summary>

```
Generate a 3D mesh of the teeth.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_17181.png" alt="牙齿输入图像" width="200"> | <img src="./images/gemini_case_17181.png" alt="3D 网格输出" width="200"> |

[数据资源](https://www.eurorad.org/case/17181)

### 示例 18：模拟大脑中肿瘤进展

<details>
<summary>显示提示</summary>

```
The red box indicates the tumor region for reference only — do not display the box in the output.
Simulate advanced-stage tumor progression in that region: enlarge the lesion by approximately 50% relative to the original size.
Keep all other brain anatomy, alignment, and texture identical to the original image, with no artifacts or hallucinated structures.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/17344.png" alt="MRI 输入图像" width="200"> | <img src="./images/17344_gemini.png" alt="MRI Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/17344)

### 示例 19：从大脑扫描中移除病变

<details>
<summary>显示提示</summary>

```
The red box indicates the lesion region to be removed — do not show the box in the output.
Generate a version of the scan with that lesion completely removed, restoring normal tissue appearance and continuity in that region.
Preserve all surrounding brain anatomy, alignment, intensity patterns, and MR noise exactly as in the original image.
The result must look anatomically realistic and artifact-free.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/17344.png" alt="手术输入图像" width="200"> | <img src="./images/17344_gemini_2.png" alt="手术 Gemini 输出" width="200"> |

[数据资源](https://www.eurorad.org/case/17344)

### 示例 20：从 MRI 扫描中移除伪影 (1)
[数据资源](https://www.auntminnieeurope.com/clinical-news/article/15648693/know-your-artifacts-to-optimize-mri-scans)
<details>
<summary>显示提示</summary>
```
Use the provided scan as the anatomical reference.
Remove imaging artifacts or acquisition noise while keeping all brain structures, intensity gradients, and MR texture identical to the original.
Do not alter anatomy, contrast, or alignment.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/artefect.png" alt="带有伪影的 MRI 输入图像" width="200"> | <img src="./images/artefect_gemini.png" alt="移除伪影的 MRI Gemini 输出" width="200"> |

### 示例 21：从 MRI 扫描中移除伪影 (2)
[数据资源](https://link.springer.com/article/10.1007/s00330-006-0470-4)

<details>
<summary>显示提示</summary>

```
Remove the imaging artifacts and restore normal brain tissue appearance while preserving all anatomical structures, symmetry, and MR intensity patterns.
Keep the ventricles, cortex, and white matter boundaries identical to the original scan.
Produce a clean, artifact-free, anatomically faithful version that looks realistic and consistent with standard T1 MRI.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/artefect2.png" alt="带有伪影的 MRI 输入图像" width="200"> | <img src="./images/artefect_gemini2.png" alt="移除伪影的 MRI Gemini 输出" width="200"> |



### 示例 22：分割图像中所有可见器官

<details>
<summary>显示提示</summary>

```
Segment all visible organs in the image..
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_15782.png" alt="原始图像" width="200"> | <img src="./images/case_15782_gemini.png" alt="地面真相掩码" width="200"> |

[数据资源](https://www.eurorad.org/case/15782)

### 示例 23：分割图像中所有可见器官（叠加）

<details>
<summary>显示提示</summary>

```
Segment all visible organs in the image..
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_15782_2.png" alt="Gemini 叠加" width="200"> | <img src="./images/case_15782_2_gemini.png" alt="Gemini 掩码" width="200"> |

[数据资源](https://www.eurorad.org/case/15782)

### 示例 24：生成心脏室的像素级分割

<details>
<summary>显示提示</summary>

```
Generate pixel-level segmentation of the cardiac chambers.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_17698.png" alt="心脏输入图像" width="200"> | <img src="./images/gemini_case_17698.png" alt="分割输出" width="200"> |

[数据资源](https://www.eurorad.org/case/17698)

### 示例 25：生成大脑胶质瘤的像素级分割

<details>
<summary>显示提示</summary>

```
Generate a pixel-level segmentation of the brain glioma.
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_13910.png" alt="大脑输入图像" width="200"> | <img src="./images/gemini_case_13910.png" alt="胶质瘤分割输出" width="200"> |

[数据资源](https://www.eurorad.org/case/13910)

### 示例 26：生成大脑分割

<details>
<summary>显示提示</summary>

```
Generate the brain segmentation
```
</details>

| 输入 | 输出 |
|-------|--------|
| <img src="./images/case_17773.png" alt="大脑输入图像" width="200"> | <img src="./images/gemini_case_17773.png" alt="大脑分割输出" width="200"> |

[数据资源](https://www.eurorad.org/case/17773)


## 📊 数据集
来源：EURORAD (https://eurorad.org)。  
许可证：请参考来源

## 🛠️ 工具

所有示例均使用 [Google AI Studio](https://aistudio.google.com/) 与 Gemini-2.5-Flash-Image 模型生成。温度和 top_p 使用默认参数。

请注意，由于生成 AI 模型的固有变异性，在多次运行中输出可能略有不同。

## 👀 观察

### 优势
在测试期间，我们发现 Nano Banana 展示了出色的多任务处理能力，能够处理各种医学成像任务，包括一些非常规应用，如从 2D 医学扫描图像生成 3D 模型。

### 医学成像应用中的局限性
尽管 Nano Banana 作为通用模型拥有广泛能力，但在医学成像应用中仍有一些局限性：

1. **幻觉问题**：模型倾向于产生幻觉，生成虚假或解剖学不一致的内容，即使在一般领域保持轻微一致性，也会偏离原始医学图像。

2. **处理复杂提示的困难**：Nano Banana 在处理过于复杂或冗长的提示时遇到困难。简洁明了的提示通常会导致更好的对齐结果。

3. **上下文学习能力**：模型具备上下文学习能力。对于出现错误的任务，当指出错误或提供参考示例时，模型可以纠正并改进其性能。

4. **生成随机性**：模型的生成过程本质上是随机的，即使使用温度=0 或控制 top-p 参数，也难以实现完全一致的输出。

5. **在简单任务上的出色表现**：模型在具有清晰数据的简单任务上表现出色，例如从医学扫描图像中移除注释或标签。

6. **多轮推理的增强效果**：多轮迭代推理可以显著提高生成输出的质量和准确性。


## 🤝 贡献

有关详细贡献指南，请参见 [contribution.md](contribution.md)。我们欢迎您贡献以扩展我们的示例集合，并推进对 AI 在医学成像中应用的理解！

## 📖 引用
如果您在研究中使用此资源，请引用：

```bibtex
@misc{awesome_nano_banana_medical,
  title={Awesome Nano Banana for Medical Imaging},
  author={Your Name},
  year={2025},
  publisher={GitHub},
  howpublished={\url{https://github.com/yourusername/awesome-nanobannan-for-medical-imaging}}
}
```

## 🙏 感谢

感谢以下仓库的作者和维护者提供的灵感：

- [JimmyLv/awesome-nano-banana](https://github.com/JimmyLv/awesome-nano-banana)
- [PicoTrex/Awesome-Nano-Banana-images](https://github.com/PicoTrex/Awesome-Nano-Banana-images)