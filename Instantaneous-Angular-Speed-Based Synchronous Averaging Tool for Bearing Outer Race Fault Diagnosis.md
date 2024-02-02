---
tags: []
parent: 'Instantaneous-Angular-Speed-Based Synchronous Averaging Tool for Bearing Outer Race Fault Diagnosis'
collections:
    - 论文2
version: 45868
libraryID: 1
itemKey: FYTR4M64

---
# Instantaneous-Angular-Speed-Based Synchronous Averaging Tool for Bearing Outer Race Fault Diagnosis

## Abstract

同步平均是一种强大的信号处理工具，它可以用于增强我们感兴趣的周期事件。然而滚动轴承外圈故障特征在随机滑动的情况下可能无法被同步平均有效增强。为此，在本文中提出了两种基于瞬时角速度的同步平均框架。随后提出了一种改进的负熵指标以表征滚动轴承故障信息中的丰富程度。此外，基于IAS信号估计特征，研究了编码器分辨率和结构阻尼因子对故障轴承波形的影响。仿真和实验结果表明提出的方法能够用于增强随机滑动下的滚动轴承故障。

## I. INTRODUCTION

引言思路：

par1：<span style="color: #ffcb00">交代背景引出IAS。</span>轴承重要性。👉轴承故障引起轴瞬时角位移发生变化，引出编码器可以用于滚动轴承故障诊断。举出若干利用编码器进行状态监测的现有研究。👉IAS比IAS更敏感。因此IAS-Based逐渐成为故障诊断领域的新兴课题。

par2：<span style="color: #ffcb00">铺垫传统SA为什么不能继续适用。</span>此外同步平均是一种流行的技术通过抑制非同步成分来提高信号的信噪比。文献11、12、13都在不同的诊断上应用SA-Based 方法。但是值得注意的是，传统的SA在齿轮啮合成分上、转频谐波等一阶循环平稳上有着出色的增强作用。另一方面，IAS虽然与转速无关，但滚动轴承由于滑动产生了二阶循环平稳IAS分量。👉因此，传统的SA不能用于增强与REB故障相关的特征。

par3：<span style="color: #ffcb00">介绍自己的contribution。</span>进一步描述摘要里面提到了两种方法。

par4：<span style="color: #ffcb00">介绍文章每部分的工作。</span>

## II. MEASUREMENT OF THE IAS

简介编码器的原理以及瞬时角速度的计算方法。

## III. WAVEFORM FEATURE OF FAULTY REB

### A. Model of Faulty REB

![\<img alt="" data-attachment-key="MNVG7LTZ" width="572" height="87" src="attachments/MNVG7LTZ.png" ztype="zimage">](attachments/MNVG7LTZ.png)

这个式子定义了滚动轴承故障的轴瞬时角位移。

### B. Effect of Main Parameters on Waveform

1.讨论阻尼因子对波形的影响

2.讨论编码器分辨率对波形的影响

3.<span style="color: #ff2020">尽管较大的编码器分辨率消弱了故障对应的IAS波形的幅值，但仍然保留了与外圈故障相关的冲击特征。 此外，基于波形形状的特征指标可能无法揭示REB的相关特征，因为不同的编码器分辨率会导致IAS信号形状的不同。不过幸运的是，冲击指标和周期性指标可以用于IAS-BASED的轴承故障诊断方法研究。</span>

## IV. ANGULAR PERIOD OF FAULTY REB

