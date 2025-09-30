Reference:
	2024A&A...TBD
Title: 
	Dense gas tracer scaling relations at kiloparsec scale across nearby galaxies with the ALMA ALMOND 
	and IRAM 30-m EMPIRE surveys
	
Authors: 
	Lukas Neumann, María J. Jiménez-Donaire, Adam K. Leroy, Frank Bigiel, Antonio Usero, Jiayi Sun, 
	Eva Schinnerer, Miguel Querejeta, Sophia K. Stuber, Ivana Bešlić, Ashley Barnes, Jakob den Brok, 
	Yixian Cao, Cosima Eibensteiner, Hao He, Ralf S. Klessen, Fu-Heng Liang, Daizhong Liu, Hsi-An Pan, 
	Thomas G. Williams
	
Abstract: 
	Dense, cold gas is the key ingredient for star formation. Over the last two decades, HCN(1-0) emission 
	has been utilised as the most accessible dense gas tracer to study external galaxies. We present new 
	measurements tracing the relationship between dense gas tracers, bulk molecular gas tracers, and star 
	formation in the ALMA ALMOND survey, the largest sample of resolved (1-2 kpc resolution) HCN maps 
	of galaxies in the local universe (d < 25 Mpc). We measure HCN/CO, a line ratio sensitive to the physical 
	density distribution, and SFR/HCN, a proxy for the dense gas star formation efficiency, as a function of 
	molecular gas surface density, stellar mass surface density, and dynamical equilibrium pressure across 
	31 galaxies, increasing the number of galaxies by a factor of > 3 over the previous largest such study 
	(EMPIRE). HCN/CO increases (slope of ~ 0.5 and scatter of ~ 0.2 dex), while SFR/HCN decreases 
	(slope of ~ -0.6 and scatter of ~ 0.4 dex) with increasing molecular gas surface density, stellar mass 
	surface density and pressure. Galaxy centres with high stellar mass surface density show a factor of a 
	few higher HCN/CO and lower SFR/HCN compared to the disc average, but both environments follow 
	the same average trend. Our results emphasise that molecular gas properties vary systematically with 
	the galactic environment and demonstrate that the scatter in the Gao-Solomon relation (SFR against HCN) 
	is of physical origin.
	
