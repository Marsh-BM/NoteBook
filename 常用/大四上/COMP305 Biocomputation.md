# COMP305 Biocomputation

## Lecture 1

### 1.1 Outline 

![image-20230926180434241](D:\笔记\笔记图片\image-20230926180434241.png)

![image-20230926180504624](D:\笔记\笔记图片\image-20230926180504624.png)

![image-20230926180646059](D:\笔记\笔记图片\image-20230926180646059.png)

### 1.2 Interview

![image-20230926180926992](D:\笔记\笔记图片\image-20230926180926992.png)

* 当被视为信息技术时，生物系统显然具有巨大的能力，可以作为控制系统，**用于敏捷性或调节、模式识别、适应性、信息存储、传感器融合以及计算机科学家、计算机工程师和任何对it相关研究感兴趣的人所关心的其他信息处理任务**。在这些领域和其他领域，生物学的表现水平比硅基系统好许多个数量级。我们相信，在生物学和信息技术的接口上进行研究，可以引出新的重要的信息系统(算法和软件)和计算机技术(硬件)。问题是我们能从生物系统中学到什么以及如何理解，以及我们如何采用它们并使它们适应以发展这些新的计算机技术





* **生物**
  * **Biology discoveries and research motivates the biological computation (algorithms), while biological computation can help biologist understand clearer biology phenomenon and better explore the mechanism.**
  * **生物学的发现和研究激发了生物计算(算法)，而生物计算可以帮助生物学家更清晰地理解生物现象，更好地探索其机制。**

![image-20230926180942311](D:\笔记\笔记图片\image-20230926180942311.png)

生物计算已被用作生物学和计算界面研究的一个包罗万象的术语。为了避免混淆，我们提出生物计算的一般领域可以分为四大类



* **生物分子计算 Biomolecular Computation** 这一类包括**利用生物大分子来实现相对标准的计算方法**。例如DNA计算，使用细菌视紫红质和生物改变细胞的存储介质，在传统计算范式中进行基本操作。

![image-20230926181555315](D:\笔记\笔记图片\image-20230926181555315.png)

* **计算生物学 Computational Biology** 这一类别包括任何通过**应用计算方法和工具来解决生物学问题**，以模拟生物学和解决生物行为的详细数学表达式。
  * 例子包括从第一性原理计算的方法，如Ab
    Initio, Monte Carlo或其他模拟程序应用于观察蛋白质-蛋白质相互作用，蛋白质折叠，药物结合位点解析等。

![image-20230926181732016](D:\笔记\笔记图片\image-20230926181732016.png)

* **生物信息学 Bioinformatics** 这一类别包括**数据管理、数据挖掘、数据建模和算法技术在生物数据库中的应用**，如基因组数据库和相关的测序信息。
  * 例子包括作为基因功能预测方法的计算机模型和用于推断和确定序列同源性信息的数据挖掘。

![image-20230926182024803](D:\笔记\笔记图片\image-20230926182024803.png)

* **生物计算学 Biological Computation** 这一类包括**确定生物学如何从亚细胞水平到系统和人口水平(例如生态学、经济和大脑)进行信息技术**

### 1.3 Biological Computation (Algorithms)

* 传统的程序流程如下图所示：

![image-20230926182700455](D:\笔记\笔记图片\image-20230926182700455.png)

![image-20230926182755518](D:\笔记\笔记图片\image-20230926182755518.png)

* 但是很明显有些地方不太能使用传统方法，因为太复杂

![image-20230926182812466](D:\笔记\笔记图片\image-20230926182812466.png)

* 流程更倾向于从输入和结果得到新的程序来解决类似的问题。

![image-20230926182923489](D:\笔记\笔记图片\image-20230926182923489.png)

* 与传统编程不同，机器学习是一个自动化的过程。它可以在许多领域增加嵌入式分析的价值，包括数据准备、自然语言接口、自动异常值检测、推荐以及因果关系和显著性检测。所有这些功能都有助于加速用户洞察并减少决策偏差

![image-20230926183112526](D:\笔记\笔记图片\image-20230926183112526.png)

![image-20230926183132545](D:\笔记\笔记图片\image-20230926183132545.png)





## Lecture 2 ANN_Intro_0

![image-20231020162239161](D:\笔记\笔记图片\image-20231020162239161.png)

![image-20231020162351253](D:\笔记\笔记图片\image-20231020162351253.png)

### 2.1 Topic 1 Historical/Biological Introduction

How does a biological neuron propagate information?
生物神经元是如何传播信息的?

![image-20231020162720657](D:\笔记\笔记图片\image-20231020162720657.png)



![image-20231020163027751](D:\笔记\笔记图片\image-20231020163027751.png)

* are remarkable among the cells of the body in their ability to propagate signals rapidly over large distances. 
* 在身体的细胞中，它们在远距离快速传播信号的能力是显著的吗
* propagate information by generating characteristic **electrical pulses** called **action potentials** or **spikes** that can travel down nerve fibers.
* 通过产生称为**动作电位或脉冲**的**特征电脉冲**来传播信息，这些脉冲可以沿着神经纤维传播。
*  are highly specialized for generating electrical signals in response to chemical and other inputs and transmitting them to other cells. []
* 对化学物质和其他输入产生电信号并将其传递给其他细胞是高度专业化的。
* represent and transmit information by firing sequence of spikes in various temporal patterns.
* 通过在不同的时间模式下发射脉冲序列来表示和传输信息。

![image-20231020163605405](D:\笔记\笔记图片\image-20231020163605405.png)

### 2.2 Biological Excitability

* Virtually all living cells maintain an **electrical potential** difference between their interiors and the environment (exteriors). 
* 几乎所有的活细胞在其内部和外部环境之间都保持着电位差。
* The **membrane potential** is one of the factors determining the energy barriers encountered by charged substances (ions) entering or leaving the cell.
* 膜电位是决定进入或离开细胞的带电物质(离子)所遇到的能量障碍的因素之一。

![image-20231020163956329](D:\笔记\笔记图片\image-20231020163956329.png)

* Within the cell membrane there are ion channels – proteins with the **central pore** through which ions can cross the membrane. 
* 在细胞膜内有离子通道——有中心孔的蛋白质，离子可以通过它穿过细胞膜。

* **A cell membrane acts as a barrier for ions.**
* **细胞膜是离子的屏障。**

![image-20231020164510746](D:\笔记\笔记图片\image-20231020164510746.png)

* Figure. A schematic diagram of **a section of the lipid bilayer** that forms the cell membrane with two ion channels embedded in it. The membrane is 3 to 4 nm thick, and the ion channels are about 10 nm long
* 数字形成细胞膜的**脂质双分子层**的示意图，其中嵌入了两个离子通道。膜厚3 ~ 4nm，离子通道长约10nm

![image-20231020164955761](D:\笔记\笔记图片\image-20231020164955761.png)

* A wide variety of membrane-spanning ion channels allow ions, predominantly sodium (Na+), potassium (K+), calcium (Ca2+), and chloride (Cl-), to move in and out of the cell.
* 各种各样的跨膜离子通道允许离子，主要是钠离子(Na+)、钾离子(K+)、钙离子(Ca2+)和氯离子(Cl-)进出细胞。
*  Ion channels control the flow of ions across the cell membrane by opening and closing in response to voltage changes and to both internal and external signals.
* 离子通道通过响应电压变化和内部和外部信号打开和关闭来控制离子在细胞膜上的流动。

![image-20231020165252770](D:\笔记\笔记图片\image-20231020165252770.png)

* Under **resting conditions (normal, inactive, not sending a signal)**, the potential inside neuron membrane is from -30 mV to -90 mV relative to that of the surrounding bath, conventionally defined to be 0 mV, and the cell is said to be **polarized.** 
* 在静息条件下(正常、不活动、不发送信号)，神经元膜内的电位相对于周围的电位在-30 mV到-90 mV之间，通常定义为0 mV，细胞被称为极化。
* The **electrical signal** of a living cell is change of the **membrane potential**.
* 活细胞的电信号是细胞膜电位的变化。

![image-20231020170759496](D:\笔记\笔记图片\image-20231020170759496.png)

*  The membrane potential may change in response to electrical perturbation from other neurons. 
* 膜电位可能因其他神经元的电扰动而改变。
* If the perturbation is sufficiently large, **above a threshold** in **intensity and duration**, the response is a large amplitude electrical wave, propagating from the stimulated points to the rest of the tissue.
* 如果扰动足够大，在强度和持续时间上超过阈值，则响应是一个大振幅的电波，从受刺激的点传播到组织的其余部分。

![image-20231020171631161](D:\笔记\笔记图片\image-20231020171631161.png)

* The wave travels with a nearly uniform velocity. 
* 波几乎以匀速传播。
* The excitation and transmission are all-or-none and do not allow varying degree of strength. 
* 兴奋和传输是全或无，不允许有不同程度的强度。
* **Excitation** is followed by an **unexcitable period** of definite duration, called the **absolute refractory period**; which is followed in turn by a **relative refractory period** when the cell has subnormal excitability.
* **兴奋期**之后是一段一定时间的**不可兴奋期**，称为**绝对不应期**;接着是一个**相对不应期**，此时细胞的兴奋性低于正常水平。

### 2.4 Neuron Components

* Important morphological specializations of neurons are **the dendrites** that receive inputs from other neurons, **soma (the cell body)**, and the **axon** that carries the neuronal output to other cells. 
* 神经元的重要形态特化是接受来自其他神经元的输入的树突、体细胞(细胞体)和将神经元输出传递给其他细胞的轴突。
* The elaborate branching structure of **the dendritic tree** allows a neuron to receive inputs from many other neurons through **synaptic connections**.
* 树突树复杂的分支结构允许一个神经元通过突触连接接收来自许多其他神经元的输入。

![image-20231020172907724](D:\笔记\笔记图片\image-20231020172907724.png)

*  The **dendrites** and **soma** act as input surface for signals from other neurons and/or receptors. 
* 树突和胞体作为其他神经元和/或受体信号的输入表面。
* The **axon** carries signals from the neuron to other neurons and/or effectors (e.g., muscle fibers or glands).
* 轴突将信号从神经元传递到其他神经元和/或效应器(如肌纤维或腺体)

![image-20231020173728946](D:\笔记\笔记图片\image-20231020173728946.png)

*  (A): cortical pyramidal cell. These are the primary excitatory neurons of the cerebral cortex. Pyramidal cell axons branch locally, sending signals to synapse with nearby neurons, and also more distally to other parts of the brain and nervous system. 
* 皮质锥体细胞。这些是大脑皮层的初级兴奋性神经元。锥体细胞轴突在局部分支，向附近神经元的突触发送信号，也向更远的大脑和神经系统的其他部分发送信号。
* (B): Purkinje cell. Purkinje cell axons transmit the output of the cerebral cortex. 
* 浦肯野细胞。浦肯野细胞轴突传递大脑皮层的输出。
* (C): stellate cell. Stellate cells are one of a large class of interneurons that provide inhibitory input to the neurons of the cerebral cortex. 
* 星状细胞。星状细胞是向大脑皮层神经元提供抑制性输入的一大类中间神经元。

![image-20231020173958574](D:\笔记\笔记图片\image-20231020173958574.png)

* The cortical pyramidal neuron A and the cortical interneuron C each receive thousands of synaptic inputs, and for the Purkinje cell B, the number is over 100,000. 
* 皮层锥体神经元A和皮层中间神经元C各自接收数千个突触输入，而浦肯野细胞B的突触输入数量超过100,000个。
* Axons from single neurons can traverse large fractions of the brain or, in some cases, of the entire body. 
* 来自单个神经元的轴突可以穿越大脑的大部分，或者在某些情况下，穿越整个身体。
* Axons can also connect with multiple targets.
* 来自单个神经元的轴突可以穿越大脑的大部分，或者在某些情况下，穿越整个身体。

 ![image-20231020174220019](D:\笔记\笔记图片\image-20231020174220019.png)

### 2.5 Trans-synaptic stimulation – External Mechanism

* The tips of the axon branches are called nerve terminals or **boutons**. 
* 轴突分支的尖端称为**神经末梢**或钮扣。
* The location of interaction between a terminal and the cell upon is called a **synapse**. 
* 终端和细胞之间相互作用的位置称为**突触**。
* A synapse shown in the left figure illustrates the presynaptic bouton at the end of the axon and a spine on the dendrite.
* 左图所示的突触显示了轴突末端的突触前按钮和树突上的棘。

![image-20231020174742967](D:\笔记\笔记图片\image-20231020174742967.png)

* The terminology of **presynaptic前突触** and **postsynaptic后突触** defines the direction of signal flow. 
* 突触前和突触后的术语定义了信号流的方向。
* Santiago Ramon y Cajal, ~1901, supposed that the specific networking of the nervous cells determines direction of transmission of information. **This discovery made clear that the coupling of the neurons constitutes a <font color=red>hierarchical system</font>.**
* 圣地亚哥·拉蒙·卡哈尔(Santiago Ramon y Cajal, 1901)认为，神经细胞的特定网络决定了信息传递的方向。这一发现清楚地表明，**神经元的耦合构成了一个分层系统。**

![image-20231021232232830](D:\笔记\笔记图片\image-20231021232232830.png)

* The **chemical transmission** of information at the synapses was mostly studied from 1920 to 1940. 
* 从1920年到1940年，人们主要研究突触中信息的化学传递。
* The two neurons are not directly connected but communicate **via the cleft经由间隙进行交流**.
* 这两个神经元不是直接相连的，而是通过间隙进行交流。

![image-20231021232459995](D:\笔记\笔记图片\image-20231021232459995.png)

* The **axon terminal轴突末端 or bouton** is filled with **synaptic vesicles神经递质** containing **neurotransmitter神经递质**.
* 轴突末端或钮扣充满了含有神经递质的突触囊泡。 
* The **neurotransmitter神经递质** is released when a **spike脉冲** arrives from the **presynaptic neuron突出前神经元**.
* 当突触前神经元发出脉冲时，神经递质就会释放出来。

![image-20231021232949459](D:\笔记\笔记图片\image-20231021232949459.png)

* **Transmitter crosses the synaptic cleft and binds to receptors on the dendritic spine树突.** 
* **递质穿过突触间隙，与树突上的受体结合。**
* **Excitatory synapses兴奋性突触** on cortical pyramidal cells form on dendritic spines as shown here. **Synapses** can form on the **dendrites树突, or axon轴突**.
* 皮层锥体细胞上的兴奋性突触在树突棘上形成。**突触**可以在树突或轴突上形成。

![image-20231021233706389](D:\笔记\笔记图片\image-20231021233706389.png)

* Although impulses spread **uniformly均匀的** along axons, **there is no physiological continuity from neuron to neuron.** 
* 虽然脉冲沿轴突均匀传播，**但在神经元之间没有生理连续性。**
* 解释一下生理连续性：意味着不同神经元之间没有直接的物理或细胞结构上的连续性。这是因为神经元之间的连接是通过化学和电信号传递的，而不是通过细胞体或轴突的物理延伸来实现的。
* When an impulse (perturbation) reaches a synapse, it does not necessarily stimulate the following neuron.
* 当一个脉冲(扰动)到达一个突触时，它不一定会刺激下一个神经元。

![image-20231021234647429](D:\笔记\笔记图片\image-20231021234647429.png)

* Trans-synaptic stimulation of a neuron requires usually 
* 神经元的突触间刺激通常需要
  * either a **repetition of impulses** in time at the same **synapse** (temporal summation). 
  * 在同一突触上脉冲的及时重复(时间叠加)。
  * or the **simultaneous同时** arrival of impulses at a sufficient number of **adjacent synapses相邻的突出** (spatial summation)
  * 或者脉冲同时到达足够数量的相邻突触(空间求和)
* to make the “density” of excitation high enough at some region of the neuron.
* 使神经元某些区域的兴奋“密度”足够高。

![image-20231021235251555](D:\笔记\笔记图片\image-20231021235251555.png)

* The arrival of impulses at **synapses** may have **opposite to excitation effect**, i.e., it may render the element less excitable to other stimuli. This decrease of excitability is called **inhibition**.
* **脉冲到达突触可能具有与兴奋效应相反的作用**，即它可能使该元件对其他刺激的兴奋性降低。这种兴奋性的降低被称为**抑制**。

### 2.6 Neuronal Excitation

![image-20231022005158538](D:\笔记\笔记图片\image-20231022005158538.png)

* The **excitatory or inhibitory兴奋或抑制作用** effect of the transmitter generally causes a potential change in the **postsynaptic membrane突触后膜**. 
* **递质的兴奋或抑制作用通常会引起突触后膜的电位变化**。
* The cooperative effect of many potential changes may **yield a synthesized potential change** in the soma that exceeds the threshold – and if this occurs at a time when the neuron has passed the **refractory period肌肉或神经做出反应后，恢复再次做出反应能力之前的短暂时间** of its previous firing, then a new impulse is fired down the axon.
* 许多电位变化的协同作用可能会在胞体中**产生超过阈值的综合电位变化**——如果这种变化发生在神经元已经过了前一次放电的不应期时，那么轴突就会产生新的脉冲。

![image-20231022005819146](D:\笔记\笔记图片\image-20231022005819146.png)

* The top trace represents a recording from an intracellular electrode connected to the soma of the neuron. The height of the action potentials has been clipped to show the subthreshold membrane potential more clearly. 
* 顶部的轨迹代表连接到神经元体的细胞内电极的记录。动作电位的高度已被剪切，以更清楚地显示阈下膜电位。
* The middle trace is a simulated extracellular recording. Action potentials appear as roughly equal positive and negative potential fluctuations with an amplitude of ~0.1mV, which is ~1000 times smaller than the approximately 0.1V amplitude of an intracellularly recorded action potential. 
* 中间的痕迹是模拟的细胞外录音。动作电位表现为大致相等的正负电位波动，振幅约为0.1mV，比细胞内记录的动作电位约0.1V振幅小约1000倍。
* The bottom trace represents a recording from an intracellular electrode connected to the axon some distance away from the soma. The full height of the action potentials is indicated in this trace.
* 底部的痕迹代表了细胞内电极的记录，该电极连接到离体细胞一定距离的轴突上。动作电位的全部高度在这张图中显示出来。

![image-20231022010021498](D:\笔记\笔记图片\image-20231022010021498.png)

* The top recording from **soma（神经元细胞体）** shows rapid spikes riding on top of a more slowly varying subthreshold potential. 
* 顶部来自躯体的记录显示快速的尖峰位于变化较慢的阈下电位之上。
* The bottom trace shows **intracellular细胞内的** recording from axon some distance out of soma. The subthreshold membrane potential waveform, apparent in the soma recording, is completely absent on the axon due to attenuation, while the action potential sequence in the two recordings is the same. 
* 底部的痕迹显示了从离体细胞一定距离的轴突传来的细胞内记录。阈下膜电位波形在胞体记录中很明显，但在轴突上由于衰减而完全不存在，而两种记录中的动作电位序列是相同的。
* The difference in records from soma and from the axon illustrates the important point that
* 体细胞和轴突记录的差异说明了重要的一点



