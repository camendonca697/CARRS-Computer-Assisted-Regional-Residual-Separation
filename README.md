CARRS (Computed Assisted Regional Residual Separation) 

The computer codes made available with this publication are organized in a set of 6 short MATLAB scripts labelled as prog01 to prog06 (pro07 only replicates figures in the paper). 
With the previously computed results in this distribution, you can start by running prog03 to avoid time consuming derivative evaluations in prog02. 
	prog01_SetMuValues illustrates the curvature and gradient shapes for data profiles when regularized derivatives are evaluated under its default criterion (discrepancy principle) or fixing a predetermined value specifying the noise level in data. Regularization parameters set in this step will be used to process the entire data set. 
	prog02_EvaluateRegularizedDerivatives evaluates the first and second order derivatives for the rows and columns of the gridded data set. For the provided data set, this operation may demand half an hour according to memory and clock specifications of the computer running the code. Once evaluated, the regularized derivatives are saved as gz1x.res, gz2x.res, gz1y.res gz2y.res files to save repetition of this time-demanding operation (~20 min). 
	prog03_SetEpslonParameters allows the user to interactively prescribe the thresholds ε_G and ε_L to identify grid points where the anomaly will be regarded as flat. A picture as shown in Figure 8a is generated. With ioption=0 the selected threshold values as in the paper are set; in making ioption = 1 you can select your own ε_G  and ε_L values. File ifm.res assigns 1 to grid points identified as lying in flat positions.
	prog04_PolynomialFitting utilizes the points selected in the former step to obtain candidate regional-fields with robust poly44, poly55 and LOWESS models.
	prog05_AnalysisAlongProfiles displays the regional models along profiles, as illustrated in Figure 9, but scanning the entire data set with a large number of profiles. 
	prog06_DataFittingQuality evaluates the data fitting quality to the selected low curvature and gradient points; cross-plot picture for the observed to the polynomial-fitting data. 
	prog07_PaperFigures reproduces figures in the real data application section of the paper.

https://doi.org/10.1190/geo2023-0546.1
