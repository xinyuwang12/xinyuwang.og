---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<!-- {% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %} -->

## Preprints

- Experimental study on mechanical and seepage properties of sandstone samples under axial unloading-reloading conditions.
- Evolution of mining-induced water inrush disaster from a hidden fault in coal seam floor based on a coupled stress-seepage-damage model.
- Theoretical and numerical investigations on wing crack initiation and propagation in rock materials containing a pre-existing crack under hydro-mechanical interaction.
- A coupled stable node-based smoothed PFEM for soil-structure interaction with large deformation.
- **Zhang Q**<sup>\*</sup>, Chen Y, Yang Z (2020) Data Driven Solutions and Discoveries in Mechanics Using Physics Informed Neural Network. [[Link]](https://doi.org/10.20944/preprints202006.0258.v1){:target="_blank"}



## Main work

- **Zhang Q**, Wang ZY, Yin ZY<sup>\*</sup>, Jin YF (2022) A novel stabilized NS-FEM formulation for anisotropic double porosity media. *Computer Methods in Applied Mechanics and Engineering* 401:115666 [[Code]](https://github.com/qizhang94/GEOKEYFEM_HM/releases){:target="_blank"} [[PDF]](../files/CMAME_115666.pdf){:target="_blank"} [[Rebuttal]](../files/CMAME_115666_Rebuttal.pdf){:target="_blank"}
    [<a href="javascript:void(0)" onclick="(function(target, id) { if ($('#' + id).css('display') == 'block') { $('#' + id).hide('fast'); $(target).text('Summary') } else { $('#' + id).show('fast'); $(target).text('Summary▲') } })(this, 'ZhangCMAME22');">Summary</a>]
<div id="ZhangCMAME22" style="display:none;">
<pre  style="white-space: normal; word-break: keep-all; background-color: #EBECE4">
Self-consistent extension of linear poroelasticity to overlapping scales of porosity within fluid-saturated anisotropic materials is developed. The coefficient matrix of poromechanical properties considering anisotropy is firstly derived from the corresponding intrinsic properties of its single porosity constituents. The momentum supply term arising from the mass transfer is also quantitatively analyzed. To provide further insight into the theory, numerical values of the poroelastic coefficients are calculated for sandstone that are consistent with the material parameters reported by prominent authors. Then, the node-based smoothed finite element method (NS-FEM) is extended to implement the coupled double porosity flow and deformation formulation. In order to provide numerical stability and accuracy, a modified nodal integration scheme based on multiple stress points over the smoothing domain (SD) and the polynomial pressure projection (PPP) scheme are further implemented in the NS-FEM. Next, four benchmark tests are simulated and compared with reference solutions, based on which the correctness of the proposed NS-FEM formulation is verified and the generalizability of the derived anisotropic double porosity model is confirmed. Finally, the elastoplastic response of double porosity media is investigated, including the impact of permeability anisotropy, the impact of permeability contrast, and the impact of strain-softening.
</pre></div>


- Wang Z, **Zhang Q**<sup>\*</sup>, Zhang W (2022) A novel collaborative study of abnormal roof water inrush in coal seam mining based on strata separation and wing crack initiation. *Engineering Failure Analysis* 142:106762 [[PDF]](../files/EFA_106762.pdf){:target="_blank"}
    [<a href="javascript:void(0)" onclick="(function(target, id) { if ($('#' + id).css('display') == 'block') { $('#' + id).hide('fast'); $(target).text('Summary') } else { $('#' + id).show('fast'); $(target).text('Summary▲') } })(this, 'WangEFA22');">Summary</a>]
<div id="WangEFA22" style="display:none;">
<pre  style="white-space: normal; word-break: keep-all; background-color: #EBECE4">
Separation water inrush poses a potential threat to safe mining on the working face, whose mechanism should be investigated in order to take better prevention and control measures. In this study, aiming at the problem of separation water inrush under hydrostatic pressure, the 21805 working face of the Yushujing coal mine was chosen as the research object to establish an in-house similar simulation experiment. The experiment could reveal the evolution law of bed separation space, the process of water accumulation in bed separation space, and the breaking characteristics of separation water inrush. Meanwhile, in order to theoretically interpret the evolution of water-conducting fractured zone (WCFZ), an analytical model for wing crack initiation from compression-shear fracture and tension-shear fracture that considers T-stress was derived. The analytical model comprehensively considers the effects of overlying strata load and aquifer water pressure, fracture geometry, and rock properties. The results show that the time of separation water inrush obtained by the similar simulation experiment is consistent with the field result, and the orientation of new cracks generated due to water injection also coincides with the analytical solution. In addition, it is found that the development of bed separation space is a long-term process, which can provide a theoretical basis for the prevention and control of separation water inrush.
</pre></div>


- **Zhang Q**, Yan X<sup>\*</sup>, Li Z (2022) A mathematical framework for multiphase poromechanics in multiple porosity media. *Computers and Geotechnics* 146:104728 [[PDF]](../files/CAGT_104728.pdf){:target="_blank"} [[Rebuttal 1]](../files/CAGT_104728_Rebuttal-pdf){:target="_blank"} [[Rebuttal 2]](../files/CAGT_104728_Rebuttal2.pdf){:target="_blank"}
    [<a href="javascript:void(0)" onclick="(function(target, id) { if ($('#' + id).css('display') == 'block') { $('#' + id).hide('fast'); $(target).text('Summary') } else { $('#' + id).show('fast'); $(target).text('Summary▲') } })(this, 'ZhangCAGT22');">Summary</a>]
<div id="ZhangCAGT22" style="display:none;">
<pre  style="white-space: normal; word-break: keep-all; background-color: #EBECE4">
Unconventional geomaterials often exhibit multi-modal pore size distribution. We have developed a comprehensive framework for porous media exhibiting multiple porosity scales that are saturated with one or two types of fluids using mixture theory. Both the governing equations and constitutive laws have been clearly derived and identified, respectively. The effective stress emerged from the energy balance equation is adoptable for both elastic and elastoplastic deformations, in which pore fractions and saturations play a central role. The proposed model is general in a sense that it works for both uncoupled simulation and coupled simulation. The field equations for uncoupled flow simulation are solved using the Laplace transform and numerical Laplace inversion methods. By visualizing the dimensionless results, we can gain a quantitative insight of the different stages in the depletion process of a naturally fractured reservoir. For coupled flow and geomechanics simulation, a strip load problem and a two-phase flow in a deformable 3D reservoir problem illustrate the impacts of plasticity, multiple porosity, inter-porosity exchange, and capillary pressure on the system response.
</pre></div>


- **Zhang Q**, Wang Z<sup>\*</sup> (2021) Spatial prediction of loose aquifer water abundance mapping based on a hybrid statistical learning approach. *Earth Science Informatics* 14(3):1349-1365 [[PDF]](../files/ESIN_2021.pdf){:target="_blank"}
    [<a href="javascript:void(0)" onclick="(function(target, id) { if ($('#' + id).css('display') == 'block') { $('#' + id).hide('fast'); $(target).text('Summary') } else { $('#' + id).show('fast'); $(target).text('Summary▲') } })(this, 'ZhangESIN21');">Summary</a>]
<div id="ZhangESIN21" style="display:none;">
<pre  style="white-space: normal; word-break: keep-all; background-color: #EBECE4">
In order to study and prevent water hazards in coal mines under thick loose strata, we need to make correct assessments of their water abundance levels based on the limited borehole data. According to the multi-source information composite principle, five main influencing factors of water abundance are chosen, and they are: the aquifer thickness, the thickness ratio between sandy and clayey layers, the consumption of the drilling fluid, the core recovery rate, and the hydraulic conductivity. Their spatial variations in the whole study area could be inferred from Kriging interpolation. Next, we have developed a novel off-the-shelf two-step assessment approach. In the first step, we apply a dimensionality reduction technique called Fisher discriminant analysis (FDA) to project the original normalized data into a low-dimensional space, which is convenient for data visualization. In this projection process, we want to keep the original information as much as possible. In the second step, we train three classification algorithms on the same transformed low-dimensional data to predict the water abundance level, and leave-one-out cross-validation is used to validate our proposed method due to data sparsity. Finally, the comprehensive zoning map of the study area's water abundance level is established, which can provide scientific guidance for the mining operations and prevention of mine water hazards in this region. The whole process is further elaborated through a case study of the Baodian coal mine, from which we are able to know the location with the highest water abundance level.
</pre></div>



- **Zhang Q**, Borja RI<sup>\*</sup> (2021) Poroelastic coefficients for anisotropic single and double porosity media. *Acta Geotechnica* 16(10):3013-3025 [[PDF]](../files/ACTA_GEOT.pdf){:target="_blank"}(TYPO is marked) [[Excel]](https://github.com/qizhang94/GEOKEYFEM_HM/releases/tag/v4.0.0){:target="_blank"}
    [<a href="javascript:void(0)" onclick="(function(target, id) { if ($('#' + id).css('display') == 'block') { $('#' + id).hide('fast'); $(target).text('Summary') } else { $('#' + id).show('fast'); $(target).text('Summary▲') } })(this, 'ZhangAGEO21');">Summary</a>]
<div id="ZhangAGEO21" style="display:none;">
<pre  style="white-space: normal; word-break: keep-all; background-color: #EBECE4">
Closed-form expressions for poroelastic coefficients are derived for anisotropic materials exhibiting single and double porosity. A novel feature of the formulation is the use of the principle of superposition to derive the governing mass conservation equations from which analytical expressions for the Biot tensor and Biot moduli, among others, are derived. For single porosity media, the mass conservation equation derived from the principle of superposition is shown to be identical to the one derived from continuum principle of thermodynamics, thus confirming the veracity of both formulations and suggesting that this conservation equation can be derived in more than one way. To provide further insight into the theory, numerical values of the poroelastic coefficients are calculated for granite and sandstone that are consistent with the material parameters reported by prominent authors. In this way, modelers are guided on how to determine these coefficients in the event that they use the theory for full-scale modeling and simulations.
</pre></div>



- Yan X, Sun H<sup>\*</sup>, Huang Z, Liu L, Wang P, **Zhang Q**, Yao J<sup>\*</sup> (2021) Hierarchical Modeling of Hydromechanical Coupling in Fractured Shale Gas Reservoirs with Multiple Porosity Scales. *Energy & Fuels* 35(7):5758-5776



- Shao J, **Zhang Q**<sup>\*</sup>, Zhang W, Wang Z, Wu X (2021) Effects of the borehole drainage for roof aquifer on local stress in underground mining. *Geomechanics and Engineering* 24(5):479-490 [[PDF]](../files/GAE09290C_online.pdf){:target="_blank"}
    [<a href="javascript:void(0)" onclick="(function(target, id) { if ($('#' + id).css('display') == 'block') { $('#' + id).hide('fast'); $(target).text('Summary') } else { $('#' + id).show('fast'); $(target).text('Summary▲') } })(this, 'ShaoGAE21');">Summary</a>]
<div id="ShaoGAE21" style="display:none;">
<pre  Pre-drainage of groundwater in the roof aquifer by boreholes is the main method for prevention of roof water disaster, and the drop in the water level during the drainage leads to the variation of the local stress in the overlying strata. Based on a multitude of boreholes for groundwater drainage from aquifer above the 1303 mining face of Longyun Coal Mine, theoretical analysis and numerical simulation are used to investigate the local stress variation in the process of borehole drainage. The results show that due to the drop in the water level of the roof aquifer during the drainage, the stress around the borehole gradually evolved. From the center of the borehole to the outside, a stress-relaxed zone, a stress-elevated zone, and a stress-recovered zone are sequentially formed. Along with the expansion of drainage influence, the stress peak in the stress-elevated zone also moves to the outside. When the radius of influence develops to the maximum, the stress peak position no longer moves outward. When the coal mining face advances to the drainage influence range, the abutment pressure in front of the mining face is superimposed with the high local stress around the borehole, which increases the risk of stress concentration. The present study provides a reference for the stress concentration caused by borehole drainage, which can be potentially utilized in the optimal arrangement of drainage boreholes in underground mining.
</pre></div>



- **Zhang Q**<sup>\*</sup>, Yan X, Shao J (2021) Fluid flow through anisotropic and deformable double porosity media with ultra-low matrix permeability: A continuum framework. *Journal of Petroleum Science and Engineering* 200:108349



- **Zhang Q**<sup>\+</sup>, Chen Y<sup>\+</sup>, Yang Z<sup>\+</sup>, Darve E<sup>\*</sup> (2020) Multi-Constitutive Neural Network for Large Deformation Poromechanics Problem. Proceedings of the Machine Learning and the Physical Sciences Workshop, 34<sup>th</sup> Conference on Neural Information Processing Systems (NeurIPS) [[PDF]](../files/2010.15549.pdf){:target="_blank"}
    [<a href="javascript:void(0)" onclick="(function(target, id) { if ($('#' + id).css('display') == 'block') { $('#' + id).hide('fast'); $(target).text('Summary') } else { $('#' + id).show('fast'); $(target).text('Summary▲') } })(this, 'MCNN');">Summary</a>]
<div id="MCNN" style="display:none;">
<pre  In this paper, we study the problem of large-strain consolidation in poromechanics with deep neural networks (DNN). Given different material properties and different loading conditions, the goal is to predict pore pressure and settlement. We propose a novel method *multi-constitutive neural network* (MCNN) such that one model can solve several different constitutive laws. We introduce a one-hot encoding vector as an additional input vector, which is used to label the constitutive law we wish to solve. Then we build a DNN which takes $(\hat{X}, \hat{t})$ as input along with a constitutive law label and outputs the corresponding solution. It is the first time, to our knowledge, that we can evaluate multi-constitutive laws through only one training process while still obtaining good accuracies. We found that MCNN trained to solve multiple PDEs outperforms individual neural network solvers trained with PDE in some cases.
</pre></div>


- **Zhang Q**<sup>\*</sup> (2020) Hydromechanical modeling of solid deformation and fluid flow in the transversely isotropic fissured rocks. *Computers and Geotechnics* 128:103812
- **Zhang Q**, Choo J, Borja RI<sup>\*</sup> (2019) On the preferential flow patterns induced by transverse isotropy and non-Darcy flow in double porosity media. *Computer Methods in Applied Mechanics and Engineering* 353:570-592
- **Zhang Q**<sup>\*</sup>, Zhu H (2018) Collaborative 3D geological modeling analysis based on multi-source data standard. *Engineering Geology* 246:233-244 [[PDF]](../files/ENGEO-myfirstsci.pdf){:target="_blank"}


## Other

- Strip load on transversely isotropic elastic double porosity media with strong permeability contrast. [*Advances in Geo-Energy Research*](https://www.yandy-ager.com/index.php/ager/index){:target="_blank"} (ESCI and EI indexed, OA Journal, Chinese Academy of Sciences JCR Q4) [[PDF]](../files/AGER_20210402.pdf){:target="_blank"}
- Mathematical Evaluation on the Control of Mining-Induced Ground Subsidence in Thick Loose Strata. *ACS Omega* [[PDF]](../files/ACSO.pdf){:target="_blank"}
- New Type of Similar Material for Simulating the Processes of Water Inrush from Roof Bed Separation. *ACS Omega*
- Numerical Investigation of the Effect of Partially Propped Fracture Closure on Gas Production in Fractured Shale Reservoirs. *Energies*
- Investigation on the Water Flow Evolution in a Filled Fracture under Seepage-Induced Erosion. *Water*
- Numerical Simulation on Non-Darcy Flow in a Single Rock Fracture Domain Inverted by Digital Images. *Geofluids*
- Experimental Study on the Basic Properties of a Green New Coal Mine Grouting Reinforcement Material. *ACS Omega*
- Study on the mechanism and prevention measures of roof separation water inrush (2021). China University of Mining and Technology Press《顶板离层水突涌机理及防治措施研究》中国矿业大学出版社
