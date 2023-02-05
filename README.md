# FaultDiagnosis

## About Dataset
### Overview
The Grid-connected PV System Faults (GPVS-Faults) data are collected from lab experiments of faults in a PV microgrid system. There are 16 data files in ‘.mat’ and also ‘.csv’, each for one experiment scenario, including photovoltaic array faults; inverter faults; grid anomalies; feedback sensor fault; and MPPT controller faults of various severity. GPVS-Faults data can be used to design/ validate/ compare various algorithms of fault detection/ diagnosis/ classification for PV system protection and reactive maintenance.  

### Description 
The faults were introduced manually halfway during the experiments. The high-frequency measurements are noisy; with disturbances and variations of temperature and insolation during and between the experiments; MPPT/IPPT modes have adverse effects on the detection of low-magnitude faults. After critical faults, the operation is interrupted and the system may shut-down; the challenge is to detect the faults before a total failure.

We refer interested researchers to read and cite the following references for detailed descriptions of: 
- GPVS-Faults scenarios, experiments, and data collection procedures are described in [1] with results for comparisons. 
- System description, energy management system, control/ communication of the PV system are detailed in [2]. 
-The description of the static multiblock version of the fault detection algorithm was presented in [3]. 
References
[1]. A. Bakdi, W. Bounoua, A. Guichi, S. Mekhilef, (2020). Real-time fault detection in PV systems under MPPT using PMU and high-frequency multi-sensor data through online PCA-KDE-based multivariate KL Divergence. International Journal of Electrical Power & Energy Systems. 
[2]. A. Guichi, A. Talha, E. M. Berkouk, S. Mekhilef, S. Gassab, (2018). A new method for intermediate power point tracking for PV generator under partially shaded conditions in hybrid system. Sol. Energy. 170, 974-987. https://doi.org/10.1016/j.solener.2018.06.027.
[3]. A. Bakdi, W. Bounoua, S. Mekhilef, L. M. Halabi, (2019). Nonparametric Kullback-divergence-PCA for intelligent mismatch detection and power quality monitoring in grid-connected rooftop PV. Energy, 116366. https://doi.org/10.1016/j.energy.2019.116366.

### Structure
GPVS-Faults data files are labelled as “Fxy”, where: 
	x∈{0,1,…,7} represents the fault scenario:
		'0' is a fault-free experiment. 
		'1',…,'7' are the 7 types of faults.
	y∈{'L','M'} is the operation mode: 
		'L' is Limited power mode (IPPT)
		'M' is Maximum power mode (MPPT)
e.g. “F4M” is fault F4 in MPPT mode, “F1L” is fault F1 in IPPT mode. 

Each data file includes the following columns: 
	Time: Time in seconds, average sampling T_s=9.9989 μs.
	Ipv: PV array current measurement. 
	Vpv: PV array voltage measurement.  
	Vdc: DC voltage measurement. 
	ia, ib, ic: 3-Phase current measurements. 
	va, vb, vc: 3-Phase voltage measurements.
	Iabc: Current magnitude.  
	If: Current frequency.
	Vabc: Voltage magnitude.  
	Vf: Voltage frequency.
