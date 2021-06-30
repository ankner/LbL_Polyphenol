# LbL_Polyphenol
Excel sheets implementing LbL polyphenol fitting

The Excel sheets in this archive accompany the manuscript "Dynamics and Self-Healing of Layer-by-Layer Hydrogen-Bonded Films of Linear Synthetic Polyphenols", by Raman Hlushko, John F. Ankner, and Svetlana A. Sukhishvili, which is currently under review at the journal Macromolecules (as of July 2021).

There are four sets of Excel sheets representing specular neutron reflectivity fits to data collected from four different samples: hydrogen-bonded polyphenol (PnHxA) / poly(ethylene oxide) PEO multilayer films deposited on silicon (Si) substrates using the Layer-by-Layer (LbL) technique: 1) P2HAA/PEO; 2) P3HAA/PEO; 3) P2HMA/PEO; and 4) P3HMA/PEO.  These four films were subsequently exposed to deuterated PEO (dPEO) solutions for 1, 2, 5, and 10 (P2HMA and P3HAA) minutes.

1) P2HAA/PEO:

REF_L_174481_2_P2HAA_110h_Final

REF_L_174529_2_P2HAA_110h_1min_Final

REF_L_174579_2_P2HAA_110h_2min_Final

REF_L_174702_2_P2HAA_110h_5min_Final

2) P3HAA/PEO:

REF_L_174473_3_P3HAA_108h_Final

REF_L_174521_3_P3HAA_108h_1min_Final

REF_L_174571_3_P3HAA_108h_2min_Final

REF_L_174695_3_P3HAA_108h_5min_Final

REF_L_174772_3_P3HAA_108h_10min_Final

3) P2HMA/PEO:

REF_L_174457_13_P2HMA_110h_Final

REF_L_174505_13_P2HMA_110h_1min_Final

REF_L_174555_13_P2HMA_110h_2min_Final

REF_L_174681_13_P2HMA_110h_5min_Final

REF_L_174758_13_P2HMA_110h_10min_Final

4) P3HMA/PEO:

REF_L_161498_2_P3HMA_112h_Final

REF_L_161589_2_P3HMA_112h_1min_Final

REF_L_161610_2_P3HMA_112h_2min_Final

REF_L_161694_2_P3HMA_112h_5min_Final

The Excel sheets use macros to calculate reflectivity, evaluate goodness-of-fit, and perform most other operations. They can therefore be viewed using open-source programs such as Gnumeric or LibreOffice, but they are only really functional when run in Excel with Macros enabled. Each sheet is independent of the others and contains all of the machinery needed to modify and optimize model fits. The sheets consist of a number of tabs, including:

Reflectivity tab:

This is the master sheet and contains the model parameters (columns B-H), data (columns I-K), model fit (column L), and fitted model scattering-length density (SLD) profile (columns M-S).  Due to variation of film thickness across the 2"-diameter substrate, fitted reflectivity curves were incoherently smeared (2-3%).   The smeared reflectivities are found in columns U-Y.  Data can be loaded from 3-column text files (the '#' symbol identifies commented lines not to be loaded) by typing ctrl-l (l as in "load"); reflectivity is evaluated by ctrl-r; and plotted data and fit display can be toggled between R and RQ^4 by ctrl-q.  Incoherent smearing is calculated using ctrl-s.

SLDs, absorptions, thicknesses and full-width-at-half-maximum (fwhm) interfacial widths are entered or calculated into the labeled columns starting at row 3.  Layers are added to the model and evaluated until the first blank row.  We have primarily used column H for parameters used to calculate and populate the reflectivity columns, but these calculations can be done anywhere on the sheet.  The calculations are described in detail in the Supplementary Information of the manuscript.  The sheets are, however, not limited in function and the models can be modified or the sheets repurposed entirely to fit different data. Goodness-of-fit is given by chi-squared in cell A10 for the bare reflectivity or in cell Y2 for the incoherently smeared reflectivity.

Uncertainties tab:

The values and statistical uncertainties of model parameters discussed in the manuscript are calculated and displayed here.

Fitted parameters tabs:

Each fitted parameter in the model has its own tab (e.g. density in REF_L_161498_2_P3HMA_112h_Final).  Parameters are identified by which cell they occupy in the Reflectivity tab (cell A2 in the parameter tab) and can be varied through a range of values (Start, Stop, and Nsteps) in cells (B-D)2.  Pressing ctrl-p evaluates the bare model reflectivity over the desired range and fits a parabola to the chi-squared profile.  Parameter minimum chi-squared and uncertainty are written in cells C4 and D4, respectively.  Fitting incoherently smeared reflectivity is done using ctrl-i.  New parameters can be added by copying, relabeling, and editing an existing parameter tab using standard Excel commands.

ScaledCombined tab:

A copy of the text file used to load in the data using the ctrl-l command in the Reflectivity tab. Data can also be cut and pasted into the relevant columns in the Reflectivity tab. Information on the ScaledCombined tab is purely documentary and does not affect the operation of the other features.

ScatteringParameters tab:

A neutron SLD calculator (using ActiveX so it won't work on Macs). Press the Compound Calculator button, enter values in the popup, and press Enter in the popup to add a line to the table. Cut and paste from columns D-F to appropriate columns C-E in the Reflectivity tab.

AtomicParameters tab:

The isotopic parameters used for the calculations in the ScatteringParameters tab (compiled by Varley Sears several decades ago).

This brief description is not in any way comprehensive, but feel free to contact the authors if questions or problems arise.
