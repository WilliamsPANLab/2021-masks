<a id="toc"></a>
# Contents
1.) [Summary](#summary)  
2.) [Usage](#usage)  
3.) [Definitions](#definitions)  
&nbsp;&nbsp;&nbsp;&nbsp; 3.1) [Default Mode Circuit](#dmn)  
&nbsp;&nbsp;&nbsp;&nbsp; 3.2) [Salience Circuit](#salience)  
&nbsp;&nbsp;&nbsp;&nbsp; 3.3) [Attention Circuit](#attention)  
&nbsp;&nbsp;&nbsp;&nbsp; 3.4) [Negative Affect Circuit: Sad](#neg_affect_sad)  
&nbsp;&nbsp;&nbsp;&nbsp; 3.5) [Negative Affect Circuit: Threat Conscious](#neg_affect_threat_conscious)  
&nbsp;&nbsp;&nbsp;&nbsp; 3.6) [Negative Affect Circuit: Threat Nonconscious](#neg_affect_threat_nonconscious)  
&nbsp;&nbsp;&nbsp;&nbsp; 3.7) [Positive Affect Circuit: Happy](#pos_affect_happy)  
&nbsp;&nbsp;&nbsp;&nbsp; 3.8) [Cognitive Control Circuit](#cognitive_control)  

<a id="summary"></a>
## [^](#toc) Summary  

This folder includes the ROI regions used in the Williams 2021 Biological Psychiatry paper:

<b>Mapping neural circuit biotypes to symptoms and behavioral dimensions of depression and anxiety</b>

Andrea N Goldstein-Piekarski<sup>†</sup>, Tali M Ball<sup>†</sup>, Zoe Samara<sup>‡</sup>, Brooke R Staveland<sup>‡</sup>, Arielle S. Keller<sup>‡</sup>, Scott L Fleming<sup>‡</sup>, Katherine A Grisanzio<sup>‡</sup>, Bailey Holt-Gosselin<sup>‡</sup>, Patrick Stetz<sup>‡</sup>, Jun Ma<sup>‡</sup>, & Leanne M Williams

<a id="usage"></a>
## [^](#toc) Usage

Please include the following citation:

>Goldstein-Piekarski A, Ball T, Samara Z, Staveland B, Keller A, Fleming S, Grisanzio K, Holt-Gosselin B, Stetz P, Ma J, & Williams L. Mapping neural circuit biotypes to symptoms and behavioral dimensions of depression and anxiety. Biological Psychiatry. 2021; doi: ??? 

To download the files, please click [here](https://github.com/WilliamsPANLab/2021-masks/archive/refs/heads/master.zip) or clone the repository


<a id="definitions"></a>
## [^](#toc) Definitions

<a id="dmn"></a>
#### [^](#toc) Default Mode Circuit
| Circuit Type | Condition | Task Contrast | Neurosynth Search criteria |
| ------ | ------ | ----- | ----- |
| Intrinsic | Task-free | --- | Terms = "default mode"; "resting state"; <br><br> Number of studies = 516; 825 <br><br> Search Date = 6.4.17 |

<br>

| Region label | Region anatomy | Z Value | Template coordinates and definitions |
| --- | --- | --- | --- | 
| D1 | amPFC   | 22.0    | -2, 50, -6 |
| D2 | AG L    | 26.1    | -46, -70, 32 |
| D3 | AG R    | 20.6    | 50, -62, 26 |
| D4 | PCC     | 29.8    | 0, -50, 28 |

<br>

| Computed inputs | Anatomical combinations | Input metric | Circuit Dysfunction Score Formula |
| --- | --- | --- | --- | 
| C<sub>D1,D2</sub> |  amPFC with AG L | Intrinsic FC | |  
| C<sub>D1,D3</sub> | amPFC with AG R | Intrinsic FC | | 
| C<sub>D1,D4</sub> | amPFC with PCC | Intrinsic FC | (C<sub>D1,D2</sub> + C<sub>D1,D3</sub> + C<sub>D1,D4</sub> + C<sub>D2,D4</sub> + C<sub>D3,D4</sub>)/5 |
| C<sub>D2,D4</sub> | AG L with PCC  | Intrinsic FC | |   
| C<sub>D3,D4</sub> | AG R with PCC  | Intrinsic FC | | 

<br>

---

<a id="salience"></a>
#### [^](#toc) Salience Circuit
| Circuit Type |   Condition | Task Contrast | Neurosynth Search criteria |
| --- | --- | --- | --- | 
| Intrinsic | Task-free | --- | Terms = "salience network"; "salience" <br><br> Number of studies = 60; 269 <br><br> Search Date = 6.4.17 |
 
 <br>
 
 | Region label |  Region anatomy | Z Value | Template coordinates and definitions |
| --- | --- | --- | --- | 
|  S1  |   aI L |   11.9 |   -38, 14, -6 |
|  S2  |   aI R |   14.8 |   38, 18, 2 |
|  S3  |   Amygdala L  |    6.9  |   AAL |
|  S4  |   Amygdala R  |    14.7  |  AAL |

 <br>

| Computed inputs  |      Anatomical combinations | Input Metric     | Circuit Dysfunction Score Formula |
 | --- | --- | --- | --- | 
|  C<sub>S1,S3</sub> | aI L with Amygdala L  |  Intrinsic FC | |
|  C<sub>S2,S4</sub> | aI R with Amygdala R  |  Intrinsic FC | (-C<sub>S1,S3</sub> - C<sub>S2,S4</sub> - C<sub>S1,S2</sub>)/3 |   
|  C<sub>S1,S2</sub> | aI L with aI R  | Intrinsic FC | |

<br>

---

<a id="attention"></a>
#### [^](#toc) Attention Circuit
 | Circuit Type |   Condition | Task Contrast | Neurosynth Search criteria |
| --- | --- | --- | --- | 
| Intrinsic | Task-free | --- | Terms = "frontoparietal network"; "attention" <br><br> Number of studies = 1447; 79 <br><br> Search Date = 6.4.17 |

<br>

| Region label | Region anatomy | Z Value | Template coordinates and definitions |
 | --- | --- | --- | --- | 
|  A1  |   msPFC  | 10.4  |  -2, 14, 52 |
|  A2  |   LPFC L | 13.9  |  -44, 6, 32 |
|  A3  |   LPFC R | 11.3  |  50, 10, 28 |
|  A4  |   aIPL L | 10.4  |  -30, -54, 40 |
|  A5  |   aIPL R | 10.4  |  38, -56, 48 |
|  A6  |   Precuneus L  |   13.0  |  -14, -66, 52 |
|  A7  |   Precuneus R  |   11.3  |  18, -68, 52 |

<br>

| Computed inputs | Anatomical combinations | Input metric | Circuit Dysfunction Score Formula |
 | --- | --- | --- | --- | 
| C<sub>A1,A4</sub> | msPFC with aIPL L   |     Intrinsic FC |  |
| C<sub>A1,A5</sub> | msPFC with aIPL R  |     Intrinsic FC |  |
| C<sub>A2,A4</sub> | LPFC L with aIPL L  |    Intrinsic FC | (- C<sub>A1,A4</sub> - C<sub>A1,A5</sub> - C<sub>A2,A4</sub> - C<sub>A3,A5</sub> - C<sub>A4,A6</sub> - C<sub>A5,A7</sub>)/6 |
| C<sub>A3,A5</sub> | LPFC R with aIPL R  |    Intrinsic FC
| C<sub>A4,A6</sub> | aIPL L with precuneus L | Intrinsic FC
| C<sub>A5,A7</sub> | aIPL R with precuneus R | Intrinsic FC

<br>

---

<a id="neg_affect_sad"></a>
#### [^](#toc) Negative Affect Circuit: Sad
| Circuit Type | Condition | Task Contrast | Neurosynth Search Criteria |
| --- | --- | --- | --- |
| Task-evoked | Conscious Facial Emotion Viewing | Sad vs Neutral based on standardized facial emotion stimuli | Term = "threat" <br> Number of studies = 170 <br> Search Date = 6.4.17 |

<br>

| Region label | Region anatomy | Z Value | Template coordinates and definitions |
| --- | --- | --- | --- |
| N1 |     pgACC* | 6.3  |   6, 42, 4 |
| N2 |     aI L   | 17.4 |   -36, 20, -4 |
| N3 |     aI R   | 16.1 |   38, 22, -4 |
| N4 |     Amygdala L |     28.4  |  AAL |
| N5 |     Amygdala R |     25.2  |  AAL |

<br>

| Computed inputs | Anatomical combinations | Input Metric | Circuit Dysfunction Score Formula |
| --- | --- | --- | --- |
| A<sub>N1</sub>     | pgACC*  | BOLD activation | |
| A<sub>N2</sub>     | aI L    | BOLD activation | |
| A<sub>N3</sub>     | aI R    | BOLD activation | |
| A<sub>N4</sub>     | Amygdala L |     BOLD activation | |
| A<sub>N5</sub>     | Amygdala R |     BOLD activation | (A<sub>N1</sub> + A<sub>N2</sub> + A<sub>N3</sub> + A<sub>N4</sub> + A<sub>N5</sub> – C<sub>N1,N2</sub> – C<sub>N1,N3</sub> + C<sub>N1,N4</sub> + C<sub>N1,N5</sub>)/9 |
| C<sub>N1,N2</sub>* | [pgACC to aI L + aI L to pgACC]/2 |      PPI | |
| C<sub>N1,N3</sub>* | [pgACC to aI R + aI R to pgACC]/2 |      PPI | |
| C<sub>N1,N4</sub>* | [pgACC to Amygdala L + Amygdala L to pgACC]/2 |  PPI | |
| C<sub>N1,N5</sub>* | [pgACC to Amygdala R + Amygdala R to pgACC]/2 |  PPI | |

<br>

---

<a id="neg_affect_threat_conscious"></a>
#### [^](#toc) Negative Affect Circuit: Threat Conscious

| Circuit Type |  Condition | Task Contrast | Neurosynth Search Criteria |
| --- | --- | --- | --- |
| Task-evoked | Conscious Facial Emotion Viewing | Fear/Anger vs Neutral based on standardized facial emotion stimuli | Term = "threat" <br><br> Number of studies = 170 <br><br> Search Date = 6.4.17 |

<br>

| Region label | Region anatomy | Z Value | Template coordinates and definitions |
| --- | --- | --- | --- |
| T1 |     dACC   | 8.2    | 6, 22, 32 |
| T2 |     Amygdala L      | 28.4 | AAL |
| T3 |     Amygdala R      | 25.2 | AAL |

<br>

| Computed inputs | Anatomical combinations | Input Metric | Circuit Dysfunction Score Formula |
| --- | --- | --- | --- |
| A<sub>T1</sub>   |  dACC |   BOLD activation | |
| A<sub>T2</sub>   |  Amygdala L |     BOLD activation  | |
| A<sub>T3</sub>   |  Amygdala R |     BOLD activation | (-A<sub>T1</sub> + A<sub>T2</sub> + A<sub>T3</sub> -C<sub>T1,T2</sub> - C<sub>T1,T3</sub>)/5 |
| C<sub>T1,T2</sub> | [dACC to Amygdala L + Amygdala L to  dACC]/2  |  PPI | |
| C<sub>T1,T3</sub> | [dACC to Amygdala R + Amygdala R to dACC]/2  |   PPI | |

<br>

---

<a id="neg_affect_threat_nonconscious"></a>
#### [^](#toc) Negative Affect Circuit: Threat Nonconscious

| Circuit Type | Condition | Task Contrast | Neurosynth Search Criteria |
| --- | --- | --- | --- |
| Task-evoked | Nonconscious Facial Emotion Viewing | Fear/Anger vs Neutral based on standardized facial emotion stimuli | Term = "threat" <br><br> Number of studies = 170 <br><br> Search Date = 6.4.17 |

| Region label | Region anatomy | Z Value | Template coordinates and definitions |
| --- | --- | --- | --- |
| T1 |     sgACC†  | 5.6    | 4, 26, -10
| T2 |     Amygdala L     | 28.4   | AAL
| T3 |     Amygdala R     | 25.2   | AAL

| Computed inputs | Anatomical combinations | Input Metric | Circuit Dysfunction Score Formula |
| --- | --- | --- | --- |
| A<sub>T1</sub> | sgACC†  | BOLD activation | |
| A<sub>T2</sub> | Amygdala L     | BOLD activation | |
| A<sub>T3</sub> | Amygdala R     | BOLD activation | (-A<sub>T1</sub> + A<sub>T2</sub> + A<sub>T3</sub> -C<sub>T1,T2</sub> - C<sub>T1,T3</sub>)/5 |
| C<sub>T1,T2</sub>† | [sgACC  to Amygdala L + Amygdala L to  sgACC]/2 | PPI | |
| C<sub>T1,T3</sub>† | [sgACC to Amygdala R + Amygdala R to  sgACC]/2  | PPI | |

<br>

---

<a id="pos_affect_happy"></a>
#### [^](#toc) Positive Affect Circuit: Happy

| Circuit Type | Condition | Task Contrast | Neurosynth Search Criteria |
| --- | --- | --- | --- |
| Task-evoked | Conscious Facial Emotion Viewing | Happy vs Neutral based on standardized facial emotion stimuli | Terms = "monetary reward"; "reward" <br><br> Number of studies = 84; 671 <br><br> Search Date = 6.4.17 |

| Region label | Region anatomy | Z Value | Template coordinates and definitions |
| --- | --- | --- | --- |
| P1 |     vMPFC  | 13.1  |  -2, 56, -8 |
| P2 |     Striatum L  |    14.0  |  FSL |
| P3 |     Striatum R  |    7.9   |  FSL |

| Computed inputs | Anatomical combinations | Input Metric | Circuit Dysfunction Score Formula |
| --- | --- | --- | --- |
| A<sub>P1</sub> |    vMPFC  | BOLD activation | |
| A<sub>P2</sub> |    Striatum L |     BOLD activation | (-A<sub>P1</sub> - A<sub>P2</sub> - A<sub>P3</sub>)/3 |
| A<sub>P3</sub> |    Striatum R |     BOLD activation | |

<br>

---

<a id="cognitive_control"></a>
#### [^](#toc) Cognitive Control Circuit   

| Circuit Type | Condition | Task Contrast | Neurosynth Search Criteria |
| --- | --- | --- | --- |
| Task-evoked | Go-NoGo task | No-Go vs. Go | Terms = "cognitive control" <br><br> Number of studies = 428 <br><br> Search Date = 6.4.17 |

| Region label | Region anatomy | Z Value | Template coordinates and definitions |
| --- | --- | --- | --- |
| C1 |     dACC    | 20.0 |   0, 18, 46 |
| C2 |     DLPFC L | 20.4 |   -44, 6, 32 |
| C3 |     DLPFC R | 12.4 |   44, 34, 22 |

| Computed inputs | Anatomical combinations | Input Metric | Circuit Dysfunction Score Formula |
| --- | --- | --- | --- |
| A<sub>C1</sub>    | dACC    | BOLD activation | |
| A<sub>C2</sub>    | DLPFC L | BOLD activation | |
| A<sub>C3</sub>    | DLPFC R | BOLD activation | (-A<sub>C1</sub>- A<sub>C2</sub> - A<sub>C3</sub> - C<sub>C1,C2</sub> - C<sub>C1,C3</sub>)/5 |
| C<sub>C1,C2</sub> | [dACC to DLPFC L + DLPFC L to dACC]/2  | PPI | |
| C<sub>C1,C3</sub> | [dACC to DLPFC R + DLPFC R to dACC]/2  | PPI | |

*The pgACC peaks were defined by decreasing the minimum cluster distance in the 3dCluster algorithm.

†Although the sgACC did not meet our quality control metrics for temporal signal-to-noise ratio, given both the difficulty of imaging this region and its importance of this region to defining the negative affect circuit elicited by implicit threat stimuli and to prior imaging findings in depression, we report supplementary analyses including this region.