![image-20231022010429970](D:\笔记\笔记图片\image-20231022010429970.png)

## Lecture 3 ANN_Intro_1

### 3.1 Abstract Model for a Neuron

* **A basic abstract model for a biological neuron.**
* **生物神经元的基本抽象模型。**

![image-20231022010623594](D:\笔记\笔记图片\image-20231022010623594.png)



* **Weights of Connections 连接的权重**

  * Neuron gets fired if it has received from the **presynaptic neurons** a summary impulse, which is above a **certain threshold某一特定阈值**. 
  * 如果一个神经元从突触前神经元接收到超过一定阈值的汇总脉冲，它就会被激活。

  * Signal from a single synapse may sometime overcome the threshold and push a neuron to fire an action potential, but other synapses can achieve this only by simultaneously delivering their signals: Some inputs are more important! 
  * 来自单个突触的信号有时可能会超过阈值，推动神经元激发动作电位，但其他突触只有同时传递信号才能实现这一目标:有些输入更重要!
    * "Signal from a single synapse may sometime overcome the threshold and push a neuron to fire an action potential" - 这部分意味着一个单独的突触（神经元连接的一个小结构，用于传递信号）的信号有时候足够强，可以使神经元兴奋到足以产生一个动作电位（action potential）。这是因为神经元具有一个电压阈值，当电位超过这个阈值时，神经元会触发动作电位，这是信息传递的一种方式。
    * "but other synapses can achieve this only by simultaneously delivering their signals" - 这部分意味着其他突触只有在同时传递它们的信号时，才能够共同达到足够的强度来使神经元产生动作电位。这表示某些突触的信号可能比其他的更强，因此需要多个较弱的信号同时作用于神经元，以产生足够的刺激来触发动作电位
    * "Some inputs are more important!" - 这句话的结尾强调了一种观点，即某些输入信号对于激活神经元的动作电位来说更为重要。这意味着不同的输入可能具有不同的重要性，某些输入可能需要更多的协同作用才能影响神经元的活动。这是神经系统中的一种重要机制，用于调节信息处理和神经元的兴奋性。
    * **在某些情况下，一个单独的突触的信号足够强烈，可以使神经元产生一个动作电位，但在其他情况下，可能需要多个突触同时共同作用，才能使神经元产生动作电位。**这反映了神经系统中的多样性，不同的突触可以对神经元的兴奋性产生不同程度的影响，有些突触更为强烈，而有些可能需要协同作用才能触发动作电位。**因此，不同的输入信号可能具有不同的重要性，有些输入更容易引发神经元的活动**

  * Therefore, input from every synapse, or “connection”, to the neuron in the abstract model must be assigned with some value w, called connection strength or weight of connection, to describe the importance of a connection.
  * 在某些情况下，一个单独的突触的信号足够强烈，可以使神经元产生一个动作电位，但在其他情况下，可能需要多个突触同时共同作用，才能使神经元产生动作电位。这反映了神经系统中的多样性，不同的突触可以对神经元的兴奋性产生不同程度的影响，有些突触更为强烈，而有些可能需要协同作用才能触发动作电位。因此，不同的输入信号可能具有不同的重要性，有些输入更容易引发神经元的活动

![image-20231022013604838](D:\笔记\笔记图片\image-20231022013604838.png)

* Shown is an abstract neuron j with n+1 inputs. 
* 图中是一个抽象的神经元j，有n+1个输入
* Each input i transmits a real value ai. 
* 每个输入i传送一个实值ai。
* Each connection is assigned with the weight wji.
* 每个连接都分配了权重wji。



* **The total input S**, i.e. the sum of the products of the inputs with the corresponding weights, **<font color=red>is compared with the threshold</font>** (equal to 0 in this case), and the outcome **Xj is produced consequently**.
* **总输入S，即输入与相应权重的乘积之和，与阈值(在这种情况下等于0)进行比较，从而产生结果Xj。**

![image-20231022014153108](D:\笔记\笔记图片\image-20231022014153108.png)

![image-20231022220844568](D:\笔记\笔记图片\image-20231022220844568.png)

![image-20231022220917051](D:\笔记\笔记图片\image-20231022220917051.png)

![image-20231022220944102](D:\笔记\笔记图片\image-20231022220944102.png)

![image-20231022221236765](D:\笔记\笔记图片\image-20231022221236765.png)

![image-20231022221402761](D:\笔记\笔记图片\image-20231022221402761.png)

![image-20231022221959159](D:\笔记\笔记图片\image-20231022221959159.png)

![image-20231022221951195](D:\笔记\笔记图片\image-20231022221951195.png)

* 



### 3.2 Final Caution

* **Massive and hierarchical networking of the brain** seems to be the fundamental precondition for the emergence of consciousness and complex behaviour. 
* **大脑的大规模和分层网络**似乎是意识和复杂行为出现的基本先决条件
* So far, however, biologists and neurologists have concentrated their research on uncovering the properties of **individual neurons.**
* 然而，到目前为止，生物学家和神经学家的研究主要集中在揭示单个神经元的特性上。



* Today, the mechanisms for the production and transport of signals from one neuron to another are well understood physiological phenomena, but 
* 今天，信号从一个神经元到另一个神经元的产生和传输机制是很好的生理现象，但是
  * **how these individual systems cooperate** 
  * **这些独立的系统是如何合作的**
* to form complex and massively **parallel system** capable of incredible information processing feats still constitutes 
* 形成复杂的大规模**并行系统**，具有难以置信的信息处理能力
  * the biggest mystery of the brain. 
  * 大脑最大的谜团。

![image-20231022223120315](D:\笔记\笔记图片\image-20231022223120315.png)

*  Mathematics, biophysics and computer science can provide invaluable help in the complex interdisciplinary study of the brain. 
* 数学、生物物理学和计算机科学可以为复杂的跨学科大脑研究提供宝贵的帮助。
* However, we should 
  * **be careful with metaphors and paradigms** 
  * **小心使用隐喻和范例**
* commonly introduced when dealing with the nervous system.
* 通常在处理神经系统时介绍。

![image-20231022223253351](D:\笔记\笔记图片\image-20231022223253351.png)

* It seems to be a constant in the history of science to compare the brain to the most complicated contemporary device produced by human industry. 
* 在科学史上，把大脑比作人类工业生产的最复杂的现代设备似乎是一个不变的现象。
  * In ancient times, the brain was compared to a pneumatic machine, 
  * 在古代，大脑被比作一台气动机器，
  * in the Renaissance to clockwork, 
  * 文艺复兴时期的发条装置
  * at the end of the nineteenth century to the telephone network. 
  * 十九世纪末，电话网络出现了。
* Today, it is popular to consider computers **the paradigm par excellence 卓越的范例** of a nervous system. 
* 今天，人们普遍认为计算机是神经系统的典范。



![image-20231022223323141](D:\笔记\笔记图片\image-20231022223323141.png)



* It is rather paradoxical that when **John von Neumann** wrote his classical description of future universal computers, he tried to choose terms that would
* 这是相当矛盾的，当约翰·冯·诺伊曼写下他对未来通用计算机的经典描述时，他试图选择一些术语
  * describe computers in terms of brains, not brains in terms of computers.
  * 用大脑来描述计算机，而不是用计算机来描述大脑。



![image-20231022224144943](D:\笔记\笔记图片\image-20231022224144943.png)



![image-20231022224220710](D:\笔记\笔记图片\image-20231022224220710.png)

![image-20231022224235422](D:\笔记\笔记图片\image-20231022224235422.png)

![image-20231022224256110](D:\笔记\笔记图片\image-20231022224256110.png)

## Week1 Questions_Answers

* Q: **Describe the biological computation and the relation with biology.**
* 描述生物计算及其与生物学的关系。
  * A: Biological computation includes efforts to determine **how biology does information technology from the sub-cellular level to the systems and population level**, for instance, ecologies, economies and brain. Biology discoveries and research motivates the biological computation (algorithms), while biological computation can help biologist understand clearer biology phenomenon and better explore the mechanism.
  * 生物计算包括努力确定生物学**如何从亚细胞水平到系统和人口水平的信息技术**，例如，生态学，经济学和大脑。生物学的发现和研究激发了生物计算(算法)，而生物计算可以帮助生物学家更清晰地理解生物现象，更好地探索其机制。



* Q: Briefly introduce the neuron signal processing
* A: The answer might be based on a table such as one below

![image-20231022225048793](D:\笔记\笔记图片\image-20231022225048793.png)

![image-20231022225150007](D:\笔记\笔记图片\image-20231022225150007.png)



* Q: Briefly describe the relation between a biological neuron and the abstract model shown below.
* 简要描述一下生物神经元与下面所示的抽象模型之间的关系。

![image-20231022225346698](D:\笔记\笔记图片\image-20231022225346698.png)

## Lecture 4 McCulloch_Pitts_0

### 4.1 McCulloch_Pitts

* McCulloch and Pitts demonstrated that
  * “...because of the **all-or-none** character of nervous activity, neural events and the relations among them can be treated by means of the propositional logic”. 
  * “…由于神经活动的非有即无的特点，神经事件及其相互关系可以用**<font color=red size=5>“命题逻辑”</font>**来处理。
  * 解释一下**全有或者全无 all or none**: 这指的是神经元动作电位（动作电位是神经元产生的电信号）的性质。当神经元的兴奋达到某一阈值时，它会触发一个完整的动作电位，而当兴奋不足以达到这个阈值时，就不会触发动作电位。因此，**神经元的反应要么完全发生，要么完全不发生，没有中间状态**。这一特性被称为“全有或全无”。

![image-20231022230005603](D:\笔记\笔记图片\image-20231022230005603.png)

* The authors modelled the neuron as 
* 作者将神经建模为
  * **a binary, discrete-time input** 
  * 一个二进制的离散的时间输入
  * **with excitatory and inhibitory connections and an excitation threshold.** 
  * 有兴奋性和抑制性联系和兴奋阈值。
    * The network of such elements was **the first model** to tie the study of neural networks to **<font color=red>the idea of computation in its modern sense</font>.** 
    * 这些元素组成的网络是第一个将神经网络研究与现代意义上的计算思想联系起来的模型。
* Other models (structures): Fully-connected neural networks, Convolutional neural networks, Residual neural network…
* 这些元素组成的网络是第一个将神经网络研究与现代意义上的计算思想联系起来的模型。

![image-20231022233743590](D:\笔记\笔记图片\image-20231022233743590.png)



* The basic idea was to divide time into units, i.e., steps, and **in each time period at most one spike can be initiated in the axon** of a given neuron.
* 基本思想是将时间分成单位，即步骤，在每个时间段内，在给定神经元的轴突中最多可以启动一个脉冲。

![image-20231022233610756](D:\笔记\笔记图片\image-20231022233610756.png)

*  **<font color=red>Discretization离散化</font>**: Comparable to a refractory period (assumed to be the same for each neuron). No Zeno executions! 
* 类似于不应期(假设每个神经元都是相同的)。没有出现无限快速的冲动
* **<font color=blue>因为神经细胞存在有不应期，所以这里的时间不是一个连续的直线，而是存在多段的离散线段</font>**
* **<font color=red>Fixed time stepsize固定时间步长</font>**: The impulse travels with a nearly uniform velocity in a biological neural system.
* 固定时间步长：脉冲在生物神经系统中以几乎均匀的速度传播。

![image-20231022235002543](D:\笔记\笔记图片\image-20231022235002543.png)

![image-20231022235713161](D:\笔记\笔记图片\image-20231022235713161.png)

![image-20231023000138347](D:\笔记\笔记图片\image-20231023000138347.png)



* 任何时刻来自前突触的值只有可能是0或者1

![image-20231023002724357](D:\笔记\笔记图片\image-20231023002724357.png)

* Comparable to the fact that only spikes are propagated in biological neural networks; 
* 与在生物神经网络中只传播尖峰信号的事实相比;

* The types of the input and the output of a MP neuron are thus unified.
* 因此，MP神经元的输入和输出类型是统一的。

![image-20231023010126632](D:\笔记\笔记图片\image-20231023010126632.png)

![image-20231023010147810](D:\笔记\笔记图片\image-20231023010147810.png)

![image-20231023010218926](D:\笔记\笔记图片\image-20231023010218926.png)

![image-20231023010226633](D:\笔记\笔记图片\image-20231023010226633.png)



*  There is an **excitation threshold θ** associated with the neuron. 
* 神经元有一个**激发阈值θ**。
* Similar to the basic abstract neuron, θ is comparable to the potential threshold in a biological neuron.
* 类似于基本的抽象神经元, θ相当于生物神经元的电位阈值。

![image-20231023010629497](D:\笔记\笔记图片\image-20231023010629497.png)

* Output Xt of the neuron at the following instant t is defined according to the rule:
* 神经元在下一时刻t的输出Xt根据以下规则定义:

![image-20231023010814633](D:\笔记\笔记图片\image-20231023010814633.png)

![image-20231023011500656](D:\笔记\笔记图片\image-20231023011500656.png)

* **<font color=red size=5>i.e., the input via a connection with negative weight -1, prevents excitation of the neuron at that instant</font>**
* **也就是说，通过负权-1连接的输入会阻止神经元在那一刻的兴奋**

* <font size=5>关于这个我不是特别了解，感觉有可能是因为wi和at都为负值结果却为正不太合适，大概吧？？？？？？？？？？？？</font>

![image-20231023011827300](D:\笔记\笔记图片\image-20231023011827300.png)

* St-1: instant state of the neuron神经元的即时状态

![image-20231023012209529](D:\笔记\笔记图片\image-20231023012209529.png)

* St-1的状态并不取决于之前的状态，只是简单的要求满足下面的公式。



### 4.2 Activation Function

* The neuron output Xt is a function of its state St-1, therefore the output can be also written as a discrete-time function
* 神经元的输出Xt是其状态St-1的函数，因此输出也可以写成离散时间函数
* 神经元的输出 Xt 是其前一时刻的状态 St-1 的函数，因此输出也可以被表示为一个离散时间的函数

![image-20231023013233286](D:\笔记\笔记图片\image-20231023013233286.png)



![image-20231023013302551](D:\笔记\笔记图片\image-20231023013302551.png)

* Here H is the Hesviside (unit step) function（阶越函数）:

![image-20231023013435409](D:\笔记\笔记图片\image-20231023013435409.png)



 ### 4.3 Summary

![image-20231023013502049](D:\笔记\笔记图片\image-20231023013502049.png)

### 4.4 MP-Neuron as a Binary Unit

* **Simple logical functions** can be implemented directly with **a single McCulloch-Pitts unit**.
* **简单的逻辑功能**可以用**单个麦卡洛克-皮茨**单元直接实现。
* The output value 1 can be associated with the logical value true and 0 with the logical value false. 
* 输出值1可以与逻辑值true关联，输出值0可以与逻辑值false关联。
* In the next lecture, I will demonstrate how weights and thresholds can be set to yield neurons which realise the logical functions AND, OR and NOT.
* 在下一讲中，我将演示如何设置权重和阈值来产生实现逻辑函数and, OR和NOT的神经元。

![image-20231023034816340](D:\笔记\笔记图片\image-20231023034816340.png)



## Lecture 5 McCulloch_Pitts_1

* The authors modelled the neuron as
* a binary, discrete-time input
* with excitatory and inhibitory connections and an excitation threshold.

![image-20231023035042977](D:\笔记\笔记图片\image-20231023035042977.png)



### 5.1 MP Neuron Computation Algorithm

* Given a fixed MP neuron, that is, all weights of connections and neuron threshold are set up in advance.
* 给定一个固定的MP神经元，即预先设置好所有连接权值和神经元阈值。

![image-20231023035153715](D:\笔记\笔记图片\image-20231023035153715.png)

![image-20231023035316088](D:\笔记\笔记图片\image-20231023035316088.png)

#### 5.1.1 Example

![image-20231023035630193](D:\笔记\笔记图片\image-20231023035630193.png)

![image-20231023035639834](D:\笔记\笔记图片\image-20231023035639834.png)

* **<font color=red size=5>记住一件事，所有的输入必须都大于等于0才可以进行下一步，否则就是X=0</font>**



### 5.2 使用MP model实现 And，Or，Not

#### 5.2.1 And

![image-20231023040029760](D:\笔记\笔记图片\image-20231023040029760.png)

![image-20231023040054157](D:\笔记\笔记图片\image-20231023040054157.png)



#### 5.2.2 Or

![image-20231023040143532](D:\笔记\笔记图片\image-20231023040143532.png)

#### 5.2.3 Not

![image-20231023040204325](D:\笔记\笔记图片\image-20231023040204325.png)

### 5.3 MP-Neuron Logic: Multiple Inputs

![image-20231023040602217](D:\笔记\笔记图片\image-20231023040602217.png)

![image-20231023040653377](D:\笔记\笔记图片\image-20231023040653377.png)

* The **<font color=red>threshold logic elements门限逻辑元件</font>** reduce the complexity of the circuit used to implement a given logical function.
* 阈值逻辑元件降低了用于实现给定逻辑功能的电路的复杂性。
  * 门限逻辑元件通过降低电路的复杂性，使得实现特定逻辑函数的过程更加高效。它们通过更灵活地处理输入信号，能够减少需要的电子元件数量，从而降低了电路的复杂度。这对于设计和构建逻辑电路以执行复杂逻辑功能非常有帮助。

### 5.4 MP-Neuron as a Register Cell寄存器单元

![image-20231023042050413](D:\笔记\笔记图片\image-20231023042050413.png)

* A single neuron with a single input a and with the weight and threshold values both of unity, computes the output
* 单个神经元具有单个输入A，并且权重和阈值都是统一的，计算输出Xt = at-1
* Such a single neuron thus behaves as a single register cell **<font color=red>able to retain the input for one period  elapsing between two instant</font>**
* 这样的单个神经元就像一个寄存器单元，**能够在两个瞬间之间的一个周期内保留输入**

### 5.5 （Extended） MP-Neuron as a Memory Cell

![image-20231023043034862](D:\笔记\笔记图片\image-20231023043034862.png)

* With a feedback loop closed around the neuron, as it is shown above, we obtain a memory cell. Note that it is not a single MP-neuron with the classical definition.
* 如上所示，在神经元周围闭合一个反馈回路，我们就得到了一个记忆细胞。注意，它不是一个具有经典定义的单个mp -神经元。

![image-20231023043708890](D:\笔记\笔记图片\image-20231023043708890.png)

* In the absence of inputs, the output value is sustained indefinitely. This is because of the output of 0 feeds back to the input does not cause firing at the next instant, while the output of 1 does.
* 在没有投入的情况下，产出值是无限持续的。这是因为0的输出反馈到输入不会在下一个瞬间触发，而1的输出会。

