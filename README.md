# MAD-SZAD

**MAD-SZAD** is a privacy-compliant clinical multimodal dataset for schizophrenia and Alzheimer's disease analysis in real doctor-patient interview scenarios.

It is associated with the following work:

**Causal-Guided Multimodal Diagnosis of Schizophrenia and Alzheimer’s Disease with MADD-CG and MAD-SZAD**

---

# Overview

Schizophrenia (SZ) and Alzheimer's disease (AD) may exhibit overlapping negative symptoms such as blunted affect, alogia, emotional flattening, and social withdrawal, increasing the risk of misdiagnosis in clinical practice.

MAD-SZAD is designed to support research on:

- multimodal psychiatric diagnosis
- robust learning under missing modalities
- question-slot-level incomplete multimodal analysis
- interpretable clinical AI
- causal-guided multimodal modeling

The dataset was collected from real doctor-patient interviews at **Guangzhou Kangning Hospital** under clinical settings.

---

# Dataset Statistics

The MAD-SZAD dataset contains **80 clinically confirmed participants**.

| Category | Male | Female | Total |
|----------|------|--------|-------|
| SZ       | 25   | 15     | 40    |
| AD       | 21   | 19     | 40    |
| Total    | 46   | 34     | 80    |

The dataset includes multimodal behavioral recordings and structured psychiatric interview information.

---

# Modalities

MAD-SZAD currently includes:

- Audio recordings
- Video recordings
- Structured PANSS-related interview responses
- Multimodal feature representations

---

# Clinical Interview Scenario

All recordings were collected in real doctor-patient interview scenarios.

The interviews were designed to evaluate:

- emotional state
- self-perception
- guilt cognition
- delusional tendency
- social cognition
- mission-related beliefs
- abnormal self-reference
- psychotic symptom-related behaviors

---

# Clinical Interview Questions

The interview protocol contains the following structured psychiatric assessment questions.

| Question ID | Question Content |
|-------------|-----------------|
| Q1 | In the past week, have you felt worried, tense, or uneasy? Have you been mostly calm and relaxed, or tense and fearful? |
| Q2 | How has your physical condition been over the past week? Are you in your best state? Any physical illnesses bothering you? |
| Q3 | How has your mood been over the past week? On a scale from 0 to 10, how would you rate yourself? Any unhappy or sad experiences? |
| Q4 | Compared with others, do you feel you are better or worse? In which aspects are you better or worse? |
| Q5 | Do you feel there is anything special about you? Do you consider yourself a genius or an ordinary person? Any extraordinary talents? Do you have any special powers or superpowers? Can you know what others are thinking without them speaking? |
| Q6 | Have you done anything in the past that makes you feel guilty or regretful now? Do you feel you deserve punishment? |
| Q7 | Are you very wealthy? Or just ordinary? Do others consider you famous? Can people see you on TV or in the newspapers? |
| Q8 | Do you feel you have a special mission or task in life? |

---

# Question-to-File Mapping

The filename suffix corresponds to different interview questions.

| File Suffix | Corresponding Question |
|-------------|------------------------|
| -2          | Q1 |
| -3, -4      | Q2 |
| -5          | Q3 |
| -6          | Q4 |
| -7, -8, -9, -10 | Q5 |
| -15         | Q6 |
| -11, -12, -13 | Q7 |
| -14         | Q8 |

Example:

```text
100001-7.csv → Q5
```

---

# Data Organization

The dataset is organized as follows:

```text
DATA/
├── audio_AD/
│   ├── 100001/
│   │   ├── 100001-1.csv
│   │   ├── ...
│   ├── 100002/
│   └── ...
│
├── audio_SZ/
│
├── video_AD/
│
└── video_SZ/
```

Each participant folder contains multimodal recordings and structured feature files corresponding to different interview questions.

---

# Feature Extraction Pipeline

## Visual Features

Visual features are extracted using MediaPipe Face Detection and Face Mesh pipelines.

- Face detection
- Face mesh landmark extraction
- Facial behavior analysis
- Geometric facial representation

Example visual pipeline:

```text
MediaPipe Face Detection
MediaPipe Face Mesh
```

---

## Audio Features

Audio features include:

- Pitch
- Loudness Energy
- Formants (F1, F2, F3)
- Spectral Features
- Voice Quality
- Temporal Features

The extracted features are organized into structured feature matrices for multimodal learning.

---

# Supported Tasks

MAD-SZAD can support the following tasks:

1. Schizophrenia vs. Alzheimer's disease classification
2. Multimodal diagnosis under missing modalities
3. Question-slot-level incomplete input analysis
4. Causal-knowledge-guided multimodal modeling
5. Interpretable psychiatric diagnostic research
6. Robust multimodal fusion research
7. Clinical behavioral representation learning

---

# Dataset Features

- Real clinical interview setting
- Multimodal audio-video behavioral data
- Structured PANSS-related symptom information
- Cross-disease psychiatric diagnosis
- Suitable for causal graph learning
- Suitable for multimodal incomplete learning
- Clinically interpretable multimodal representations
- Privacy-compliant clinical data organization

---

# Repository

GitHub repository:

- https://github.com/huiguoo28256/MAD-SZAD

---

# Access

Due to privacy, ethics, and clinical data governance requirements, the raw dataset is **not directly downloadable at this stage**.

The dataset page and access information are provided here:

- Dataset page: https://huiguoo28256.github.io/MAD-SZAD/
- Access request: please contact the corresponding author by email

If a processed or de-identified version is released in the future, this section will be updated accordingly.

---

# Ethics Statement

All data collection procedures complied with institutional ethical requirements and patient privacy regulations.

Personally identifiable information has been removed or anonymized where necessary.

The dataset is intended strictly for academic and research purposes.

---

# Paper

This dataset is associated with the following manuscript:

**Causal-Guided Multimodal Diagnosis of Schizophrenia and Alzheimer’s Disease with MADD-CG and MAD-SZAD**

**Authors:** Weiqi Chen, Chuanhui Han

**Status:** Unpublished manuscript / under preparation

**Paper link:** Coming soon

---

# Citation

If you use MAD-SZAD in your research, please cite the following manuscript:

```bibtex
@article{mad_szad_2026,
  title   = {Causal-Guided Multimodal Diagnosis of Schizophrenia and Alzheimer’s Disease with MADD-CG and MAD-SZAD},
  author  = {Weiqi Chen and Chuanhui Han},
  journal = {Manuscript in preparation},
  year    = {2026}
}
```

---

# License

This repository page is for academic and informational use only.

The dataset itself is subject to:

- clinical data governance
- privacy protection
- ethical approval
- usage authorization requirements

Please do not redistribute any dataset files without permission.

---

# Contact

For questions regarding the dataset, collaboration, or access requests, please contact:

- Chuanhui Han: 3075309697@qq.com

---

# Acknowledgement

MAD-SZAD was constructed with the support of Guangzhou Kangning Hospital and is intended to support research on robust and interpretable multimodal diagnosis for schizophrenia and Alzheimer's disease under real-world clinical interview settings.