![\<img alt="" data-attachment-key="JGDUS8R3" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FSD8MVJL3%22%2C%22annotationKey%22%3A%22DVE5K8WZ%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%226252%22%2C%22position%22%3A%7B%22pageIndex%22%3A2%2C%22rects%22%3A%5B%5B358.75%2C321.167%2C561.667%2C345.333%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FD7329F2B%22%5D%2C%22locator%22%3A%226252%22%7D%7D" width="338" height="40" src="attachments/JGDUS8R3.png" ztype="zimage">](attachments/JGDUS8R3.png)

由随机滑动所引起的二阶循环平稳变量定义式。

上述重新定义了考虑随机滑动的REB故障角度周期。

## V. TWO IAS-BASED SA FRAMEWORKS

<span style="color: #ffcb00">Methodology</span>

### A 传统的SA

<span style="background-color: #a28ae580">简述传统SA，给出公式。点明传统的SA无法适用于有滑动的REB故障。</span>

### B 准备工作

#### 1）重采样

因为存在的滑动与滚动轴承故障相关冲击衰减振荡的角度区间是一个二阶循环平稳变量。

另一方面，传统的降采样操作会丢失故障信息，因为未考虑冲击前后存在的滑移差。

![\<img alt="" data-attachment-key="AVZ67TSN" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FSD8MVJL3%22%2C%22annotationKey%22%3A%224SZVCHTY%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%226253%22%2C%22position%22%3A%7B%22pageIndex%22%3A3%2C%22rects%22%3A%5B%5B298.75%2C601.5833333333334%2C536.25%2C730.75%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FD7329F2B%22%5D%2C%22locator%22%3A%226253%22%7D%7D" width="396" height="215" src="attachments/AVZ67TSN.png" ztype="zimage">](attachments/AVZ67TSN.png)

#### 2）改进负熵

$$
\operatorname{Sh}(x)=\wp_{1}(x) \wp_{2}(x)
$$

$\wp_1(x)$是标准差，它用于表征能量的偏差。

$\wp_2(x)$是负熵的计算，基于自适应软阈值工具MAD可以减少背景噪声的干扰

#### 3）提出的方法

![\<img alt="" data-attachment-key="Z9BGYJJY" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FSD8MVJL3%22%2C%22annotationKey%22%3A%22GPJTFCSA%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%226254%22%2C%22position%22%3A%7B%22pageIndex%22%3A4%2C%22rects%22%3A%5B%5B319.853%2C413.912%2C540.441%2C729.794%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FD7329F2B%22%5D%2C%22locator%22%3A%226254%22%7D%7D" width="368" height="527" src="attachments/Z9BGYJJY.png" ztype="zimage">](attachments/Z9BGYJJY.png)

#### 1）Indicator-Based SA(ISA)

⭐上述左图就是ISA（详见论文）

#### 2) Cyclic Dislocation Averaging

⭐上述右图（详见论文）

#### 3) Computational Cost

#### 4) Discussion

## VI. VALIDATION

为了验证所提方法得有效性，分别对比了传统得同步平均算法和谱相干算法。

### A. Simulation

生成仿真编码器信号

![\<img alt="" data-attachment-key="WXINWHE6" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FSD8MVJL3%22%2C%22annotationKey%22%3A%22UVI7FKMB%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%226257%22%2C%22position%22%3A%7B%22pageIndex%22%3A7%2C%22rects%22%3A%5B%5B28.125%2C520.594%2C293.438%2C733.875%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FD7329F2B%22%5D%2C%22locator%22%3A%226257%22%7D%7D" width="442" height="355" src="attachments/WXINWHE6.png" ztype="zimage">](attachments/WXINWHE6.png)

![\<img alt="" data-attachment-key="4VWKRR7D" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FSD8MVJL3%22%2C%22annotationKey%22%3A%22L24ZS4WM%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%226257%22%2C%22position%22%3A%7B%22pageIndex%22%3A7%2C%22rects%22%3A%5B%5B27.188%2C389.812%2C292.5%2C514.969%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FD7329F2B%22%5D%2C%22locator%22%3A%226257%22%7D%7D" width="442" height="209" src="attachments/4VWKRR7D.png" ztype="zimage">](attachments/4VWKRR7D.png)

![\<img alt="" data-attachment-key="3946JECV" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FSD8MVJL3%22%2C%22annotationKey%22%3A%22YHTLHUR6%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%226257%22%2C%22position%22%3A%7B%22pageIndex%22%3A7%2C%22rects%22%3A%5B%5B30%2C261.844%2C292.03125%2C382.78099999999995%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FD7329F2B%22%5D%2C%22locator%22%3A%226257%22%7D%7D" width="437" height="202" src="attachments/3946JECV.png" ztype="zimage">](attachments/3946JECV.png)

![\<img alt="" data-attachment-key="6PY2J32D" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FSD8MVJL3%22%2C%22annotationKey%22%3A%22G488MZDW%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%226257%22%2C%22position%22%3A%7B%22pageIndex%22%3A7%2C%22rects%22%3A%5B%5B296.71875%2C472.3119999999999%2C555%2C733.8749999999999%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FD7329F2B%22%5D%2C%22locator%22%3A%226257%22%7D%7D" width="430" height="435" src="attachments/6PY2J32D.png" ztype="zimage">](attachments/6PY2J32D.png)

### B. Experiments

通过对两种不同的工况实验数据（with and without gear mesh）进行分析、处理、对比，如图所示：

![\<img alt="" data-attachment-key="P9N8QY27" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FSD8MVJL3%22%2C%22annotationKey%22%3A%22LPUYJ6M2%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%226258%22%2C%22position%22%3A%7B%22pageIndex%22%3A8%2C%22rects%22%3A%5B%5B38.046437149719765%2C303.579%2C297.238%2C580.367%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FD7329F2B%22%5D%2C%22locator%22%3A%226258%22%7D%7D" width="432" height="461" src="attachments/P9N8QY27.png" ztype="zimage">](attachments/P9N8QY27.png)

![\<img alt="" data-attachment-key="IIQZ3CR4" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FSD8MVJL3%22%2C%22annotationKey%22%3A%22J5ZSGSQT%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%226258%22%2C%22position%22%3A%7B%22pageIndex%22%3A8%2C%22rects%22%3A%5B%5B300.091%2C604.146%2C559.758%2C723.992%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FD7329F2B%22%5D%2C%22locator%22%3A%226258%22%7D%7D" width="433" height="200" src="attachments/IIQZ3CR4.png" ztype="zimage">](attachments/IIQZ3CR4.png)

![\<img alt="" data-attachment-key="FM85PB38" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FSD8MVJL3%22%2C%22annotationKey%22%3A%224EFHYFUB%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%226258%22%2C%22position%22%3A%7B%22pageIndex%22%3A8%2C%22rects%22%3A%5B%5B300.091%2C340.674%2C559.283%2C597.963%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F9613257%2Fitems%2FD7329F2B%22%5D%2C%22locator%22%3A%226258%22%7D%7D" width="432" height="429" src="attachments/FM85PB38.png" ztype="zimage">](attachments/FM85PB38.png)

## VII. CONCLUSION

提出了两种基于IAS的SA框架，用于增强随机滑动条件下REB故障的相关特性。然后，引入改进的负熵指标来评估冲击波形是否严格对齐，并表征与REB故障相关的能量流。进一步研究了故障相关波形与编码器分辨率之间的关系，为两次最大随机滑动采样保留故障相关的衰减脉冲振荡特性提供了支持。仿真和实验结果表明，所提出的方案可用于增强REB相关的故障特征。 值得一提的是，在未来的工作中，将进一步研究鲁棒性更高的特征指标，因为在低信噪比条件下，不合适的特征指标可能无法增强与REB故障相关的特征。