![image-20231023044047120](D:\笔记\笔记图片\image-20231023044047120.png)

![image-20231023044106389](D:\笔记\笔记图片\image-20231023044106389.png)



## Lecture 6 McCulloch_Pitts_2

![image-20231023044454212](D:\笔记\笔记图片\image-20231023044454212.png)



* Without time 意味着不考虑时间因素



### 6.1 Geometric Interpretation: 2D 'OR' 几何解释

![image-20231024012233783](D:\笔记\笔记图片\image-20231024012233783.png)

* A single MP neuron splits the input space (4 points in the case of 2 inputs) into two halves
* 单个MP神经元将输入空间(2个输入的情况下为4个点)分成两半

![image-20231024013035707](D:\笔记\笔记图片\image-20231024013035707.png)

* 根据**∑ ai -1**这条线将整个图分成两个部分，一个是在这条线上和在线之上的空间，一个是在线之下的位置

![image-20231024013307988](D:\笔记\笔记图片\image-20231024013307988.png)

* In other words, all inputs firing the neuron will be one side of the line, while all inputs inhibiting the neuron lie on the other side.
* 换句话说，所有激发神经元的输入都在线的一边，而所有抑制神经元的输入都在线的另一边。

* Does a MP neuron implement a boundary that linearly separates the input space?

* MP神经元是否实现了线性分离输入空间的边界?

  * **<font color=blue>这个需要解释一下什么是线性分离输入空间的边界</font>**

  * 在机器学习和模式识别领域，线性分隔边界是一种将不同类别或类别之间的数据点分隔开的决策边界。这个决策边界是线性的，意味着它可以表示为输入特征的线性组合。MP神经元是一种二元分类器，它对多个二进制输入进行加权求和，并与阈值进行比较，产生二进制输出。

    MP神经元可以实现线性分隔边界，但只能在非常简单的情况下。它的分隔能力受限于它的阈值和输入权重。如果数据可以被单个MP神经元的阈值和权重设置所正确分离，那么它可以实现线性分隔边界。然而，对于更复杂的数据分布，通常需要更复杂的神经网络结构，如多层感知机（MLP），以实现非线性分隔边界。



### 6.2 Geometric Interpretation: 2D “AND”

![image-20231024014507957](D:\笔记\笔记图片\image-20231024014507957.png)

* 与“OR”类似， 同样有一条线将其分成了两部分。

![image-20231024014653095](D:\笔记\笔记图片\image-20231024014653095.png)

* 很明显，这里还有一个面，如果有三个输入的话。



### 6.3 Representation Power of a single MP Neuron 一个MP神经元的代表能力

* A single MP neuron can be used to represent some Boolean functions which are **linearly separable**. 
* 单个MP神经元可以用来表示一些**线性可分**的布尔函数。
* Linear separability (for Boolean functions): There exists a line (plane) such that all inputs which produce a 1 for the function lie on one side of the line (plane) and all inputs which produce a 0 lie on other side of the line (plane).
* 线性可分性(布尔函数):存在一条线(平面)，使得所有产生1的输入位于线(平面)的一侧，所有产生0的输入位于线(平面)的另一侧。

![image-20231024015134320](D:\笔记\笔记图片\image-20231024015134320.png)

* Try to prove there is no single MP neuron implementation for the linear separable function indicated in the figure. 
* 试图证明图中所示的线性可分函数没有单一的MP神经元实现。

#### 6.3.1 Revisit definition 重新定义一下MP 神经元

![image-20231024020435147](D:\笔记\笔记图片\image-20231024020435147.png)

* Enumerating all the cases, it is easy to obtain that only 0,1 fires the neuron. Does the neuron act as a linear boundary in this case?
* 列举所有的情况,很容易得到,只有0,1触发神经元。在这种情况下,神经元是一个线性边界吗?

![image-20231024021156128](D:\笔记\笔记图片\image-20231024021156128.png)

* After obtaining a boundary, remove the face of a1 = 1 from the positive side
* 得到边界后，从正侧移除a1 = 1的面

![image-20231024021306065](D:\笔记\笔记图片\image-20231024021306065.png)

* Iteratively do the above, until all the inhibitory connections are considered.
* 反复执行上述操作，直到考虑到所有抑制连接。

![image-20231024021431257](D:\笔记\笔记图片\image-20231024021431257.png)



![image-20231024021438093](D:\笔记\笔记图片\image-20231024021438093.png)

* **迭代进行上述操作**

![image-20231024021503162](D:\笔记\笔记图片\image-20231024021503162.png)

* A single MP neuron can be used to represent some Boolean functions which are linearly separable. 
* 单个MP神经元可以用来表示一些线性可分的布尔函数。
* Linear separability (for Boolean functions): There exists a line (plane) such that all inputs which produce a 1 for the function lie on one side of the line (plane) and all inputs which produce a 0 lie on other side of the line (plane). 
* 线性可分性(布尔函数):存在一条线(平面)，使得所有产生1的输入位于线(平面)的一侧，所有产生0的输入位于线(平面)的另一侧。
* Completeness: Can each linear separable function be represented by a single MP neuron? No! 
* 完备性:每个线性可分函数可以用单个MP神经元表示吗?不!
* A single MP neuron describes a specific linear boundary that is only determined by the threshold in the hyper-cube state space, removing the faces corresponding to inhibitory connections. 
* 单个MP神经元描述一个特定的线性边界，该边界仅由超立方体状态空间中的阈值决定，去除与抑制性连接相对应的面。



## Week2 Homework with answer

* Describe the motivation of having a discrete-time, binary inputs for a MP neuron
* 描述MP神经元的离散时间二进制输入的动机

![image-20231024025005350](D:\笔记\笔记图片\image-20231024025005350.png)



![image-20231024025037448](D:\笔记\笔记图片\image-20231024025037448.png)



![image-20231024025058195](D:\笔记\笔记图片\image-20231024025058195.png)

![image-20231024025118963](D:\笔记\笔记图片\image-20231024025118963.png)



![image-20231024025127403](D:\笔记\笔记图片\image-20231024025127403.png)



## Lecture7 McCulloch_Pitts_3

![image-20231024025701201](D:\笔记\笔记图片\image-20231024025701201.png)

* It deals with propositions (which can be true or false) and relations between propositions, including the construction of arguments based on them. Compound propositions are formed by connecting propositions by logical connectives. Propositions that contain no logical connectives are called atomic propositions. Unlike first-order logic, propositional logic does NOT deal with non-logical objects, predicates about them, or quantifiers.
* 它处理命题(可以是真或假)和命题之间的关系，包括基于它们构建的论证。复合命题是通过逻辑连接词将命题连接起来形成的。不包含逻辑连接词的命题称为原子命题。与一阶逻辑不同，命题逻辑不处理非逻辑对象、关于它们的谓词或量词。

![image-20231024025824223](D:\笔记\笔记图片\image-20231024025824223.png)

* Although the McCulloch-Pitts neuron model was very simplistic, it can perform **the basic logic operations AND, OR and NOT** 
* 虽然McCulloch-Pitts神经元模型非常简单，但它可以执行基本的逻辑运算AND, OR和NOT
* An MP neural network can implement any **multivariable propositional logic function**, with the thresholds and weights being appropriately selected. 
* MP神经网络可以实现任何多变量命题逻辑函数,具有适当选择的阈值和权重。



### 7.1 MP神经网络实现多变量逻辑函数

* Example

![image-20231024030238541](D:\笔记\笔记图片\image-20231024030238541.png)

![image-20231024030315147](D:\笔记\笔记图片\image-20231024030315147.png)

![image-20231024030204210](D:\笔记\笔记图片\image-20231024030204210.png)



![image-20231024031034424](D:\笔记\笔记图片\image-20231024031034424.png)

![image-20231024031026408](D:\笔记\笔记图片\image-20231024031026408.png)

* Furthermore, the discrete time, or unity delay property of the model makes it even possible to build a sequential digital circuitry.
* 此外,离散时间,或者模型的统一延迟属性,甚至可能建立一个连续的数字电路。

![image-20231024032346829](D:\笔记\笔记图片\image-20231024032346829.png)

### 7.2 MP Neuron Conclusion

* The McCulloch and Pitts 1943 paper had a huge influence on the thoughts and studies that led to modern digital computer design. 
* 麦卡洛克和皮茨1943年的论文对导致现代数字计算机设计的思想和研究产生了巨大影响。
* MP-neuron outlined the first formal model of an elementary computing unit.
* MP-neuron概述了基本计算单元的第一个正式模型。

![image-20231024032536955](D:\笔记\笔记图片\image-20231024032536955.png)

* The McCulloch and Pitts neuron model included all necessary elements to perform logic operations, and thus
* 麦卡洛克和皮茨的神经元模型包含了执行逻辑运算的所有必要元素，因此
* MP-neuron could function as an arithmetic-logic computing element to compute any computable function.
* mp -神经元可以作为一个算术逻辑计算单元来计算任何可计算的函数。

![image-20231024032736057](D:\笔记\笔记图片\image-20231024032736057.png)

* The McCulloch-Pitts neuron was a very significant result and with it, it is generally agreed that the disciplines of neural networks and artificial intelligence were born.
* 麦卡洛克-皮茨神经元是一个非常重要的成果，有了它，人们普遍认为神经网络和人工智能学科诞生了。

![image-20231024032844007](D:\笔记\笔记图片\image-20231024032844007.png)

* Though the threshold elements are, from the combinatorial point of view, more versatile than conventional logic gates, there was a problem with assumed unlimited fan-in (number of inputs of a logic gate): 
* 虽然从组合的角度来看，阈值元素比传统逻辑门更通用，但假设无限扇入(逻辑门的输入数量)存在一个问题:
* the implementation of the compact electronic model was not feasible in the days of bulky vacuum tubes. 
* 虽然从组合的角度来看，阈值元素比传统逻辑门更通用，但假设无限扇入(逻辑门的输入数量)存在一个问题:

![image-20231024033015069](D:\笔记\笔记图片\image-20231024033015069.png)

* The formal neuron model was not widely adopted for the vacuum tube hardware description, and the model never became technically significant. 
* 正式的神经元模型并没有被广泛应用于真空管的硬件描述，该模型在技术上也没有多大意义。



![image-20231024033006771](D:\笔记\笔记图片\image-20231024033006771.png)

* Now-days a possible way of overcoming the hardware difficulties could be the use of 
  * optical computing elements 
  * 光学计算元件
* capable of providing unlimited fan-in by changing the angle of lens. 
* But still not quite clear yet…

![image-20231024033222475](D:\笔记\笔记图片\image-20231024033222475.png)



## Lecture8 Hebbs_Rules_0

![image-20231025010447040](D:\笔记\笔记图片\image-20231025010447040.png)

* A single MP neuron can be used to represent some Boolean functions which are linearly separable.
* 单个MP神经元可以用来表示一些线性可分的布尔函数。
* Linear separability (for Boolean functions): There exists a line (plane) such that all inputs which produce a 1 for the function lie on one side of the line (plane) and all inputs which produce a 0 lie on other side of the line (plane).
* 线性可分性(布尔函数):存在一条线(平面)，使得所有产生1的输入位于线(平面)的一侧，所有产生0的输入位于线(平面)的另一侧。
* Completeness: Can each linear separable function be represented by a single MP neuron? No!
* 完备性:每个线性可分函数可以用单个MP神经元表示吗?不!
* A single MP neuron describes a specific linear boundary that is only determined by the threshold in the hyper-cube state space, removing the faces corresponding to inhibitory connections.
* 单个MP神经元描述一个特定的线性边界，该边界仅由超立方体状态空间中的阈值决定，去除与抑制性连接相对应的面



![image-20231025010309687](D:\笔记\笔记图片\image-20231025010309687.png)

*  Although the McCulloch-Pitts neuron model was very simplistic, it can perform the basic logic operations AND, OR and NOT 
* 虽然McCulloch-Pitts神经元模型非常简单，但它可以执行基本的逻辑运算AND, OR和NOT
* An MP neural network can implement any multivariate propositional logic function, with the thresholds and weights being appropriately selected. 
* 通过适当选择阈值和权值，MP神经网络可以实现任意多元命题逻辑函数。
* Furthermore, the discrete time, or unity delay property of the model makes it even possible to build a sequential digital circuitry.
* 此外，该模型的离散时间或单位延迟特性甚至使构建顺序数字电路成为可能。

![image-20231025012738190](D:\笔记\笔记图片\image-20231025012738190.png)

* The main “ideological” problems of the McCulloch- Pitts model were that. 
* 麦卡洛克-皮茨模型的主要“意识形态”问题是。
  * The network must be completely specified before its using 
  * 在使用网络之前，必须完全指定网络
  * There were no free parameters to suit different problems. 
  * 没有自由参数来适应不同的问题。
* There are actually no well-known learning algorithms for standard MP neuron models.
* 对于标准的MP神经元模型，实际上并没有众所周知的学习算法。



### 8.1 Hebb’s Rules

* Hebb’s Rules and the historical background.
* Hebb's 规则和历史背景。



![image-20231025021820459](D:\笔记\笔记图片\image-20231025021820459.png)

* The McColloch-Pitts neuron made a base for a machine (network of units) capable of 
* McColloch-Pitts神经元为机器(单元网络)提供了一个基础
  * storing information and 
  * producing logical and arithmetical operations on it 
  * 储存资料及
    对其进行逻辑和算术运算
* The next step 
  * **<font color=red size=5>must be to realise another important function of the brain, which is to acquire new knowledge through experience, i.e. learning.</font>** 
  * **<font size=5 color=red>一定是为了实现大脑的另一个重要功能，那就是通过经验获取新知识，也就是学习。</font>**

* Learning means to change in response to experience 改变:根据经验而改变
* In an MP neural network, no free parameters. 
* 在MP神经网络中，没有自由参数。
* We need a new model, of which the parameters are easily changeable (to be learnt).
* 我们需要一种新的模型，它的参数容易改变(易于学习)。

![image-20231025022300748](D:\笔记\笔记图片\image-20231025022300748.png)

![*](D:\笔记\笔记图片\image-20231025013757195.png)

* Q: What parameters do you think can be free parameters?
* 问:你认为哪些参数可以是自由参数?

![image-20231025013804226](D:\笔记\笔记图片\image-20231025013804226.png)

* The ideal free parameters to adjust, and so to resolve learning, are **<font color=red>the weights of connections w</font>**.
* 为了解决学习问题，需要调整的理想自由参数是连接的**<font color=red>权重w</font>**。



![image-20231025014011808](D:\笔记\笔记图片\image-20231025014011808.png)

*  From now, we do NOT have the restriction on the weight. That is, the weight can be any real value. 
* 从现在起，我们对重量没有限制。也就是说，权重可以是任何实值。
* We do NOT **check the inhibitory input**.
* 我们不检查**抑制性输入**。



![image-20231025022557190](D:\笔记\笔记图片\image-20231025022557190.png)

* **Motivations are different. Thus, the models are different.**
* **动机是不同的。因此，模型是不同的。**



![image-20231025022945041](D:\笔记\笔记图片\image-20231025022945041.png)

* **<font color=red size=5>ANN learning rule is the rule how to adjust the weights of connections to get desirable output.</font>**
* **<font color=red>人工神经网络的学习规则是如何调整连接的权重以获得理想输出的规则。</font>**

![image-20231025041347403](D:\笔记\笔记图片\image-20231025041347403.png)

* Much work in Artificial Neural Networks focuses on the learning rules that define 
* 人工神经网络中的许多工作都集中在定义的学习规则上
  * how to change the weights of connections between neurons to better adapt a network to serve some overall function. 
  * 如何改变神经元之间连接的权重，以更好地使网络服务于某些整体功能。

![image-20231025041523760](D:\笔记\笔记图片\image-20231025041523760.png)

* As for the first time the problem was formulated in 1940s, when experimental neuroscience was limited, the classic definitions of these learning rules came not from biology, but 
* 至于第一次提出这个问题是在20世纪40年代，当时实验神经科学还很有限，这些学习规则的经典定义不是来自生物学，而是
  * from psychological studies of Donald Hebb and Frank Rosenblatt.
  * 来自唐纳德·赫布和弗兰克·罗森布拉特的心理学研究。

![image-20231025041640048](D:\笔记\笔记图片\image-20231025041640048.png)

* Hebb proposed that a **particular type of use-dependent modification of the connection strength of synapses might underlie learning in the nervous system.** 
* Hebb提出，一种特定类型的突触连接强度的使用依赖性修改可能是神经系统学习的基础。

![image-20231025041802145](D:\笔记\笔记图片\image-20231025041802145.png)



* Hebb introduced a neurophysiological postulate :
  *  “... When an axon of cell A  当A细胞的轴突
    * is near enough to excite a cell B and  足以激发细胞B和
    * repeatedly and persistently takes part in firing it,  反复且持续地参发送，
* some growth process or metabolic change takes place in one or both cells, such that A’s efficiency as one of the cells firing B, is increased. ”
* 在一个或两个细胞中发生了一些生长过程或代谢变化，因此A作为发射B的细胞之一的效率提高了。”



* **<font color=blue>这是一个生物学小知识，Hebb发现，如果一个细胞A作为轴突发射某物质B，发射了很多次后，发现发射B的效率提高了</font>**



![image-20231025042335593](D:\笔记\笔记图片\image-20231025042335593.png)

* “… Cells that fire together, wire together…”
* 一起放电的细胞连接在一起

![image-20231025042439830](D:\笔记\笔记图片\image-20231025042439830.png)

* **the long-term potentiation, a sustained state of increased synaptic efficacy consequent to intense synaptic activity**
* **长时程增强，是一种持续的突触效能增加的状态，这是由于强烈的突触活动引起的**





![image-20231025042449259](D:\笔记\笔记图片\image-20231025042449259.png)

* have now been found to cause the **long-term potentiation** in some neurons of **hippocampus** and other brain areas.
* 现在已经发现在海马体和其他大脑区域的一些神经元中引起长期增强。

![image-20231025042818572](D:\笔记\笔记图片\image-20231025042818572.png)

* Consider the above neuron, the weight Wti is what we want to learn.
* 考虑上面的神经元，权重Wti是我们想要学习的。 
* Again, here we allow wti could be other than -1 or 1, and we do not check inhibitory inputs. It is NOT an MP neuron.
* 同样，这里我们允许wti不是-1或1，**我们不检查抑制输入。它不是MP神经元**。

![image-20231025043050174](D:\笔记\笔记图片\image-20231025043050174.png)

* The simplest formulation of Hebb’s rule is to increase weight of connection at every next instant in the way:
* 赫布法则最简单的表述就是在接下来的每一个瞬间增加连接的权重:

![image-20231025043918840](D:\笔记\笔记图片\image-20231025043918840.png)

![image-20231025044105795](D:\笔记\笔记图片\image-20231025044105795.png)



* Thus, the weight of connection changes at the next instant only if both preceding input via this connection and the resulting output simultaneously are not equal to 0. 