------------------------------------------
Description:
	This directory contains the data products (directory "data") and tables (directory "maps") published in 
	Neumann et al., 2024b (2024A&A...TBD). The data products are produced using the PyStructure pipeline 
	(https://github.com/jdenbrok/PyStructure) following the procedure described in the paper. The stacked 
	spectra are obtained via the PyStacker package (https://github.com/PhangsTeam/PyStacker) as described 
	in the paper and in Neumann et al., 2023b (2023A&A...675A.104N). All files are provided as csv files. 
	A column-by-column description is provided below.

Scripts:	
	All scripts used to process, analyse and visualise the data are publicly available via: 
	https://github.com/lukas-neumann-astro/publications/tree/main/Neumann_etal_2024b/. 


Description of files
-------------------------------------------------------------------------------------------
File					Description
-------------------------------------------------------------------------------------------
data/HCN_literature_compilation.csv	HCN and SFR literature compilation
data/sightlines.csv			pixel-based measurements
data/sightlines_centres.csv		galaxy centre measurements
data/sightlines_wo_centres.csv		pixel-based measurements excluding the galaxy centres
data/stacks_pressure.csv		spectral stacks of HCN and CO as a function of dynamical equilibrium pressure
data/stacks_pressure_wo_centres.csv	spectral stacks of HCN and CO as a function of dynamical equilibrium pressure (excluding galaxy centres)
data/stacks_SDmol.csv			spectral stacks of HCN and CO as a function of molecular gas surface density
data/stacks_SDmol_wo_centres.csv	spectral stacks of HCN and CO as a function of molecular gas surface density (excluding galaxy centres)
data/stacks_SDstar.csv			spectral stacks of HCN and CO as a function of stellar mass surface density
data/stacks_SDstar_wo_centres.csv	spectral stacks of HCN and CO as a function of stellar mass surface density (excluding galaxy centres)
tables/Table_1.csv			Gao-Solomon relation across literature data sets
tables/Table_2.csv			dense gas scaling relation fit parameters
tables/Table_E1.csv			galaxy sample table
tables/Table_E2.csv			dense gas ratio statistics in centre vs disc regtions
-------------------------------------------------------------------------------------------

------------------------------------------

*data*

Column-by-column description of file: data/HCN_literature_compilation.csv	
-------------------------------------------------------------------------------------------
Col	Label			Units		Explanation	
-------------------------------------------------------------------------------------------
0	Name			none		short name of the reference
1	L_CO			K.km/s.pc2	CO(1-0) luminosity 
2	L_HCN			K.km/s.pc2	HCN(1-0) luminosity
3	L_TIR			Lsun		total infrared luminosity
4	M_mol			Msun		molecular gas mass
5	M_dense			Msun		dense gas mass
6	SFR			Msun/yr		star formation rate
7	Type			none		target catagory
8	Target			none		target
9	Reference		none		reference
10	Publication date	MM/YYYY		date of publication
-------------------------------------------------------------------------------------------

Column-by-column description of file: data/sightlines.csv	
and analogously for 
data/sightlines_centres.csv; 
data/sightlines_wo_centres.csv
-------------------------------------------------------------------------------------------
Col	Label				Units		Explanation	
-------------------------------------------------------------------------------------------
0	Survey				none		name of the survey
1	Galaxy				none		name of the galaxy
2	R.A				deg		right ascension (J2000)
3	Dec.				deg		declination (J2000)
4	rgal				kpc		galactocentric radius
5	W_CO21				K.km/s		CO(2-1) integrated intensity*
6	e_W_CO21			K.km/s		uncertainty of CO(2-1) integrated intensity*
7	W_CO10				K.km/s		CO(1-0) integrated intensity*
8	e_W_CO10			K.km/s		uncertainty of CO(1-0) integrated intensity*
9	W_HCN				K.km/s		HCN(1-0) integrated intensity
10	e_W_HCN				K.km/s		uncertainty of HCN(1-0) integrated intensity
11	W_HCOP				K.km/s		HCO+(1-0) integrated intensity
12	e_W_HCOP			K.km/s		uncertainty of HCO+(1-0) integrated intensity
13	SD_mol (MW)			Msun/pc2	molecular gas surface density, constant CO-to-H2 factor
14	e_SD_mol (MW)			Msun/pc2	uncertainty of molecular gas surface density, constant CO-to-H2 factor
15	SD_mol (SL24) 			Msun/pc2	molecular gas surface density, varying CO-to-H2 factor
16	e_SD_mol (SL24) 		Msun/pc2	uncertainty of molecular gas surface density, varying CO-to-H2 factor
17	SD_dense			Msun/pc2	dense gas surface density
18	e_SD_dense			Msun/pc2	uncertainty of dense gas surface density
19	SD_star				Msun/pc2	stellar mass surface density
20	e_SD_star			Msun/pc2	uncertainty of stellar mass surface density
21	P_DE (MW)			kB.K/cm3	dynamical equilibrium pressure, constant CO-to-H2 factor
22	e_P_DE (MW)			kB.K/cm3	uncertainty of dynamical equilibrium pressure, constant CO-to-H2 factor
23	P_DE (SL24)			kB.K/cm3	dynamical equilibrium pressure, varying CO-to-H2 factor
24	e_P_DE (SL24)			kB.K/cm3	uncertainty of dynamical equilibrium pressure, varying CO-to-H2 factor
25	SD_SFR				Msun/yr/kpc2	star formation rate surface density
26	e_SD_SFR			Msun/yr/kpc2	uncertainty of star formation rate surface density
27	SD_SFR (wo incl. corr.)		Msun/yr/kpc2	star formation rate surface density (without inclination correction)
28	e_SD_SFR (wo incl. corr.)	Msun/yr/kpc2	uncertainty of star formation rate surface density (without inclination correction)
29	Reference			none		short name of the reference
-------------------------------------------------------------------------------------------
* note: for ALMOND, CO(1-0) are inferred from CO(2-1) intensities and vice versa for EMPIRE


Column-by-column description of file: data/stacks_pressure.csv	
and analogously for 
data/stacks_pressure_wo_centres.csv; 
data/stacks_SDmol.csv;
data/stacks_SDmol_wo_centres.csv; 
data/stacks_SDstar.csv; 
data/stacks_SDstar_wo_centres.csv
-------------------------------------------------------------------------------------------
Col	Label				Units		Explanation	
-------------------------------------------------------------------------------------------
0	P_DE (SL24)			kB.K/cm3	dynamical equilibrium pressure, varying CO-to-H2 factor
1	e_P_DE (SL24)			kB.K/cm3	uncertainty of dynamical equilibrium pressure, varying CO-to-H2 factor
2	W_CO21				K.km/s		CO(2-1) integrated intensity*
3	e_W_CO21			K.km/s		uncertainty of CO(2-1) integrated intensity*
4	W_CO10				K.km/s		CO(1-0) integrated intensity*
5	e_W_CO10			K.km/s		uncertainty of CO(1-0) integrated intensity*
6	W_HCN				K.km/s		HCN(1-0) integrated intensity
7	e_W_HCN				K.km/s		uncertainty of HCN(1-0) integrated intensity
8	W_HCOP				K.km/s		HCO+(1-0) integrated intensity
9	e_W_HCOP			K.km/s		uncertainty of HCO+(1-0) integrated intensity
10	SD_mol_MW			Msun/pc2	molecular gas surface density, constant CO-to-H2 factor
11	e_SD_mol_MW			Msun/pc2	uncertainty of molecular gas surface density, constant CO-to-H2 factor
12	SD_mol_SL24			Msun/pc2	molecular gas surface density, varying CO-to-H2 factor
13	e_SD_mol_SL24 			Msun/pc2	uncertainty of molecular gas surface density, varying CO-to-H2 factor
14	SD_dense			Msun/pc2	dense gas surface density
15	e_SD_dense			Msun/pc2	uncertainty of dense gas surface density
16	SD_SFR				Msun/yr/kpc2	star formation rate surface density
17	e_SD_SFR			Msun/yr/kpc2	uncertainty of star formation rate surface density
18	SD_SFR (wo incl. corr.)		Msun/yr/kpc2	star formation rate surface density (without inclination correction)
19	e_SD_SFR (wo incl. corr.)	Msun/yr/kpc2	uncertainty of star formation rate surface density (without inclination correction)
20	Survey				none		name of the survey
-------------------------------------------------------------------------------------------
* note: for ALMOND, CO(1-0) are inferred from CO(2-1) intensities and vice versa for EMPIRE


*tables*

Column-by-column description of file: tables/Table_1.csv
-------------------------------------------------------------------------------------------
Col	Label				Units					Explanation	
-------------------------------------------------------------------------------------------
0	data			none			name of the data set
1	SFR/HCN (16th)		Msun/yr/(K.km/s.pc2)	star formation rate-to-HCN(1-0) luminosity ratio (16th percentile)
2	SFR/HCN (median)	Msun/yr/(K.km/s.pc2)	star formation rate-to-HCN(1-0) luminosity ratio (50th percentile)
3	SFR/HCN (84th)		Msun/yr/(K.km/s.pc2)	star formation rate-to-HCN(1-0) luminosity ratio (84th percentile)
4	TIR/HCN (16th)		Lsun/(K.km/s)		total infrared luminosity-to-HCN(1-0) luminosity ratio (16th percentile)
5	TIR/HCN (median)	Lsun/(K.km/s)		total infrared luminosity-to-HCN(1-0) luminosity ratio (50th percentile)
6	TIR/HCN (84th)		Lsun/(K.km/s)		total infrared luminosity-to-HCN(1-0) luminosity ratio (84th percentile)
7	t_tepl_dense (16th)	yr			dense gas depletion time (16th percentile)
8	t_tepl_dense (median)	yr			dense gas depletion time (50th percentile)
9	t_tepl_dense (84th)	yr			dense gas depletion time (84th percentile)
10	e_ff_dense (16th)	none			dense gas star formation efficiency (16th percentile)
11	e_ff_dense (median)	none			dense gas star formation efficiency (50th percentile)
12	e_ff_dense (84th)	none			dense gas star formation efficiency (84th percentile)
-------------------------------------------------------------------------------------------


Column-by-column description of file: tables/Table_2.csv
-------------------------------------------------------------------------------------------
Col	Label		Units	Explanation	
-------------------------------------------------------------------------------------------
0	log(Y)		none	y-axis quantity
1	log(X)		none	x-axis quantity
2	x0		none	x-axis offset
3	m		none	slope
4	m_err		none	slope (1-sigma uncertainty)
5	b		none	intercept
6	b_err		none	intercept (1-sigma uncertainty)
7	sigma		none	1-sigma scatter of S/N>3 data about the best-fit line
8	r_pearson	none	Pearson correlation coefficient of S/N>3 data
9	p_value		none	p-value corresponding to the Pearson correlation coefficient		
-------------------------------------------------------------------------------------------


Column-by-column description of file: tables/Table_E1.csv
-------------------------------------------------------------------------------------------
Col	Label			Units		Explanation	
-------------------------------------------------------------------------------------------
0	Galaxy			none		name of the galaxy
1	R.A			deg		right ascension (J2000)
2	Dec.			deg		declination (J2000)
3	Dist.			Mpc		distance
4	Incl.			deg		inclination
5	M_star (log10)		Msun		stellar mass
6	SFR (log10)		Msun/yr		star formation rate
7	SFR/M_star (log10)	yr-1		star formation rate-to-stellar mass ratio
8	Bar			none		presence of a bar
9	AGN			none		presence of an active galactic nucleus
10	SFR tracer		none		star formation rate tracer(s)
11	HI survey		none		HI 21-cm line survey
12	CO survey		none		CO line survey
13	HCN survey		none		HCN line survey
14	HCN res (as)		arcsec		native HCN resolution
15	HCN res (kpc)		kpc		native HCN resolution-corresponding linear scale
-------------------------------------------------------------------------------------------


Column-by-column description of file: tables/Table_E2.csv
-------------------------------------------------------------------------------------------
Col	Label			Units	Explanation	
-------------------------------------------------------------------------------------------
0	log(Y)			none	y-axis quantity
1	environment		none	environmental region
2	16th perc.		none	16th percentile value of S/N>3 data
3	median			none	50th percentile value of S/N>3 data
4	84th perc.		none	84th percentile value of S/N>3 data
5	median (all S/N)	none	50th percentile value of all S/N data
-------------------------------------------------------------------------------------------


------------------------------------------
**Contact**: [Lukas Neumann](mailto:lukas.neumann.astro@gmail.com)