* 因此，只有当通过该连接的前一个输入和同时产生的输出不等于0时，连接的权重在下一时刻才会改变。

![image-20231025044621974](D:\笔记\笔记图片\image-20231025044621974.png)

* The second equation emphasizes the correlation nature of a Hebbian synapse. 
* 第二个方程强调了Hebbian突触的相关性。
* Sometimes the Hebb’s rule is referred to as activity product rule. 
* 第二个方程强调了Hebbian突触的相关性。
* Hebb’s original learning rule referred exclusively to excitatory synapses
* 赫布最初的学习规则只涉及兴奋性突触

![image-20231025044853163](D:\笔记\笔记图片\image-20231025044853163.png)

## Lecture9 Hebbs_Rules_1 

![image-20231025050715345](D:\笔记\笔记图片\image-20231025050715345.png)

![image-20231025050822253](D:\笔记\笔记图片\image-20231025050822253.png)

![image-20231025050833252](D:\笔记\笔记图片\image-20231025050833252.png)



![image-20231025053744941](D:\笔记\笔记图片\image-20231025053744941.png)

![image-20231025053753289](D:\笔记\笔记图片\image-20231025053753289.png)

![image-20231025053759890](D:\笔记\笔记图片\image-20231025053759890.png)

![image-20231025053806791](D:\笔记\笔记图片\image-20231025053806791.png)

![image-20231025053814877](D:\笔记\笔记图片\image-20231025053814877.png)

![image-20231025053824611](D:\笔记\笔记图片\image-20231025053824611.png)

![image-20231025053833723](D:\笔记\笔记图片\image-20231025053833723.png)

![image-20231025053841157](D:\笔记\笔记图片\image-20231025053841157.png)

![image-20231025053849990](D:\笔记\笔记图片\image-20231025053849990.png)

![image-20231025053900395](D:\笔记\笔记图片\image-20231025053900395.png)

![image-20231025053913247](D:\笔记\笔记图片\image-20231025053913247.png)

![image-20231025053928395](D:\笔记\笔记图片\image-20231025053928395.png)

![image-20231025053936590](D:\笔记\笔记图片\image-20231025053936590.png)

![image-20231025053946005](D:\笔记\笔记图片\image-20231025053946005.png)

![image-20231025053955147](D:\笔记\笔记图片\image-20231025053955147.png)

![image-20231025054036984](D:\笔记\笔记图片\image-20231025054036984.png)

![image-20231025054052897](D:\笔记\笔记图片\image-20231025054052897.png)

![image-20231025055151396](D:\笔记\笔记图片\image-20231025055151396.png)

![image-20231025055430053](D:\笔记\笔记图片\image-20231025055430053.png)



* **Intuition: If two adjacent neurons always fire together, they should have strong relation (large weight).**
* **:如果两个相邻的神经元总是一起放电，那么它们应该有很强的关系(权重大)。**

![image-20231025055550920](D:\笔记\笔记图片\image-20231025055550920.png)



![image-20231025055712587](D:\笔记\笔记图片\image-20231025055712587.png)

![image-20231025060327958](D:\笔记\笔记图片\image-20231025060327958.png)

![image-20231025060340987](D:\笔记\笔记图片\image-20231025060340987.png)![image-20231025060457222](D:\笔记\笔记图片\image-20231025060457222.png)

* **The weights of the neuron model after Hebbian learning, reflects the most important feature of the average a(a上面有个横杠表示平均值) of the data set D.**
* **经过Hebbian学习的神经元模型的权重，反映了数据集D的平均a(a)(1)(杠)的最重要特征**。

![image-20231025060631486](D:\笔记\笔记图片\image-20231025060631486.png)

* **All the weights increase monotonously. Finally, each weight will become large enough such that any activated input can fire the neuron alone.**
* **所有的权重都是单调递增的。最后，每个权重将变得足够大，以至于任何激活的输入都可以单独激活神经元。**

## Week3 Questions with answer

![image-20231025061306541](D:\笔记\笔记图片\image-20231025061306541.png)

![image-20231025062642880](D:\笔记\笔记图片\image-20231025062642880.png)

![image-20231025062725033](D:\笔记\笔记图片\image-20231025062725033.png)

![image-20231025062737334](D:\笔记\笔记图片\image-20231025062737334.png)



![image-20231025062744628](D:\笔记\笔记图片\image-20231025062744628.png)



## Lecture10 Ojas_Rules_0

![image-20231026031018119](D:\笔记\笔记图片\image-20231026031018119.png)

* 这节课的内容比较多，这么解释一下：
* https://www.zhihu.com/question/26564573
* ![image-20231026031232890](D:\笔记\笔记图片\image-20231026031232890.png)

## 10.1 Normalized Hebb’s Rule (Oja’s rule)标准化赫布规则

![image-20231026031327563](D:\笔记\笔记图片\image-20231026031327563.png)

* By normalization, the weights will not monotonously increase, but converge after, which reflects the predisposition to different inputs. It plays an important role **in unsupervised learning or selforganisation.** 
* 归一化后，**权重不会单调增加，而是收敛**，反映了对不同输入的倾向性。它在**无监督学习或自组织**中起着重要作用。

![image-20231026031702557](D:\笔记\笔记图片\image-20231026031702557.png)

* 标准化 Normalization

### 10.1.1 Normalization

![image-20231026032248878](D:\笔记\笔记图片\image-20231026032248878.png)

* Check the following convergence criteria with a given small positive real δ
* 用给定的小正实δ检验下列收敛准则

![image-20231026032701308](D:\笔记\笔记图片\image-20231026032701308.png)

### 10.1.2 Example

![image-20231026033447130](D:\笔记\笔记图片\image-20231026033447130.png)

![image-20231026035348333](D:\笔记\笔记图片\image-20231026035348333.png)

![image-20231026035356600](D:\笔记\笔记图片\image-20231026035356600.png)

![image-20231026035406359](D:\笔记\笔记图片\image-20231026035406359.png)

![image-20231026035415729](D:\笔记\笔记图片\image-20231026035415729.png)

![image-20231026035423940](D:\笔记\笔记图片\image-20231026035423940.png)

![image-20231026035436442](D:\笔记\笔记图片\image-20231026035436442.png)

![image-20231026035446011](D:\笔记\笔记图片\image-20231026035446011.png)

![image-20231026035453670](D:\笔记\笔记图片\image-20231026035453670.png)

![image-20231026035502364](D:\笔记\笔记图片\image-20231026035502364.png)

![image-20231026035512417](D:\笔记\笔记图片\image-20231026035512417.png)



![image-20231026035521979](D:\笔记\笔记图片\image-20231026035521979.png)





## Lecture11 Ojas_Rules_1



![image-20231026041125877](D:\笔记\笔记图片\image-20231026041125877.png)

![image-20231026041133765](D:\笔记\笔记图片\image-20231026041133765.png)

* Intuition: Weights will NOT increase monotonously. The most frequent firing pattern will be remembered and finally dominate.
* 直觉:权重不会单调增加。最频繁的射击模式将被记住并最终占据主导地位。

![image-20231026041307025](D:\笔记\笔记图片\image-20231026041307025.png)

* The exact dynamics of the Oja’s rule have been solved by Wyatt and Elfaldel 1995 
* Wyatt和Elfaldel在1995年解决了Oja规则的确切动态
* It shows that the weight w → , where �∗ is the eigenvector of the largest eigenvalue �∗ of the matrix based on average �<. • Without normalization (the original Hebb’s rule) the weight of each connection grows exponentially with ��. With normalization (Oja’s rule) only the largest �∗ can survive.



### 11.1 Observations of the Running Example

* The data set D = {[1,0,1,0]}. That is, we only use one input to train the neuron. 
* 数据集D ={[1,0,1,0]}。也就是说，我们只用一个输入来训练神经元。
* Thus, the weights of the neuron [0.71,0.04,0.71,0.04] reflects the characteristic of this single input [1,0,1,0].
* 因此，神经元的权值[0.71,0.04,0.71,0.04]反映了该单一输入[1,0,1,0]的特征。

![image-20231026051838572](D:\笔记\笔记图片\image-20231026051838572.png)

* Applying Hebb’s rules (including the original one and the normalized one) on a neural network, we know that
* 在神经网络上应用Hebb规则(包括原始规则和归一化规则)，我们知道
* the weight of connection increases between nodes having activated outputs simultaneously
* 同时具有激活输出的节点之间的连接权重增加

![image-20231026051941728](D:\笔记\笔记图片\image-20231026051941728.png)

* the weight of connections between neurons eventually comes to represent the correlation between their outputs, and that fact is used to solve association problems. 
* 神经元之间连接的权重最终代表了它们输出之间的相关性，这一事实被用来解决关联问题。

![image-20231026052038448](D:\笔记\笔记图片\image-20231026052038448.png)

* As we did before, let a = (a1, a2, ⋯ , an) be the input vector. Let W = (w1, w2, ⋯ , wn) be the weight vector of the connections between the input vector a and the output X.
* 正如我们之前所做的，设a = (a1, a2，⋯an)为输入向量。设W = (w1, w2，⋯，wn)为输入向量a与输出向量X之间连接的权值向量。

![image-20231026052317162](D:\笔记\笔记图片\image-20231026052317162.png)

* 这个其实没什么太好说的，很简单，就是两个矩阵相乘

![image-20231026052404080](D:\笔记\笔记图片\image-20231026052404080.png)

![image-20231026052448993](D:\笔记\笔记图片\image-20231026052448993.png)

* 由此得出结论： Training data 和神经权重相关

![image-20231026052551415](D:\笔记\笔记图片\image-20231026052551415.png)

* As seen in previous lectures, training of a neuron with normalised Hebb’s learning rule results in a vector of weights of connections similar to the training input vector. 
* 如前所述，使用归一化的Hebb学习规则训练神经元会得到一个类似于训练输入向量的连接权重向量。
* Thus, **the neuron “remembers” the training pattern via increasing weight of corresponding connections**.
* 因此，**神经元通过增加相应连接的权重来“记住”训练模式**。 

![image-20231026052752956](D:\笔记\笔记图片\image-20231026052752956.png)

* If the trained network is presented with an input vector a′ similar to the training one a, it should be also similar to the weight of the network W, and result in the similar neuron output.
* 如果训练网络的输入向量a '与训练向量a相似，那么它也应该与网络W的权值相似，从而得到相似的神经元输出。

![image-20231026053158296](D:\笔记\笔记图片\image-20231026053158296.png)

* If the trained network is presented with an input vector a′ similar to the training one a, it should be also similar to the weight of the network W, and result in the similar neuron output a.
* 如果训练网络的输入向量a '与训练向量a相似，那么它也应该与网络W的权值相似，从而得到相似的神经元输出a。
* One may say that , the network “recognises” the new input or “associates” it with the training one.
* 有人可能会说，神经网络“识别”了新的输入，或者将其与训练的输入“关联”起来。 

![image-20231026053320074](D:\笔记\笔记图片\image-20231026053320074.png)

* Definition: **Association is the task of mapping patterns to patterns.** 
* 定义:**关联是将模式映射到模式的任务。**
  * An **associative memory** is to learn and remember the mapping between two unrelated pattens. 
  * **定联想记忆**是学习和记住两个不相关模式之间的映射。
  *  For instance, a person may learn a word and its meaning before (learn the mapping between word and meaning). When the person reads the word that is spelled incorrectly, she or he may know it has the same meaning with the correct word by association (remember the mapping).
  * 例如，一个人可以先学习一个单词和它的意思(学习单词和意思之间的映射)。当这个人读到拼写错误的单词时，她或他可能通过联想知道它与正确的单词有相同的意思(记住映射)。



![image-20231026054344111](D:\笔记\笔记图片\image-20231026054344111.png)

* We **do not label any input** in the data set during learning. The weight updating in each iteration only **involves the input, the output and the current weight.** 
* 在学习过程中，我们不**标记数据集中的任何输入**。每次迭代中的权值更新只**涉及输入、输出和当前权值**。
* We do not care what the output pattern means. We **care which inputs are considered similar** by the network. That is, **unsupervised** learning.
* 我们不关心输出模式的含义。**我们关心的是网络认为哪些输入是相似的。也就是无监督学习。**

![image-20231026054539968](D:\笔记\笔记图片\image-20231026054539968.png)

* Unsupervised learning is a type of machine learning in which the algorithm **is not provided with any pre-assigned labels or scores for the training data.** As a result, unsupervised learning algorithms must **first self-discover any naturally occurring patterns** in that training data set. 
* 无监督学习是一种机器学习，其中**算法没有为训练数据提供任何预先分配的标签或分数。**因此，无监督学习算法必须**首先自我发现训练数据集中任何自然发生的模式**。
* It will be much clearer when we extend the network with single output to the network with multiple outputs.
* 当我们将单输出的网络扩展到多输出的网络时，就会清楚得多。

![image-20231026055122453](D:\笔记\笔记图片\image-20231026055122453.png)

* What can we expect for a multi-output network? 
* 对于多输出网络，我们可以期待什么?
* **For a single output network,** we can strengthen the link between an input pattern and an output by **normalized Hebb’s rule**. The network can therefore **recognize other similar inputs;**
* **对于单输出网络**，我们可以通过**归一化的Hebb规则**来加强输入模式和输出模式之间的联系。因此，网络可以**识别其他类似的输入;**
* **For a multi-output networ**k, it is supposed to recognize multiple types of patterns. Each input could be recognized as either one type of pattern, or none of them. (Clustering)
* 对于一个多输出网络，它应该能够识别多种类型的模式。每个输入可以被识别为一种模式，也可以不被识别。**(聚类)**

![image-20231026055245673](D:\笔记\笔记图片\image-20231026055245673.png)





## Lecture12  Kohonen_Rules_0

### 12.1 Unsupervised Learning 非监视学习

* Unsupervised learning is a type of machine learning in which the algorithm is not provided with any pre-assigned labels or scores for the training data. As a result, unsupervised learning algorithms must first self-discover any naturally occurring patterns in that training data set. 
* 无监督学习是一种机器学习，其中算法没有为训练数据提供任何预先分配的标签或分数。因此，无监督学习算法必须首先自我发现训练数据集中任何自然发生的模式。
* **A common example is clustering, that is, an unsupervised network can group similar sets of input patterns into clusters predicated upon a predetermined set of criteria relating the components of the data.** 
* **无监督学习是一种机器学习，其中算法没有为训练数据提供任何预先分配的标签或分数。因此，无监督学习算法必须首先自我发现训练数据集中任何自然发生的模式。**
* Clustering can be achieved when we extend the single neuron to the network with multiple outputs.
* 当我们将单个神经元扩展到具有多个输出的网络时，可以实现聚类。



### 12.2 Kohonen Rule: Competitive Learning

![image-20231026055538149](D:\笔记\笔记图片\image-20231026055538149.png)

* We consider a one-layer neural network with multiple outputs. 
* 我们考虑一个具有多个输出的单层神经网络。
* In competitive learning, as the name implies, an output neuron of a network compete among all the outputs to be updated (regarding the weights). 
* 在竞争学习中，顾名思义，一个网络的输出神经元在所有需要更新的输出之间竞争(关于权重)。
* Whereas in a neural network based on Hebbian learning several output neurons may be updated simultaneously, in competitive learning only a single output neuron is updated at any instant. 
* 在基于Hebbian学习的神经网络中，多个输出神经元可以同时更新，而在竞争学习中，每个时刻只更新一个输出神经元。
* This makes competitive learning highly suited to discover statistically important features that may be used to classify a set of input patterns. 
* 这使得竞争性学习非常适合于发现统计上重要的特征，这些特征可能用于对一组输入模式进行分类。

![image-20231026062700745](D:\笔记\笔记图片\image-20231026062700745.png)

* Teuvo Kohonen suggested **a network in which the output neurons compete for the right to respond to an input.** 
* Teuvo Kohonen提出了一个网络，**在这个网络中，输出神经元会竞争对输入的响应权**
* The learning rule first assumes that **one of the output neurons, say the j-th, has maximum value of the instant state Sj at that instant.** 
* 学习规则首先假设其中**一个输出神经元，比如说第j个神经元，在那个时刻具有瞬时状态Sj的最大值。**
* That neuron is declared to be the winner, and **only the weights of the winner’s connections**
* 该神经元被宣布为获胜者，并且**只有获胜者的连接的权重**

![image-20231026063622320](D:\笔记\笔记图片\image-20231026063622320.png)

* We further relax the restriction on the input type, i.e., we allow real inputs in the competitive learning. 
* 我们进一步放宽了输入类型的限制，即在竞争性学习中允许真实输入
* Only the winner outputs a 1, while others output 0.
* 只有赢家输出1，其他人输出0。

![image-20231026063726274](D:\笔记\笔记图片\image-20231026063726274.png)

* The learning rule first assumes that one of the output neurons, say the j-th, has maximum value state Sj at that instant.
* 学习规则首先假设其中一个输出神经元，比如说第j个，在那一刻具有最大值状态Sj。

![image-20231026063824262](D:\笔记\笔记图片\image-20231026063824262.png)

* That neuron is declared the winner, and only its vector of connections weights.
* 该神经元被宣布为赢家，只有它的连接向量权重。
  * ![image-20231026063918628](D:\笔记\笔记图片\image-20231026063918628.png)





![image-20231026064204581](D:\笔记\笔记图片\image-20231026064204581.png)



![image-20231026064243929](D:\笔记\笔记图片\image-20231026064243929.png)

* Having the maximum weighted input, means that the winning output neuron has the vector of connection weights most similar to the input vector.
* 具有最大的加权输入，意味着获胜的输出神经元具有与输入向量最相似的连接权重向量。

![image-20231026064426402](D:\笔记\笔记图片\image-20231026064426402.png)

![image-20231026064433993](D:\笔记\笔记图片\image-20231026064433993.png)

![image-20231026064443632](D:\笔记\笔记图片\image-20231026064443632.png)

* After the adjustment, the winner connection weights tend to even better correlate with the input pattern. 
* 调整后，赢家连接权重倾向于更好地与输入模式相关。

![image-20231026070501704](D:\笔记\笔记图片\image-20231026070501704.png)

![image-20231026070510330](D:\笔记\笔记图片\image-20231026070510330.png)

![image-20231026070519717](D:\笔记\笔记图片\image-20231026070519717.png)

![image-20231026070527266](D:\笔记\笔记图片\image-20231026070527266.png)



### 12.3 Self-Organizing Map (SOM)

![image-20231026070953681](D:\笔记\笔记图片\image-20231026070953681.png)

* We are interested in a specific application of Kohonen learning rule (competitive learning), **self-organizing map (SOM).**
* 我们感兴趣的是Kohonen学习规则(竞争学习)的一个具体应用，**自组织映射(SOM)**
* **SOM is used to produce a lowdimensional (typically two-dimensional)** representation of a higher dimensional data set while preserving the topological structure of the data. For instance, in left figure, a SOM maps a n-dimensional input to a 2-dimensional space. **It can be used for clustering or visualization.**
* SOM用于生成高维数据集的低维**(通常是二维)**表示，同时保留数据的拓扑结构。例如，在左图中，SOM将n维输入映射到2维空间。**它可以用于集群或可视化。**

![image-20231026071153753](D:\笔记\笔记图片\image-20231026071153753.png)

* The training of such specific networks is based on Kohonen learning rule (competitive learning).
* 这种特定网络的训练基于Kohonen学习规则(竞争性学习)。

![image-20231026071307522](D:\笔记\笔记图片\image-20231026071307522.png)

* Sometimes, the winning neighbourhood is extended beyond the single neuron winner, so that it includes the neighbouring neurons, for which some corrections to the connection weights may also be done.
* 有时，获胜邻域被扩展到超越单个获胜神经元的范围，使其包括相邻的神经元，因此也可以对连接权值进行一些修正。

![image-20231026071949249](D:\笔记\笔记图片\image-20231026071949249.png)

![image-20231026071957107](D:\笔记\笔记图片\image-20231026071957107.png)

* In the map, location of the most strongly excited neurons (winner) is correlated with the certain input signals. 
* 在地图上，最强烈兴奋的神经元(赢家)的位置与特定的输入信号相关。
* Neighbouring excited neurons correspond to inputs with similar features.
* 邻近的兴奋神经元与具有相似特征的输入相对应。

![image-20231026072006381](D:\笔记\笔记图片\image-20231026072006381.png)

* Because in the training phase weights of the whole neighbourhood are moved in the same direction, similar items tend to excite adjacent neurons. Therefore, SOM forms a semantic map where similar samples are mapped close together and dissimilar ones apart.
* 因为在训练阶段，整个邻域的权值都向同一方向移动，所以相似的项目往往会激发相邻的神经元。因此，SOM形成了一个语义图，其中相似的样本被紧密地映射在一起，不相似的样本被分开。



## Class Test 1



## Lecture 13 Peceptron_0

### 13.1 ANN Learning Rules

* The McCullock-Pitts neuron made a base for a machine (network of units) capable of
* The McCullock-Pitts neuron为机器（单元网络）奠定了基础。
  * **<font color=red>storing information and</font>**
  * **<font color=red>存储信息</font>**
  * **<font color=red>producing logical and arithmetical operations on it</font>**
  * **<font color=red>对其进行逻辑和算术运算</font>**

* 这里先简化一下这个神经元是干嘛用的
* ![  ](D:\笔记\笔记图片\image-20231126000614230.png)

* The next step
  * must be to realise another important function of the brain, which is
    * to acquire new knowledge through experience, i.e. learning.
    * 下一步，是实现大脑的重要功能之一，学习。

![image-20231126000823094](D:\笔记\笔记图片\image-20231126000823094.png)

* ANN learning rule is the rule **how to adjust the weights of connections to get desirable output.**
* ANN 学习规则是如何**调整连接权重以获得理想输出的规则**。



### 13.2 MP Neuron vs. Hebb’s Rule

![image-20231126001045301](D:\笔记\笔记图片\image-20231126001045301.png)



* Given a fixed MP neuron, that is, **all weights of connections** and neuron threshold are set up **in advance.**
* 给定一个固定的 MP 神经元，即事**先设置好所有连接权重**和神经元阈值。

![image-20231126001512586](D:\笔记\笔记图片\image-20231126001512586.png)

![image-20231126001604575](D:\笔记\笔记图片\image-20231126001604575.png)

![image-20231126003249849](D:\笔记\笔记图片\image-20231126003249849.png)



### 13.3 Unsupervised Learning 无监督学习

* Unsupervised learning is a type of machine learning in which **<font color=red size=5>the algorithm is not provided with any pre-assigned labels or scores for the training data.</font>** As a result, unsupervised learning algorithms must first **self-discover any naturally occurring patterns** in that training data set.
* 无监督学习是机器学习的一种类型，在这种类型中，**算法没有为训练数据提供任何预先分配的标签或分数。**因此，无监督学习算法必须首先**自我发现训练数据集中任何自然出现的模式**。

![image-20231126004138235](D:\笔记\笔记图片\image-20231126004138235.png)

* 这个问题是在 20 世纪 40 年代首次提出的、在神经科学实验还很有限的情况下，这些学习规则的经典定义
  这些学习规则的经典定义并非来自生物学，而是心理学



### 13.4 Perceptron 感知器

* Rosenblatt (1958) explicitly considered the problem of pattern recognition, where a “teacher” is essential. (Consider the difference with unsupervised learning)
* 罗森布拉特（Rosenblatt，1958 年）明确考虑了模式识别问题，在这个问题上，"教师 "是必不可少的。(考虑与无监督学习的区别）
* A Perceptron is a neural network that changes with “experience” using an **error-correction rule.**
* 感知器是一种利用纠错规则随 "经验 "变化的神经网络。
* According to the rule, **weight of a neuron changes when it makes error response to the input presented to the network.**
* 根据这一规则，**当神经元对网络输入做出错误响应时，其权重就会发生变化。**

![image-20231126005252762](D:\笔记\笔记图片\image-20231126005252762.png)

![image-20231126004749106](D:\笔记\笔记图片\image-20231126004749106.png)

* The simplest architecture of perceptron comprises **one layer of idealised “neurons”**, which we also sometimes call “units” of the network.
* 最简单的感知器结构包括**一层理想化的 "神经元"**，我们有时也称其为网络的 **"单元"**。

 ![image-20231126004837149](D:\笔记\笔记图片\image-20231126004837149.png)

![image-20231126012104933](D:\笔记\笔记图片\image-20231126012104933.png)

* **输入层（Input Layer）**：由一系列输入单元*a*1,*a*2,...,*a**n* 组成，其中 a0=1*a*0=1 通常表示偏置单元，它的作用是允许输出阈值可调整。
* **输出层（Output Layer）**：包含一个或多个输出神经元 *x* *j*，在这个例子中，只显示了一个输出神经元。

![image-20231126012752329](D:\笔记\笔记图片\image-20231126012752329.png)

* The two layers are fully interconnected, i.e. every input neuron is connected to every output neuron.
* 两层都是充分互联的

![image-20231126012952359](D:\笔记\笔记图片\image-20231126012952359.png)

* Semantically, a perceptron can be considered as a vector-valued function that maps
* 从语义上讲，感知器可被视为 可视为一个向量值函数

**![Uploaded image](D:\笔记\笔记图片\av4RUJF5eUbei8c3WkAVEwhUKvfVOO0JyqW3GDY%3D.png)**

* 尽管每个输出神经元都接收相同的输入，但它们对应的连接权重 *w**ji* 是独立的。这意味着即使对于相同的输入，不同的输出神经元也可能有不同的反应，因为它们通过独立的权重来加权输入信号。
* 幻灯片中提到的“individual connections”表明每个输入和输出之间的连接是唯一的，每个连接都有自己的权重 *w**ji*。由于这些权重是独立的，每个输出神经元可以独立调整，以便在学习过程中进行优化。
* 以 *j*-th 输出神经元为例，它的输出 *X**j* 会由输入的加权和通过激活函数 *f* 确定。权重 0*w**j*0（等于 −−*θ**j*）是偏置权重，用于调节激活阈值。这种结构允许感知机模型对每个输出神经元进行个性化的学习，使其能够识别输入模式并据此做出独立的决策。

![image-20231126014952246](D:\笔记\笔记图片\image-20231126014952246.png)

![image-20231126015104405](D:\笔记\笔记图片\image-20231126015104405.png)

* a0=1是一个偏置单元，往往用于调整激活函数的阙值。这么想，当a0大,wj0为正数，那么就以激活，反之。

![image-20231126015324246](D:\笔记\笔记图片\image-20231126015324246.png)

* With this trick, we have no need to set a threshold manually. Now we can train the threshold like weights.
* 有了这个技巧，我们就不需要 手动设置阈值。现在我们 可以像训练权重一样训练阈值。

![image-20231126015422997](D:\笔记\笔记图片\image-20231126015422997.png)

#### 13.4.1 MP Neuron vs. Perceptron (Syntax and Semantics)

![image-20231126020800637](D:\笔记\笔记图片\image-20231126020800637.png)

![image-20231126020817894](D:\笔记\笔记图片\image-20231126020817894.png)

![image-20231126020846812](D:\笔记\笔记图片\image-20231126020846812.png)

![image-20231126020904287](D:\笔记\笔记图片\image-20231126020904287.png)

![image-20231126021021811](D:\笔记\笔记图片\image-20231126021021811.png)

* - 与Hebb法则类似，我们通过调整两层之间的权重（训练）来学习 知识。
  - 如果数据集是无标记的，我们可以训练感知器网络将输入分组到不同的组中（无监督学习）。

![image-20231126021141199](D:\笔记\笔记图片\image-20231126021141199.png)

* 如果数据集是有标签的，我们就可以训练感知器网络，使其针对特定输入产生所需的输出（监督学习）。

## Lecture 14 Peceptron_1

![image-20231126021505580](D:\笔记\笔记图片\image-20231126021505580.png)

* Rosenblatt (1958) explicitly considered the problem of pattern recognition, where a “teacher” is essential.
* A Perceptron is a neural network that changes with “experience” using an **<font color=red>error-correction rule</font>**. (Supervised learning!)
* According to the rule, **<font color=red>weight of a response unit changes when it makes error response to the input presented to the network.</font>**
* **根据该规则，当响应单元对呈现给网络的输入做出错误响应时，响应单元的权重会发生变化。**



### 14.1.1 Perceptron Training

![image-20231126021748237](D:\笔记\笔记图片\image-20231126021748237.png)

* **<font color=red>Weights 𝑤ji</font>** of connections between two layers are changed according to **<font color=red>perceptron learning rule</font>**, so the network is more likely to produce the desired output in response to certain inputs.
* 两层之间连接的**权重𝑤ji** 会根据**感知器学习规则**发生变化，因此网络更有可能对特定输入产生所需的输出。

![image-20231126023302958](D:\笔记\笔记图片\image-20231126023302958.png)

* The perceptron is trained by using a training set with target outputs (labels).
* 感知器通过使用带有目标输出（标签）的训练集进行训练。
  * **Training set**: a set of input patterns repeatedly presented to the network during training;
  * **训练集**：在训练过程中反复呈现给网络的一组输入模式；
  * **Target/desired output (label)**: the pre-defined correct output of an input pattern in the training set.
  * **目标/预期输出（标签）**：训练集中输入模式的预定义正确输出。

![image-20231126024714824](D:\笔记\笔记图片\image-20231126024714824.png)

* Every input pattern is used multiple times for training
* 每个输入模式都会被多次用于训练

![image-20231126024800195](D:\笔记\笔记图片\image-20231126024800195.png)

* Input pattern in the set is 𝒏-dimensional! Note 𝑎 ! =1
* 集合中的输入模式为 𝒏 维！注意 𝑎 0=1

![image-20231126024903078](D:\笔记\笔记图片\image-20231126024903078.png)

* Note that in unsupervised learning, no label is needed.
* 请注意，在无监督 学习中不需要标签。

![image-20231126025003795](D:\笔记\笔记图片\image-20231126025003795.png)

* The network outputs 𝑿 𝒋 are then **compared to the desired outputs** specified in the training set and obtain the error.
* 然后将网络输出 𝑿 𝒋 与训练集中**指定的期望输出进行比较**，得出误差。
* 这是一个有监督学习，比较输出结果和标准结果得出误差是一个很典型的监督学习特征。

![image-20231126025454546](D:\笔记\笔记图片\image-20231126025454546.png)

* The **error of an output neuron** is the difference between the target output and the instant one.
* **神经元的错误**输出是目标输出与即时输出的差值。

![image-20231126025717617](D:\笔记\笔记图片\image-20231126025717617.png)

* The **errors** are then used to readjust the values of the weights of the connections.
* 然后利用**误差**重新调整连接的权重值。

![image-20231126025840216](D:\笔记\笔记图片\image-20231126025840216.png)

* The weights readjustment is done in such a way that the network is – on the whole – **more likely to give the desired response next time.**
* 权重重新调整的方式是使网络整体上**更有可能在下一次做出预期的响应**。

* The **goal of the training** is to arrive at a single set of weights that allow each input in the training set to be mapped to the correct output by the network.
* 训练的**目的是获得一组权重**，使网络能将训练集中的每个输入映射到正确的输出。



### 14.1.2 Weight Update

![image-20231126030835562](D:\笔记\笔记图片\image-20231126030835562.png)

![image-20231128004732106](D:\笔记\笔记图片\image-20231128004732106.png)

#### 14.1.2.1 Difference with Hebb`s Rule

![image-20231128005158158](D:\笔记\笔记图片\image-20231128005158158.png)



![image-20231128005417818](D:\笔记\笔记图片\image-20231128005417818.png)

* The value of the “learning rate” C is  
  * usually set below 1 and 
  * 经常设置在1以下
  * determines the amount of correction made in a single iteration.
  * 决定了单词迭代的修正量

![image-20231128005349786](D:\笔记\笔记图片\image-20231128005349786.png)

* The overall learning time of the network is affected by the value of the “learning rate” C: slower for small values and faster for larger.
* 越小的学习率意味着越慢的学习时间，反之。

![image-20231128005955579](D:\笔记\笔记图片\image-20231128005955579.png)

* The network performance during training session is measured by a **root-mean-square (RMS)** error value. 
* 训练过程中的网络性能以**均方根误差值**来衡量。

![image-20231128010154312](D:\笔记\笔记图片\image-20231128010154312.png)

* 当RMS=0的时候，停止计算。

![image-20231128010451887](D:\笔记\笔记图片\image-20231128010451887.png)

* The first sum is taken over all patterns in the training set, and the second sum is taken over all output neurons. 
* 第一个总和是训练集中所有模式的总和，第二个总和是所有输出神经元的总和。
* 1. **对所有模式进行求和**：这个步骤累加了整个数据集的误差贡献。
* 2. **对每个模式的所有输出神经元的误差平方进行求和**：这个步骤考虑了单个数据点对所有输出的贡献。

![image-20231128011608524](D:\笔记\笔记图片\image-20231128011608524.png)

* 由于t，r,m,都是固定的值，所以将RMS理解成一个函数，唯一受影响的就是X。

![image-20231128011806010](D:\笔记\笔记图片\image-20231128011806010.png)

* 若是将X也视作一个函数，影响X的值就是各个权重w，因为a是固定的，是一个恒定值

![image-20231128012350584](D:\笔记\笔记图片\image-20231128012350584.png)

* 最终可以获得这个函数

![image-20231128012437939](D:\笔记\笔记图片\image-20231128012437939.png)

* **<font color=red>The best performance of the network</font>** over a given data set D corresponds to **<font color=red>the minimum of the RMS error</font>**, and we adjust the weight of connections w in order to reach the minimum.
* 在给定的数据集 D 上，网络的最佳性能与均方根误差的最小值相对应，我们通过调整连接权重 w 来达到最小值。

![image-20231128013437613](D:\笔记\笔记图片\image-20231128013437613.png)

![image-20231128013458705](D:\笔记\笔记图片\image-20231128013458705.png)

![image-20231128013754599](D:\笔记\笔记图片\image-20231128013754599.png)

* 最终，函数收敛converged。

## Lecture15_Peceptron_2

### 15.1 **A Running Example**

![image-20231128060256517](D:\笔记\笔记图片\image-20231128060256517.png)



![image-20231128061555933](D:\笔记\笔记图片\image-20231128061555933.png)



![image-20231128061607332](D:\笔记\笔记图片\image-20231128061607332.png)

![image-20231128061701216](D:\笔记\笔记图片\image-20231128061701216.png)

![image-20231128061710883](D:\笔记\笔记图片\image-20231128061710883.png)

## Lecture 16 Peceptron_3

### 16.1 Convergence of Perceptron Learning Algorithm

* **<font color=red size=5>The perceptron learning algorithm can converge for the data set that is linearly separable</font>**
* 对于线性可分离的数据集，感知器学习算法可以收敛

![image-20231128064347408](D:\笔记\笔记图片\image-20231128064347408.png)

* Without loss of generality, we consider a simplified case. 
* 在不失一般性的前提下，我们考虑一种简化的情况。
  * There is only one output in the network
  * 我们一般考虑在神经网络只输出一个结果
  * The learning rate C is set as 1.
  * 学习率被设置为1

![image-20231128064533510](D:\笔记\笔记图片\image-20231128064533510.png)

* Recall the following informal definition we mentioned for MP neuron. 
* 回顾一下我们提到的 MP 神经元的非正式定义。
* **<font size=5>Linear separability</font>** (for Boolean functions): There exists a line (plane) such that all inputs which produce a 1 for the function lie on one side of the line (plane) and all inputs which produce a 0 lie on other side of the line (plane).
* 线性可分性（布尔函数）： 存在一条线（一个平面），使得函数产生 1 的所有输入都位于该线（平面）的一边，而产生 0 的所有输入都位于该线（平面）的另一边。

* ![image-20231128065104038](D:\笔记\笔记图片\image-20231128065104038.png)

![image-20231128065236972](D:\笔记\笔记图片\image-20231128065236972.png)

![image-20231128065814800](D:\笔记\笔记图片\image-20231128065814800.png)

#### 16.1.1 Perceptron Learning Algorithm (One output)

![image-20231128070039656](D:\笔记\笔记图片\image-20231128070039656.png)

* Rewriting the general perceptron learning algorithm. 
  * Since we only consider one output, the result becomes a weight vector w=(w0, w1, w2......, wn)  rather than the weight matrix. Here wi represents for the weight of the connection between the i-th input and the output.
  * 由于我们只考虑一个输出，结果就变成了权重向量 w=（w0, w1, w2......, wn），而不是权重矩阵。这里 wi 代表第 i 个输入和输出之间的连接权重。

![image-20231128071912265](D:\笔记\笔记图片\image-20231128071912265.png)

* 由于线性可分，我们将D`分为P和N两个数组，通过这个来对进行划分。

![image-20231128072120081](D:\笔记\笔记图片\image-20231128072120081.png)

* **The convergence of the learning rule means we successfully find a feasible w∗!** 
* **当学习率递归的时候意味着寻找特征w成功**

![image-20231128072347291](D:\笔记\笔记图片\image-20231128072347291.png)

![image-20231128072516169](D:\笔记\笔记图片\image-20231128072516169.png)

![image-20231128072601258](D:\笔记\笔记图片\image-20231128072601258.png)



#### 16.1.2 Geometric Interpretation 几何解读

![image-20231128072736562](D:\笔记\笔记图片\image-20231128072736562.png)

* Red arrows denote the points in P, 
* 红色箭头表示在集合P的点
* Blue arrows denote the points in N, 
* 蓝色的箭头表示在集合N的点
* Thick black line denotes the barrier of w*T a = 0

![image-20231128073740105](D:\笔记\笔记图片\image-20231128073740105.png)

![image-20231128073728493](D:\笔记\笔记图片\image-20231128073728493.png)

*  **<font size=5>Orthogonal 横向</font>**

![image-20231128074227748](D:\笔记\笔记图片\image-20231128074227748.png)



![image-20231128074738388](D:\笔记\笔记图片\image-20231128074738388.png)



![image-20231128074956470](D:\笔记\笔记图片\image-20231128074956470.png)

![image-20231128075011764](D:\笔记\笔记图片\image-20231128075011764.png)

![image-20231128075114948](D:\笔记\笔记图片\image-20231128075114948.png)

![image-20231128080434134](D:\笔记\笔记图片\image-20231128080434134.png)

![image-20231128080817764](D:\笔记\笔记图片\image-20231128080817764.png)

* 这里的权重wk被分配为1

![image-20231128084625011](D:\笔记\笔记图片\image-20231128084625011.png)

![image-20231128084732241](D:\笔记\笔记图片\image-20231128084732241.png)

![image-20231128084802452](D:\笔记\笔记图片\image-20231128084802452.png)

* 我们得到了分母的上限

![image-20231128085329791](D:\笔记\笔记图片\image-20231128085329791.png)

![image-20231128085531575](D:\笔记\笔记图片\image-20231128085531575.png)

* 得到结果

![image-20231128085612816](D:\笔记\笔记图片\image-20231128085612816.png)

![image-20231128085640957](D:\笔记\笔记图片\image-20231128085640957.png)

![image-20231128085650532](D:\笔记\笔记图片\image-20231128085650532.png)

![image-20231128090309275](D:\笔记\笔记图片\image-20231128090309275.png)



## Lecture 17  Multi-Layer Perceptron_0

![image-20231128222745929](D:\笔记\笔记图片\image-20231128222745929.png)

![image-20231128223654328](D:\笔记\笔记图片\image-20231128223654328.png)

* 具体来说，我们关心的是S这个公式的符号。
* w的方向非常重要，而不是长度。比如|w|不中用
* 将学习规则视为在不同情况下改变 w 方向的方法。
* Consider the learning rule as the ways to change the direction of w under different situations.
* 那么，感知器学习规则的收敛性可以认为是，w 最终与存在但未知的最优 w* 具有相似的方向。
* Then the convergence of perceptron learning rule can be considered as that w finally has the similar direction with the optimal w* that exists but is unknown.
* 在证明过程中，我们要做的是证明 w 和 w∗ 之间的夹角会随着w∗数目的增加而变小（不一定是单调的）。和 w∗ 之间的夹角会随着误分类次数的增加而变小（不一定是单调的 的角度会越来越小（不一定是单调的），并且不会小于 0。

![image-20231128224321379](D:\笔记\笔记图片\image-20231128224321379.png)

### 17.1 Beyond Linear Separability

![image-20231128224521993](D:\笔记\笔记图片\image-20231128224521993.png)

* 现在我们知道，对于线性可分离的数据集，感知器学习算法最终可以收敛。收敛。
* **那么，不可线性分离的数据集呢？**
* **最著名的例子就是 "XOR"（排他 "OR"）门、 称为 XOR 问题。**



#### 17.1.1 The XOR Problem （一个典型的非线性问题）

![image-20231128225013099](D:\笔记\笔记图片\image-20231128225013099.png)

![image-20231128230120370](D:\笔记\笔记图片\image-20231128230120370.png)

* 由上面这个式子可以证明XOR不符合线性可分



![image-20231128231233712](D:\笔记\笔记图片\image-20231128231233712.png)

* Minsky and Papert showed that in the case of any non-linearly separable problem, such as XOR, in the network architecture there must be **<font color=red size=5>“hidden neurons”</font>**, i.e. the neurons with output not available to the outside world, in order to help turn the problem into a linearly separable one for the outputs.
* 明斯基和帕帕特指出，在任何非线性可分问题（如 XOR）的情况下，网络结构中必须有 "隐藏神经元"，即对外部世界没有输出的神经元，以帮助将问题转化为输出的线性可分问题。

#### 17.1.2 Hidden Neurons

![image-20231128233328557](D:\笔记\笔记图片\image-20231128233328557.png)

* Minsky and Papert showed that in the case of any non-linearly separable problem, such as XOR, in the network architecture there must be “hidden neurons”, i.e. the neurons with output not available to the outside world, in order to help turn the problem into a linearly separable one for the outputs.

* 明斯基和帕帕特指出，在任何非线性可分问题（如 XOR）的情况下，网络结构中必须有 "隐藏神经元"，即对外部世界没有输出的神经元，以帮助将问题转化为输出的线性可分问题。

![image-20231128234001899](D:\笔记\笔记图片\image-20231128234001899.png)

* The three-layer perceptron below is capable to represent XOR. 
* 下面的三层感知器能够表示 XOR。
* Each hidden neuron separates the input space into a **closed positive** and **open negative half-space**. 
* 每个隐藏神经元将输入空间分为封闭的**正半空间和开放的负半空间**。
* The left bottom figure shows the linear separations defined by each hidden unit, while the positive half-spaces are shaded. 
* 左下图显示了每个隐藏单元定义的线性分隔，而正半空则用阴影表示。



* 这里解释一下这里的hidden neuron, **标注为 −0.5−0.5 的值是两个隐藏层神经元的偏置项。**在神经网络中，每个神经元可以有一个偏置项，这个偏置项是在计算神经元的总输入时加上的一个常数。偏置项的作用是使得神经元激活函数的阈值可以调整，这样即使所有输入都是零，神经元也可以输出一个非零值。
* ![image-20231128234429518](D:\笔记\笔记图片\image-20231128234429518.png)



![image-20231128234448598](D:\笔记\笔记图片\image-20231128234448598.png)



#### 17.1.3 Multilayer Perceptron 多重感知器

![image-20231128234556845](D:\笔记\笔记图片\image-20231128234556845.png)

* A multilayer perceptron (MLP) is a layered architecture of neurons, where 
* 多层感知器（MLP）是一种神经元分层结构，其中
  * all the neurons are divided into - subsets, each set is called a layer; 
  * 所有神经元被分为 - 个子集，每个子集称为一层；
  * There are only connections between two adjacent layers. Usually, the neurons within a layer are not connected to each other, though some neural models make use of this kind of architecture. 
  * 相邻两层之间只有连接。通常情况下，层内的神经元之间没有连接，但有些神经模型会使用这种结构。

![image-20231128234918046](D:\笔记\笔记图片\image-20231128234918046.png)

* The first layer is **the input layer** (We don’t usually count it); 
* 第一层是输入层（我们通常不计算它）；
* The last layer is **the output layer**. 
*  最后一层是输出层。
* All other layers with no direct connections from or to the outside are called **hidden layers**. 
* 所有与外部没有直接联系的其他层都称为隐藏层。



![image-20231128235232325](D:\笔记\笔记图片\image-20231128235232325.png)

* We consider the fully-connected architectures in this module, that is, **every neuron from one layer is connected to all neurons in the following layer.** 
* 我们在本模块中考虑了全连接架构，**即一层的每个 都与下一层的所有神经元相连接**
* Each connection is associated with **a real weight and a real bias**. 
* 每个连接都与**实际权重和实际偏差**相关联。
* Inputs are real. Outputs are real.
* 输入是真实的。输出是真实的。



![image-20231128235451085](D:\笔记\笔记图片\image-20231128235451085.png)

* The input is processed and propagated from one layer to the next, until the final result is computed. 
* 输入经过处理后从一层传播到下一层，直到计算出最终结果。
* This process represents **<font color=red size=5>the forward propagation</font>**. 
*  这个过程就是**前向传播**。
* For simplicity, from now we assume **<font color=red>the biases in the network are all zero.</font>**
* 为简单起见，从现在起我们假设**网络中的偏差均为零。**



![image-20231128235815096](D:\笔记\笔记图片\image-20231128235815096.png)

* The difference of the multilayer perceptron, compared to the single layer one, is that the output value X' of the first layer is not the output value of the multilayer perceptron any more. 
* 多层感知器与单层感知器的区别在于，第一层的输出值 X'不再是多层感知器的输出值。
* The output value X' of the first layer is the input to the next layer.
* 第一层的输出值 X' 是下一层的输入。

![image-20231129000534879](D:\笔记\笔记图片\image-20231129000534879.png)

![image-20231129000651132](D:\笔记\笔记图片\image-20231129000651132.png)

* First of all, we introduce the computation for a single neuron. For instance, consider the first neuron in the first hidden layer.
* 首先，我们介绍单个神经元的计算。例如，考虑第一个隐藏层的第一个神经元。

![image-20231129001549392](D:\笔记\笔记图片\image-20231129001549392.png)

* We start from the first hidden layer. The output of the 3-th neuron in the first layer is
* 我们从第一隐藏层开始。第一层第 3 个神经元的输出为

![image-20231129002048335](D:\笔记\笔记图片\image-20231129002048335.png)

![image-20231129002141982](D:\笔记\笔记图片\image-20231129002141982.png)

* The process of such layer-by-layer calculation to obtain the output of a multilayer perceptron is thus called **forward propagation.**
* 因此，这种逐层计算以获得多层感知器输出的过程被称为**前向传播。**

##### 17.1.3.1 A Running Example

![image-20231129003344268](D:\笔记\笔记图片\image-20231129003344268.png)

![image-20231129003405620](D:\笔记\笔记图片\image-20231129003405620.png)

* 这里需要解释一下ID函数和sigmoid函数
* 在第一层隐藏层中，因为所使用的激活函数是**恒等函数（identity function，通常表示为 *id*）**
* 在第二层隐藏层中，使用的是 **Sigmoid 激活函数**，这是一种常用的非线性激活函数

![image-20231129003414411](D:\笔记\笔记图片\image-20231129003414411.png)

![image-20231129003627641](D:\笔记\笔记图片\image-20231129003627641.png)

* 通过以上计算可以得到各个节点的值，但是注意，第二层的节点的值需要通过sigmoid计算得到X

![image-20231129003821310](D:\笔记\笔记图片\image-20231129003821310.png)

* **Issue: The hidden neurons cannot be trained by making their outputs become closer to the desired values given by the training set.** 
* **问题： 无法通过让隐神经元的输出更接近训练集给出的期望值来训练隐神经元。**



## Lecture 18_Multilayer_Peceptron_1

### 18.1 Gradient Decent and Activation Function Design 梯度修正和激活函数设计

![image-20231129005952810](D:\笔记\笔记图片\image-20231129005952810.png)

* The output error of a multilayer perceptron for the k-th input pattern is a half of the squared error:
* 多层感知器对第 k 个输入模式的输出误差是平方误差的一半

![image-20231129010057432](D:\笔记\笔记图片\image-20231129010057432.png)

* Now we define the performance of multilayer perceptron over a Data set D as a half of the total squared error:

* 现在，我们将多层感知器在数据集 D 上的性能定义为总平方误差的一半：

![image-20231129011113331](D:\笔记\笔记图片\image-20231129011113331.png)

* Now we define the performance of multilayer perceptron over a Data set D as a half of the total squared error:
* 现在，我们将多层感知器在数据集 D 上的性能定义为总平方误差的一半：

![image-20231129011331797](D:\笔记\笔记图片\image-20231129011331797.png)

![image-20231129011646959](D:\笔记\笔记图片\image-20231129011646959.png)

* During the training stage, the input value a to the network are the input vectors of the training set, which are constant parameters for the process. 
* 在训练阶段，网络的输入值 a 是训练集的输入向量，它们是过程的恒定参数。
* Therefore, the MLP error function E is a function of the weights of connections only:
* ![image-20231129011710473](D:\笔记\笔记图片\image-20231129011710473.png)
* 因此，MLP 误差函数 E 只是连接权重的函数：
* The better the MLP performs, the smaller the MLP error function E is.
* MLP 的表现越好，MLP 误差函数 E 就越小。
* Thus MLP learning can be considered as the optimization problem: min wE(w)
* 因此，MLP 学习可视为优化问题： min wE(w)



### 18.2 Gradient Decent 梯度下降

![image-20231129012016382](D:\笔记\笔记图片\image-20231129012016382.png)

* Gradient descent is based on the observation that if the multi-variable function F(x) is defined and differentiable in a neighborhood of a point a, then F(x) decreases fastest if one goes from a in the direction of the negative gradient of F at a, −∇F(a) . It follows that, if
* 梯度下降法的基础是，如果多变量函数 F(x) 在点 a 的邻域内是可定义和可微分的，那么如果从点 a 沿 F 在点 a 的负梯度方向（-∇F(a)）下降，F(x) 下降得最快。由此可见，如果

![image-20231129014559375](D:\笔记\笔记图片\image-20231129014559375.png)

* **<font color=red size>感觉非常像之前高中的求导，目的是寻找最大的值</font>**



![image-20231129015054752](D:\笔记\笔记图片\image-20231129015054752.png)



![image-20231129015020017](D:\笔记\笔记图片\image-20231129015020017.png)

![image-20231129015220388](D:\笔记\笔记图片\image-20231129015220388.png)

* Gradient descent method addresses the issue of how to update weights.
* 梯度下降算法解决了如何更新权重的问题。

![image-20231129015324874](D:\笔记\笔记图片\image-20231129015324874.png)

* One of the most popular techniques is called 
  * **error backpropagation,  （反向传播）**
* where the error of output neurons is propagated back to derive the weight adjustment of a given hidden neuron, based on how much the neuron contributes to the output error.
* 即根据输出神经元对输出误差的贡献程度，将输出神经元的误差反向传播，从而得出给定隐藏神经元的权重调整。
* The backpropagation algorithm updates the weights of connections w computationally efficiently based on the method of gradient descent.
* 反向传播算法基于梯度下降法，以高效的计算方式更新连接权重 w。
* **这里所说的就是通过反向传播来更新hidden layer中的权重。**

![image-20231129020338420](D:\笔记\笔记图片\image-20231129020338420.png)

* Gradient descent method addresses the issue of how to update weights. 
* 梯度下降法解决了如何更新权重的问题。
* The backpropagation algorithm makes the weight updating efficient.
* 反向传播算法使权重更新变得高效。

![image-20231129020551102](D:\笔记\笔记图片\image-20231129020551102.png)



## Lecture21_ Genetic Algorithms

 ### 21.1 Biological Motivation

![image-20231129043542589](D:\笔记\笔记图片\image-20231129043542589.png)

* Species adapt to the environment via **<font color=red>natural selection</font>**.
* 物种通过**自然选择**来适应环境。
* The selection favours those species for survival and further evolution that are best adapted to the environmental condition – **<font color=red>“survival of the fittest”</font>**.
* 选择有利于那些最能适应环境条件的物种生存和进一步进化--**"适者生存"**。
* <font color=red>**Phenotype**</font> is the manner of response and physical embodiment of an individual. There occur small, apparently random and undirected variations between the phenotypes of parents and their offspring.
* **<font color=red>表型</font>**是个体的反应方式和身体体现。亲代和子代的表型之间存在着微小的、明显随机的和非定向的变异。
* These **mutations** prevail through selection, if they prove their worth in the current environment; otherwise they perish.
* 如果这些**变异**在当前环境中证明了它们的价值，它们就会通过选择而获胜；否则，它们就会灭亡。



![image-20231129045600746](D:\笔记\笔记图片\image-20231129045600746.png)

* **<font color=red>Production of offspring</font>** is the basic driving force for selection. 
* **生产后代**是选择的基本动力。
* In a favourable environment, population grows exponentially. This growth is generally limited by **finite resources.** 
* 在有利的环境中，人口呈指数增长。这种增长通常受到**有限资源的限制**。
* When resources are no longer sufficient to support all individuals in a population, **only the fittest, i.e. those most effectively utilizing the resources, survive and produce offspring.** 
* 当资源不再足以支持种群中的所有个体时，**只有那些最适合的个体，即那些最有效地利用资源的个体，才能生存下来并繁衍后代。**
  * **In an unkind environment, organisms in a population are at a selective advantage to utilize resources most effectively.** 
  * **在不友善的环境中，种群中的生物具有选择性优势，能够最有效地利用资源。**

### 21.2 Neo-Darwinism Theory of Evolution (Microscope)

![image-20231129050046861](D:\笔记\笔记图片\image-20231129050046861.png)

* All living organisms consist of **cells**. 
* 所有生物体都由**细胞**组成。
* Each cell in an organism contains the same set of one or more **chromosomes** 
* 生物体中的每个细胞都含有相同的一组或多组**染色体**。
* Chromosomes are strings of **DNA** that serve as a **blueprint** for the organism. 
* 染色体是一串 DNA，是生物体的蓝图。

![image-20231129050510162](D:\笔记\笔记图片\image-20231129050510162.png)

![image-20231129050529652](D:\笔记\笔记图片\image-20231129050529652.png)

#### 21.2.1 DNA Structure DNA结构

![image-20231129050620438](D:\笔记\笔记图片\image-20231129050620438.png)

* A chromosome can be conceptually divided into genes --- **Gene is a functional block of DNA coding a particular protein.** 
* 从概念上讲，染色体可分为基因--基因是 DNA 的一个功能块，**编码一种特定的蛋白质**

#### 21.2.2 DNA Code DNA编码

![image-20231129050813943](D:\笔记\笔记图片\image-20231129050813943.png)

* DNA molecule consists of 
  * two ribbons of phosphate-sugar chains, and 
  * 两条磷酸-糖链，以及 
  * the horizontal rods of the pairs of nitrogenous bases holding the chains together 
  * 将糖链固定在一起的一对含氮碱基的水平杆
* **There exist only four different nitrogenous bases in DNA: <font color=red size=5>adenine, guanine, thymine, cytosine.</font>** 
* **DNA 中只有四种不同的含氮碱基：腺嘌呤、鸟嘌呤、胸腺嘧啶和胞嘧啶。**

![image-20231129051410751](D:\笔记\笔记图片\image-20231129051410751.png)

* The two chains held together by **hydrogen bonds(氢键)** formed between **pairs of bases 碱基对之间的序列** . 
* 通过碱基对之间形成的氢键将两条链固定在一起。
* Pairing is highly specific. It is always that 
* 配对具有高度特异性。总是这样 
  * Adenine pairs with Thymine, A = T; 
  * 腺嘌呤与胸腺嘧啶配对，A = T； 
  * Guanine pairs with Cytosine, G = C. 
  * 鸟嘌呤与胞嘧啶配对，G = C。
* **<font color=red>The precise sequence of bases carries the genetic information.</font>** 
* **<font color=red>碱基的精确序列携带着遗传信息。</font>**

![image-20231129052106058](D:\笔记\笔记图片\image-20231129052106058.png)

* The precise sequence of bases carries the genetic information. 
* 精确的碱基序列携带遗传信息。
* Gene is a functional block of DNA coding a particular protein. 
* 基因是 DNA 的一个功能块，编码一种特定的蛋白质。
* **Problem: there are just 4 letters in the DNA alphabet to code, but 20 amino acids氨基酸 found in proteins.**
* **问题：DNA 字母表中只有 4 个字母可以编码，但蛋白质中却有 20 种氨基酸。**

![image-20231129052540119](D:\笔记\笔记图片\image-20231129052540119.png)

* 首先，肯定不可以一一对应，因为数量上不够

![image-20231129052628237](D:\笔记\笔记图片\image-20231129052628237.png)

* There can not be a two nitrogenous bases to one amino acid match either, as it gives just 4^2 = 16 different pairs of nucleotides < 20
* 也不可能存在两个含氮碱基对一个氨基酸的匹配，因为这样就只有 4^2 = 16 对不同的核苷酸 < 20

![image-20231129053836846](D:\笔记\笔记图片\image-20231129053836846.png)

* **Nitrogenous bases(含氮碱基对)** in combination as a triplet are required to code for each amino acid, as this gives 4^3 = 64 possible combinations.
* 每个氨基酸都需要含氮碱基以三联体的形式组合编码，这样就有 4^3 = 64 种可能的组合。

![image-20231129054611269](D:\笔记\笔记图片\image-20231129054611269.png)

* The genetic code is **<font color=red>universal</font>**, as the codons that code for amino acids are the same in bacteria, plants and animals.
* 遗传密码是**通用**的，因为编码氨基酸的密码子在细菌、植物和动物中都是相同的。



##### 21.2.2.1 DNA Code Crossing-Over

![image-20231129054905132](D:\笔记\笔记图片\image-20231129054905132.png)

* **Organisms with unpaired sets of chromosomes are called haploid.** 
* **染色体不成对的生物称为单倍体。**
* **Organisms, whose chromosomes are arranged in pairs are called diploid.** Most sexually reproducing organisms are diploid.
* **染色体成对排列的生物称为二倍体。**大多数有性生殖的生物都是二倍体。 
* During sexual reproduction, **<font color=red>crossing-over</font>** or **<font color=red>recombination</font>** of genes in parent chromosomes occurs. In each parent cell, a pair of chromosomes first doubles, then the chromosomes exchange genes, and finally produce four gametes, single chromosomes, ready to couple with the other parent gametes to form a new diploid cell.
* 在有性生殖过程中，亲本染色体上的基因会发生**交叉或重组**。在每个亲本细胞中，一对染色体首先加倍，然后染色体交换基因，最后产生四个配子（单条染色体），准备与其他亲本配子结合形成新的二倍体细胞。



##### 21.2.2.2 DNA Code Mutations

![image-20231129060500575](D:\笔记\笔记图片\image-20231129060500575.png)

* **<font color=red>Mutation is a random change of a “letter”, single nucleotide in a chromosome.</font>** 
* **<font color=red>突变是染色体中一个 "字母"（单个核苷酸）的随机变化。</font>**
* Mutations usually result from copying errors in parent chromosomes and then are reproduced in offspring.
* 突变通常是由亲代染色体的复制错误引起的，然后在子代中复制。

##### 21.2.2.3 Neo-Darwinism Theory of Evolution

![image-20231129060659764](D:\笔记\笔记图片\image-20231129060659764.png)

* **Gene is a functional block of DNA coding a particular protein**, see “gene encodes a trait, e.g. eye colour”. 
* **基因是编码特定蛋白质的 DNA 功能块**，见 "基因编码性状，如眼睛颜色"。
* **Different possible settings for a trait**, e.g. blue, brown, black eye colour, are called alleles. 
* **一种性状的不同可能设置**，如蓝色、棕色、黑色的眼睛颜色，称为等位基因。
* Each gene is located at a particular **locus (position)** on the chromosome. 
* 每个基因都位于**染色体上的一个特定位点**（位置）。

![image-20231129061400113](D:\笔记\笔记图片\image-20231129061400113.png)

* **Gene is a functional block of DNA coding a particular protein**, see “gene encodes a trait, e.g. eye colour”. 
* **基因是编码特定蛋白质的 DNA 功能块**，见 "基因编码性状，如眼睛颜色"。
* **<font color=red>The complete collection of all genetic material,</font>** that is all chromosomes taken together, is called the organism’s **<font color=red>genome or genotype</font>**.
* **所有遗传物质的完整集合**，即所有染色体加在一起，称为生物体的**基因组或基因型。**

![image-20231129061648109](D:\笔记\笔记图片\image-20231129061648109.png)

* **<font color=red>Genes are transfer units of heredity.</font>** Genes are occasionally changed by mutations. 
* **基因是遗传的传递单位。**基因偶尔会因突变而改变。
* **Phenotype** expresses complex interaction within the genotype as well as its interaction with environment. 
* **表型**表达了基因型内部复杂的相互作用以及与环境的相互作用。

* Modern biochemistry and genetics explain microscopic mechanisms of heredity. 
* 现代生物化学和遗传学解释了遗传的微观机制。

![image-20231129062317397](D:\笔记\笔记图片\image-20231129062317397.png)

* **种群是不断进化的单位。**种群作为一个单位，限定了一个共同的基因库 包括所有个体的基因型。

![image-20231129062422939](D:\笔记\笔记图片\image-20231129062422939.png)

* **<font color=red size=5>Individual fitness</font>** is measured indirectly as the individual growth rate in comparison to others. 
* **个体适宜性**是通过与其他人相比的个体增长率来间接衡量的。
* **<font color=red>The fitness is the individual propensity to survive and reproduce in a particular environment. </font>**
* 适应性是个体在特定环境中生存和繁殖的倾向。
* Thus, **Natural Selection** according to the individual fitness 
* 因此，根据个体适宜性进行的**自然选择** 
  * is NOT an active driving force, 
  * 不是一种主动的驱动力
  * is differential survival and reproduction within a population.
  * 是种群内部生存和繁殖的差异
* 

![image-20231129070302988](D:\笔记\笔记图片\image-20231129070302988.png)

## Lecture22_Comp_appeal

* 紧接着Lecture21

![image-20231129070448112](D:\笔记\笔记图片\image-20231129070448112.png)

#### 22.1 Natural Evolution. Computational Appeal? **Natural Evolution. Computational Appeal?**

![image-20231129070549895](D:\笔记\笔记图片\image-20231129070549895.png)

* 基因如何映射到表型，然后再反应到适应性上



* map a given genotype into the corresponding phenotype and 
* 将给定的基因型映射到相应的表型中，以及 
* map the phenotype into the individual fitness to survive and reproduce ? 
* 将表型映射到个体的生存和繁殖能力？

![image-20231129071349474](D:\笔记\笔记图片\image-20231129071349474.png)

![image-20231129071533387](D:\笔记\笔记图片\image-20231129071533387.png)

![image-20231129071823271](D:\笔记\笔记图片\image-20231129071823271.png)

![image-20231129071836868](D:\笔记\笔记图片\image-20231129071836868.png)





##### 22.1.1 Parallelism 并行性

![image-20231129071636484](D:\笔记\笔记图片\image-20231129071636484.png)

* **<font color=red size=5>Parallelism 并行性</font>**
  * **Every individual in the population is tested independently in parallel with the others, and that speeds up evolution of the population.**
  * **种群中的每个个体都要与其他个体同时接受独立测试，这就加快了种群的进化速度。**



##### 22.1.2 Adaptation to a changing environment. 适应变化的环境

![image-20231129072121287](D:\笔记\笔记图片\image-20231129072121287.png)

* **<font color=red size=5>Adaptation to a changing environment.  适应不断变化的环境</font>**
  * **Due to the natural selection, only those individuals best fitted for the current environment do survive. The selection results in the population as a whole best adapted to the environment.**
  * **由于自然选择的作用，只有那些最适合当前环境的个体才能生存下来。选择的结果是整个种群最适应环境。**



##### 22.1.3 Optimization 优化

![image-20231129072350203](D:\笔记\笔记图片\image-20231129072350203.png)

* **<font color=red size=5>Optimization 优化</font>**
*  Due to the natural selection, only individuals best fitted or “optimal” for the current environment do survive and reproduce. Thus, the selection also performs optimization on an individual level. 
* 在自然选择的作用下，只有最适合或 "最佳 "当前环境的个体才能生存和繁衍。因此，选择也是在个体层面上进行优化。





![image-20231129072533344](D:\笔记\笔记图片\image-20231129072533344.png)

* The listed features of the natural selection are very attractive for many problems in computer science.
* 对于计算机科学中的许多问题来说，自然选择的上述特点非常具有吸引力。
* As these parallelism, adaptation, and optimisation are achieved in nature by very simple manipulation of individual DNA sequences, it is tempting to use the algorithm for non-bio problem solving in engineering, computer science, etc.
* 由于这些并行性、适应性和优化性在自然界中是通过对单个 DNA 序列进行非常简单的操作来实现的，因此将该算法用于解决工程、计算机科学等领域的非生物问题是很有吸引力的。



### 22.2 Genetic Algorithms. Historical Introduction 遗传算法的历史简介

* **By 1950s, it became clear that** 
  * **if a solution of a computational problem might be formulated, i.e., coded, in a form of string of “characters”,** 
  * **如果一个计算问题的解决方案可以用 "字符 "串的形式来表述，即编码**
  * **then the optimal solution to the problem might be searched for using the natural selection technique among a “population”, i.e., set of candidate solutions.**
  * **那么就可以利用自然选择技术，在 "种群"（即一组候选解决方案）中寻找问题的最佳解决方案。**

![image-20231129073449846](D:\笔记\笔记图片\image-20231129073449846.png)

* 1950s-1960s -- several computer scientists independently studied evolutionary systems with the idea to use the algorithm to solve optimisation problems in engineering.
* 20 世纪 50 年代至 60 年代 -- 几位计算机科学家独立研究了进化系统，并萌生了使用该算法解决工程优化问题的想法。



![image-20231129073433085](D:\笔记\笔记图片\image-20231129073433085.png)

![image-20231129073635901](D:\笔记\笔记图片\image-20231129073635901.png)

![image-20231129073717202](D:\笔记\笔记图片\image-20231129073717202.png)

![image-20231129073736544](D:\笔记\笔记图片\image-20231129073736544.png)

* In contrast with Nature, 
  * **there is no universal code in GAs,** 
  * **全球定位系统中没有通用的编码**
  * **every coding is problem dependent.** 
  * **每个编码都取决于问题**
* The art of coding, though left beyond the scope, is very important in Genetic Algorithms, as from the very beginning the approach depends on whether the problem can be coded as a string of characters at all. 
* 编码艺术虽然不在本文讨论范围之内，但在遗传算法中却非常重要，因为从一开始，方法就取决于问题是否能被编码成一串字符。
* The above implies serious restrictions on the class of problems capable of solving by GAs. 
* 上述情况严重限制了全球定位系统所能解决的问题类别

## Lecture_23_Terminology

* 紧接着上一课的内容

### 23.1 GAs by John Holland: Chromosomes 约翰-霍兰的基因算法: 染色体

* **Definition: Genetic Algorithm’s Chromosome is <font color=red>a string of characters</font>**
* **定义 遗传算法的染色体是一串字符**
  * Often the GA chromosome is defined as a
  * 通常，GA 染色体被定义为 
    * Fixed length binary string,
    * **<font color=red>固定长度的二进制字符串</font>**



* 解释一下关于基因算法
* ![image-20231130053906363](D:\笔记\笔记图片\image-20231130053906363.png)

![image-20231130051518727](D:\笔记\笔记图片\image-20231130051518727.png)

* The same as nature blindly operates on real chromosomes and does not know or care what information is actually coded in the chromosomes, Holland had left behind the question of what particular information and in what way was coded in the strings of the Genetic Algorithms chromosomes
* 就像大自然盲目地对真正的染色体进行操作，不知道也不关心染色体中到底编码了什么信息一样，霍兰也抛开了遗传算法染色体串中到底编码了什么特定信息以及以何种方式编码的问题。

![image-20231130054040436](D:\笔记\笔记图片\image-20231130054040436.png)

* Haploid organisms, i.e., the organisms with on-paired chromosomes are considered in the Genetic Algorithms for some operators, e.g., crossover.
* 遗传算法中的某些运算符（如交叉）会考虑单倍体生物，即染色体成对的生物。

![image-20231130054048916](D:\笔记\笔记图片\image-20231130054048916.png)

* 遗传因子染色体与基因型重合，即基因型由单条染色体组成。

![image-20231130054309592](D:\笔记\笔记图片\image-20231130054309592.png)

* For simplicity, there is no phenotype concept in Genetic Algorithms either, and therefore we do not distinguish the following concepts:
  GAs chromosome = GAs genotype = GAs organism
* 为简单起见，遗传算法中也没有表型概念。因此我们不区分以下概念：
  **遗传算法染色体 = 遗传算法基因型 = 遗传算法生物体**

![image-20231130054448487](D:\笔记\笔记图片\image-20231130054448487.png)

* It is also called population of candidate solutions.
* 它也被称为候选方案群。

![image-20231130060319500](D:\笔记\笔记图片\image-20231130060319500.png)

* **In a GAs chromosome, a character represents a gene.**
* **在基因组染色体中，一个字符代表一个基因。**
* **Possible settings for a gene are called <font color=red>alleles</font>**, e.g. in the example above the alleles are 0s and 1s, and if a gene codes a trait then an allele is the trait instance. For binary chromosomes, the alleles “alphabet” consists of just two characters, 0 and 1. There might be bigger “alphabets” to represent bigger number of alleles.
* **基因的可能设置称为等位基因**，例如，在上面的例子中，等位基因是 0 和 1，如果一个基因编码一个性状，那么等位基因就是该性状的实例。对于二进制染色体，等位基因的 "字母表 "只有 0 和 1 两个字符。
* **Position of a gene in the string is called <font color=red>locus of the gene</font>.**
* **基因在字符串中的位置称为基因座。**



### 23.2 GAs by John Holland: Crossover 交叉

![image-20231130060846778](D:\笔记\笔记图片\image-20231130060846778.png)

* In nature, crossover occurs when two parents exchange parts of their corresponding chromosomes
* 在自然界中，当两个亲本交换其相应染色体的一部分时，就会发生交叉现象
* In a genetic algorithm, crossover recombines parts of two parent chromosomes to make two “children”.
* 在遗传算法中，交叉将两个亲代染色体的一部分重组为两个 "子代"。

![image-20231130070032927](D:\笔记\笔记图片\image-20231130070032927.png)

* **The crossover cutting point is chosen randomly.** 
* **交叉切点是随机选择的。**
* **<font color=red size=5>One-point crossover is considered most often.</font>**
* **最常考虑单点交叉。**

### 23.3 GAs by John Holland: Mutation

![image-20231130070248487](D:\笔记\笔记图片\image-20231130070248487.png)

* **<font color=red size=5>Mutation is random of allele of gene at randomly chosen location</font>**
* **突变是随机选择基因等位基因的位置**

![image-20231130070448967](D:\笔记\笔记图片\image-20231130070448967.png)

* **对于二进制染色体来说，这意味着在随机选择的位点上翻转一个比特，例如**
* **For binary chromosomes that means a flip of a bit at random chosen locus, e.g.,**

![image-20231130071124277](D:\笔记\笔记图片\image-20231130071124277.png)

* **For chromosomes with larger alphabet, mutation means replacement of a character at randomly chosen location with randomly chosen new character.** 
* **对于字母较大的染色体，突变意味着用随机选择的新字符替换随机选择位置上的字符。**



### 23.4 GAs by John Holland: Inversion and Translocation 反转和移位

![image-20231130071325249](D:\笔记\笔记图片\image-20231130071325249.png)

* **<font size=5>Inversion</font>** is a mutation when part of a chromosome is cut out, rotates by 180° and then fitted back into the same position
* **<font size=5>倒位</font>**是一种突变，即染色体的一部分被切掉，旋转 180°，然后装回原来的位置。
* ![image-20231130071354734](D:\笔记\笔记图片\image-20231130071354734.png)
* **<font size=5>Translocation</font>** is a mutation when part of a chromosome is cut out and moved to a different location in the chromosome:
* **<font size=5>移位</font>**是指染色体的一部分被切掉并移到染色体的另一个位置的突变：
* ![image-20231130071414187](D:\笔记\笔记图片\image-20231130071414187.png)



### 23.5 GAs by John Holland: Fitness Function 适应度函数

![image-20231130071751005](D:\笔记\笔记图片\image-20231130071751005.png)

* **To evaluate a chromosome fitness**, that is how good the candidate solution solves the problem, **a Genetic Algorithm uses fitness function.** 
* **为了评估染色体的适应度**，即候选方案解决问题的好坏，**遗传算法使用了适应度函数**。
* The fitness function
  *  Takes a chromosome as an input; 
  * 将染色体作为输入
  * Produces its quantitative fitness evaluation as an output.
  * 将染色体的定量适配性评价作为输出

![image-20231130072141842](D:\笔记\笔记图片\image-20231130072141842.png)

![image-20231130072811565](D:\笔记\笔记图片\image-20231130072811565.png)

* The same as that a particular code to be used for coding a problem solution in a form of GAs chromosomes depends on the problem itself, a particular form of the fitness function also depends on the problem to be solved. 
* 就像在遗传算法染色体形式中编码问题解决方案所使用的特定代码取决于问题本身一样，特定形式的适应度函数也取决于要解决的问题。

![image-20231130072741847](D:\笔记\笔记图片\image-20231130072741847.png)



![image-20231130073014785](D:\笔记\笔记图片\image-20231130073014785.png)

* Two important requirements: 
  * Should **correlate closely with the designer's goal** 
  * 应与**设计者的目标密切相关**
  * Should be **computationally efficient**
  * 应具**有计算效率**

* Precise fitness function but computation is time consuming
* 适合度函数精确，但计算耗时
* Approximate fitness function but very efficient 
* **近似拟合函数，但非常高效（We Chose this way）**

![image-20231130073225398](D:\笔记\笔记图片\image-20231130073225398.png)

* Specifically, we may use approximate fitness function when:
* 具体来说，我们可以在以下情况下使用近似拟合函数
  * Precise fitness function is extremely time consuming;
  * 精确拟合函数非常耗时；
  * Precise fitness function is missing or hardly obtained;
  * 精确拟合函数缺失或难以获得；
  * Precise fitness function model itself contains uncertainties.
  * 精确拟合函数模型本身包含不确定性。

### 23.6 GAs by John Holland: Evolving unit 演化单位

![image-20231130073709107](D:\笔记\笔记图片\image-20231130073709107.png)

* The same as in nature, in **GAs Population** of chromosomes is **the evolving unit**. 
* 自然界相同，在遗传优化中，染色体群是进化单位。
* The GAs population evolves from **one generation** of chromosomes to the next generation and so on.
* 遗传算法的群体从一代染色体进化到下一代染色体，以此类推。

### 23.6 GAs by John Holland: Selection Operator 选择操作

![image-20231130075110302](D:\笔记\笔记图片\image-20231130075110302.png)

*  To simulate natural evolution of population of chromosomes, there must be **a rule how to choose which chromosome is more likely to produce offspring for the next generation.** 
* 要模拟染色体群体的自然进化，**必须有一个规则来选择哪条染色体更有可能为下一代产生后代。**
* We shall call that rule **<font color=red>a selection operator.</font>** 
*  我们称这种规则为**选择算子。**
* Usually, a selection operator is defined in a way that better fitted chromosome is selected for reproduction more often and therefore will produce more offspring.
* 通常，选择算子的定义是，更适合的染色体被更频繁地选择用于繁殖，因此会产生更多的后代。



### 23.7 GAs by John Holland: Search Space. 搜索空间

![image-20231130075400661](D:\笔记\笔记图片\image-20231130075400661.png)

* 由于遗传算法的目的是寻找问题的最佳解决方案，因此自然要为算法引入 "搜索空间"（Search Space）的概念。
* **定义：**
  **一个问题所有可能解决方案的集合称为遗传算法搜索空间。**
* 因此，我们要在可能解决方案的搜索空间中寻找问题的最佳解决方案。问题的最佳解决方案。

### 23.8 GAs by John Holland: Fitness Landscape 和适度图

![image-20231130075455752](D:\笔记\笔记图片\image-20231130075455752.png)

* A fitness landscape is a representation of all possible solutions along with their fitness. 
* 适合度景观是所有可能解决方案及其适合度的表示。
* The candidate solutions are represented by points in the coordinate plane, i.e. the search space, and corresponding fitness is measured along an additional dimension.
* 候选方案由坐标平面（即搜索空间）上的点表示，相应的适配度则沿着额外的维度进行测量。

![image-20231130075655203](D:\笔记\笔记图片\image-20231130075655203.png)

- 适合度景观是所有可能解决方案及其适合度的表示。
- 这里会有 "山峰"、"丘陵 "和 "山谷"，就像自然景观一样。景观。
- **<font size=5>进化使种群 向适合度的峰顶移动 景观。</font>**

## Lecture24_Basic_GAs

### 24.1 Basic Genetic Algorithms

![image-20231130214203640](D:\笔记\笔记图片\image-20231130214203640.png)

* a **“population”** of binary strings which he called **“chromosomes”**.
* 他称之为 "染色体 "的二进制字符串 "种群"。
* The **“population”** evolves using kind of **“natural selection”** together with the genetics- inspired operators of **crossover, mutation, and inversion**.
* 种群 "通过 "**自然选择** "与遗传学启发的**交叉、突变和反转**运算符一起进化。
* **Bits in a “chromosome” represent genes, and each “gene” is an instance of a particular “allele”, 0 or 1.**
* 染色体 "中的比特代表基因，每个 "基因 "都是特定 "等位基因"（0 或 1）的实例。
* The **selection operator** chooses those chromosomes in the population that will be allowed to reproduce, and on average the fitter chromosomes produce more offspring than the less fit ones.
* **选择算子**选择种群中可以繁殖的染色体，平均而言，适合的染色体比不适合的染色体产生更多的后代。
* **Crossover** exchange subparts of two chromosomes
* **交叉交换**两个染色体的子部分
* **Mutation** randomly changes the allele values at some locations in the chromosome.
* **突变**随机改变染色体上某些位置的等位基因值。
* **Inversion** reverses the order of a contiguous section of the chromosome rearranging the genes order.
* **倒置**将染色体上连续部分的顺序颠倒过来，重新排列基因顺序。



#### 24.1.1 Basic Structure of a Genetic Algorithm

![image-20231130214911289](D:\笔记\笔记图片\image-20231130214911289.png)

1. Randomly generate initial population of n bit strings (“chromosomes”). 

2. 随机生成由 n 个比特串（"染色体"）组成的初始群体。

3. **<font color=red size=5>Evaluate</font>** the fitness of each string in the population. 

4. 评估种群中每个字符串的适合度。

5. Repeat the following steps until next generation of n individual produced. 

   a. **<font color=red size=5>Select</font>** pair of parent chromosomes from current population according to their fitness, i.e. chromosomes with higher fitness are selected more often. 

   根据适配度从当前种群中选择一对父染色体，即适配度越高的染色体被选择的次数越多。

   b. Apply **<font color=red size=5>crossover</font>** (with probability). 

    应用交叉（概率）。

   c. Apply **<font color=red size=5>mutation</font>** (with probability of occurrence) . 

   应用突变概率

6. a. 根据适配度从当前种群中选择一对父染色体，即适配度越高的染色体被选择的次数越多。 b. 应用交叉（概率）。

7. Apply generational **<font color=red size=5>replacement</font>**. 

8. 应用世代**替换** 

9. Go to 2 or terminate if termination condition is met.

10. 如果满足终止条件，则转到 2 或终止。

##### 24.1.1.1 Example Implementation of a GA

![image-20231130215651741](D:\笔记\笔记图片\image-20231130215651741.png)

* Let length of each chromosome (binary string) l = 8. And the number of chromosomes in the population (population size) n = 4. 
* 假设每条染色体（二进制字符串）的长度为 l = 8，种群中染色体的数量（种群大小）为 n = 4。
* Fitness function f(x) is equal to **the number of ones in the bit string x.** 
* 适合度函数 f(x) **等于比特串 x 中的 1 的个数。**
* Selection operator. Fitness-proportionate selection, that is, the number of times an individual expected to be selected is equal to its fitness fi divided by the average fitness of the population ˉ*f*ˉ(平均值)(also known as **Roulette Wheel Selection**):
* 选择运算符。适合度比例选择，即个体被选中的次数等于其适合度 fi 除以种群的平均适合度 f(平均值)（又称**轮盘选择**）：

![image-20231130220457813](D:\笔记\笔记图片\image-20231130220457813.png)

###### 24.1.1.1.1 The First Generation

![image-20231130220615737](D:\笔记\笔记图片\image-20231130220615737.png)

![image-20231130220630421](D:\笔记\笔记图片\image-20231130220630421.png)

![image-20231130220716036](D:\笔记\笔记图片\image-20231130220716036.png)

![image-20231130221337390](D:\笔记\笔记图片\image-20231130221337390.png)

* chromosome number 1 shall be selected one time, 
* 1 号染色体应选择一次
* chromosome number 2 shall be selected two times, 
* 2号染色体应选择两次
* chromosome number 3 shall not be selected at all, 
* 第 3 号染色体根本不会被选中
* chromosome number 4 shall be selected one time. 
* 第 4 号染色体应选择一次

* ![image-20231130221359023](D:\笔记\笔记图片\image-20231130221359023.png)

![image-20231130221500236](D:\笔记\笔记图片\image-20231130221500236.png)

* **<font color=red>选择N最高的作为父本进行交叉</font>**

![image-20231130222115384](D:\笔记\笔记图片\image-20231130222115384.png)

* **Use a generator producing random numbers in the range between 0 and 1 to get a random number r for each pair of parental chromosomes.** 
* **使用随机数发生器，在 0 和 1 之间产生随机数，为每对亲本染色体获取随机数 r。**
* **If the random number r produced by the generator for the pair of “parents” is less or equal to the crossover probability pc, then apply crossover to the “parents” at randomly chosen locus, otherwise the parents do not crossover.** 
*  **如果生成器为一对 "亲本 "产生的随机数 r 小于或等于交叉概率 pc，则在随机选择的位点上对 "亲本 "进行交叉，否则亲本不进行交叉。**
* **If a pair of parents do not undergo crossover, their offspring are their identical copies**
* **如果一对 "亲本 "不进行交叉，那么它们的后代就是完全相同的拷贝**



![image-20231201000630789](D:\笔记\笔记图片\image-20231201000630789.png)

![image-20231201000723629](D:\笔记\笔记图片\image-20231201000723629.png)

* Use a generator producing random numbers in the range between 0 and 1 to get a random number r for each new chromosome. 
* 使用随机数发生器，在 0 和 1 之间产生随机数，为每条新染色体获取一个随机数 r。
* If the random number r is less or equal to the mutation probability pm(, apply mutation to the chromosome, i.e., flip a bit at randomly chosen locus.
* 如果随机数 r 小于或等于突变概率 pm(，则对染色体进行突变，即在随机选择的位点上翻转一位。

![image-20231201001053466](D:\笔记\笔记图片\image-20231201001053466.png)

![image-20231201001208119](D:\笔记\笔记图片\image-20231201001208119.png)

![image-20231201001718094](D:\笔记\笔记图片\image-20231201001718094.png)



###### 24.1.1.1.2 The Second Generation

**<font size=5>第二个例子</font>**

![image-20231201002511741](D:\笔记\笔记图片\image-20231201002511741.png)

![image-20231201002521589](D:\笔记\笔记图片\image-20231201002521589.png)

![image-20231201002650559](D:\笔记\笔记图片\image-20231201002650559.png)

![image-20231201002840659](D:\笔记\笔记图片\image-20231201002840659.png)



![image-20231201002851329](D:\笔记\笔记图片\image-20231201002851329.png)

![image-20231201002859929](D:\笔记\笔记图片\image-20231201002859929.png)

![image-20231201002911086](D:\笔记\笔记图片\image-20231201002911086.png)

![image-20231201002959902](D:\笔记\笔记图片\image-20231201002959902.png)

![image-20231201003013929](D:\笔记\笔记图片\image-20231201003013929.png)

![image-20231201003032901](D:\笔记\笔记图片\image-20231201003032901.png)

###### 24.1.1.1.3 The Third Generation

<font size=5>第三个例子</font>

![image-20231201004326283](D:\笔记\笔记图片\image-20231201004326283.png)

![image-20231201004410954](D:\笔记\笔记图片\image-20231201004410954.png)

![image-20231201004427316](D:\笔记\笔记图片\image-20231201004427316.png)

![image-20231201004451421](D:\笔记\笔记图片\image-20231201004451421.png)

![image-20231201004502347](D:\笔记\笔记图片\image-20231201004502347.png)

![image-20231201004549032](D:\笔记\笔记图片\image-20231201004549032.png)

![image-20231201004612330](D:\笔记\笔记图片\image-20231201004612330.png)

![image-20231201004912704](D:\笔记\笔记图片\image-20231201004912704.png)

###### 24.1.1.1.4 Evaluate The Fitness

![image-20231201005007720](D:\笔记\笔记图片\image-20231201005007720.png)

![image-20231201005015953](D:\笔记\笔记图片\image-20231201005015953.png)

* **<font color=red>The average fitness in the population of possible solutions increases with every generation. </font>**
* **可能的解决方案群体的平均适合度每一代都在增加**。

![image-20231201005023448](D:\笔记\笔记图片\image-20231201005023448.png)

## Lecture25_Schema_preliminary

![image-20231201012202852](D:\笔记\笔记图片\image-20231201012202852.png)

![image-20231201012303466](D:\笔记\笔记图片\image-20231201012303466.png)

![image-20231201012338912](D:\笔记\笔记图片\image-20231201012338912.png)



![image-20231201012352461](D:\笔记\笔记图片\image-20231201012352461.png)

![image-20231201012403620](D:\笔记\笔记图片\image-20231201012403620.png)

### 25.1 Why do GAs work?

![image-20231201012530542](D:\笔记\笔记图片\image-20231201012530542.png)

* Observation 1: **similar “looking” chromosomes do have similar fitness values.**
* 观察结果 1：**"看起来 "相似的染色体确实具有相似的适应度值。**
* Thus, we can obtain an almost optimal chromosome by searching for a chromosome that “looks” similar to the optimal solution;
* 因此，我们可以通过搜索 "看起来 "与最优解相似的染色体，得到一个几乎最优的染色体；
* Observation 2: A chromosome can be described by a set of “substrings”. Thus, **<font color=red>Similar “looking” chromosomes</font> ⟺ <font color=red>Their “substrings” are similar</font>**
* 观察结果 2：染色体可以用一组 "子串 "来描述。因此，**"看起来 "相似的染色体 ⟺ 它们的 "子串 "相似**

#### 25.1.1 Observation1

![image-20231201013005249](D:\笔记\笔记图片\image-20231201013005249.png)

![image-20231201013120846](D:\笔记\笔记图片\image-20231201013120846.png)

*  similar “looking” chromosomes do have similar fitness values, and therefore are taken for reproduction equally often. 
* 看起来 "相似 "的染色体确实具有相似的适应度值，因此被用于繁殖的次数也相同。

![image-20231201013205403](D:\笔记\笔记图片\image-20231201013205403.png)

* Observation 1 leads to a fact: 
* 观察结果 1 揭示了一个事实
  * **<font color=red>Similarities among highly fit strings guide the search. </font>**
  * **<font color=red>高度匹配的字符串之间的相似性会引导搜索。</font>**
* Combining with Observation 2 (**Similar chromosomes ⟺ Similar Substrings**), we focus on the similar “substrings” of chromosomes.
* 结合观察结果 2（相似的染色体 ⟺ 相似的子串），我们将重点放在染色体的相似 "子串 "上。

#### 25.1.2 Similarity Template = Schema 相似性模板 = 模式

![image-20231201014152993](D:\笔记\笔记图片\image-20231201014152993.png)

* Holland introduced a 
* 荷兰引入了一个 
  * **similarity template = schema = building block** 
  * **相似性模板 = 模式 = 构建模块** 
* **to describe subset of strings with similarities at certain positions.** 
* **来描述在某些位置上具有相似性的字符串子集。**

![image-20231201014451035](D:\笔记\笔记图片\image-20231201014451035.png)

* **A schema is a similarity template describing **
* **模式是一种相似性模板**
* **<font color=red size=5>a subset of strings with similarities at certain string positions.</font>**
* **用于描述在特定字符串位置上具有相似性的字符串子集。**
*  **Other name for a schema is a <font color=red>building block</font> of a chromosome.**
* **模式的另一个名称是染色体的构件。**



![image-20231201015322323](D:\笔记\笔记图片\image-20231201015322323.png)

* To describe building blocks of binary chromosomes, the following three letter alphabet is used.
* 为了描述二进制染色体的构建模块，使用了以下三个字母的字母表。
* ![image-20231201015525809](D:\笔记\笔记图片\image-20231201015525809.png)
* Here ∗ is a wildcard symbol, i.e., is a kind of **placeholder**, which can be interpreted as a number of literal characters.
* 这里的 ∗ 是一个通配符号，即一种**占位符**，可以解释为多个文字字符。
* ![image-20231201015534162](D:\笔记\笔记图片\image-20231201015534162.png)
* Example: 111**0 is a schema of the chromosome 111100
* 例如：111**0 是染色体 111100 的模式

![image-20231201015730102](D:\笔记\笔记图片\image-20231201015730102.png)

* Example: 111**0 is a schema of the chromosome 111100 
* 例如：111**0 是染色体 111100 的模式 
* The meaning of the schema is that it works a **pattern matching device:** 
* 模式的意义在于它是一种**模式匹配装置**： 
  * **a schema matches a particular string ⟺ at every location in the schema a 1 matches 1 in the string, a 0 matches a 0, or a * matches either.** 
  * **模式匹配特定的字符串 ⟺ 在模式中的每个位置，1 与字符串中的 1 匹配，0 与字符串中的 0 匹配，或者 * 与字符串中的任一个匹配。**

![image-20231201023238433](D:\笔记\笔记图片\image-20231201023238433.png)

![image-20231201023328054](D:\笔记\笔记图片\image-20231201023328054.png)

* To match a particular chromosome of a fixed length the schema must 
* 要与固定长度的特定染色体匹配，模式必须 
  * a) be of the same length, 
  * 长度相同
  * b) have either 
    * the same defining symbol as the chromosome does or 
    * 与染色体的定义符号相同，或者
    * an “*“ – placeholder symbol - at any particular locus
    * 在任何特定基因座上有一个 "*"--占位符

![image-20231201023356007](D:\笔记\笔记图片\image-20231201023356007.png)

* Thus, for each of the k placeholder positions, the chromosome that can be matched by the schema can have a 1 or a 0. So there will be 2^k chromosomes.
* 因此，对于 k 个占位符位置中的每个位置，模式可匹配的染色体可以是 1 或 0。



![image-20231201031349842](D:\笔记\笔记图片\image-20231201031349842.png)

![image-20231201031601104](D:\笔记\笔记图片\image-20231201031601104.png)

![image-20231201031629617](D:\笔记\笔记图片\image-20231201031629617.png)

* **How many building blocks are there in a particular chromosome of a fixed length l?** 
* **固定长度为 l 的特定染色体中有多少构件？**
* To match a particular chromosome of a fixed length the schema must 
* 要与固定长度的特定染色体相匹配，模式必须 
  * a) be of the same length, 
  * 长度相同
  * b) have either 
    * the same symbol as the chromosome does or 
    * 与染色体符号相同，或者 
    * an “*“ – placeholder symbol - at any particular locus
    * 在任何特定基因座上有一个 "*"--**占位符**



* Thus, in a binary chromosome of a length l there are 2^l building blocks, as a symbol at a particular locus in the chromosome must correspond to the same or the placeholder symbol in the corresponding locus in the schema. 
* 因此，在长度为 l 的二进制染色体中，有 2^l 个构建模块，因为染色体中特定位点上的符号必须与模式中相应位点上的相同或占位符号相对应。

##### 25.1.2.1 Order

![image-20231201032007881](D:\笔记\笔记图片\image-20231201032007881.png)

* **<font color=red>The Order of a schema H is represented as O(H) , denoting the number of defining symbols (non-* symbols) it contains.</font>**
* **模式 H 的顺序用 O(H)表示，表示它包含的定义符号（非*符号）的数量。**



##### 25.1.2.2 Defining Length

![image-20231201033150312](D:\笔记\笔记图片\image-20231201033150312.png)

![image-20231201033356208](D:\笔记\笔记图片\image-20231201033356208.png)

**定义**：模式的定义长度 *δ*(*H*) 指的是在模式中，两个定义符号（即非“*”符号）之间的最大距离。



![image-20231201033420026](D:\笔记\笔记图片\image-20231201033420026.png)





## Lecture26_Schema_Theorem

![image-20231201033632594](D:\笔记\笔记图片\image-20231201033632594.png)

### 26.1 Schema Theorem

![image-20231201035310343](D:\笔记\笔记图片\image-20231201035310343.png)

![image-20231201035824236](D:\笔记\笔记图片\image-20231201035824236.png)

#### 26.1.1 Schema Theorem: Proof

##### 26.1.1.1 crossover

![image-20231201040528086](D:\笔记\笔记图片\image-20231201040528086.png)

![image-20231201040544213](D:\笔记\笔记图片\image-20231201040544213.png)

![image-20231201042214192](D:\笔记\笔记图片\image-20231201042214192.png)

![image-20231201042200795](D:\笔记\笔记图片\image-20231201042200795.png)



##### 26.1.1.2 mutation

![image-20231201042315681](D:\笔记\笔记图片\image-20231201042315681.png)





















