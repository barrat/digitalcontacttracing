# digitalcontacttracing
This scripts corresponds to the results of the manuscript "Effect of manual and digital contact tracing on COVID-19 outbreaks: a 
study on empirical contact data" by Alain Barrat, Ciro Cattuto, Mikko Kivelä, Sune Lehmann, Jari Saramäki
(medRxiv:2020.07.24.20159947v1), for the SocioPatterns data sets.

The script takes as input the temporal contact data, simulates the spread of a compartmental model of SARS-Cov2 propagation, as well as several 
mitigation measures: 
(i) detection and isolation of severe cases and of a fraction of mild cases
(ii) contact tracing
(iii) digital contact tracing (for contacts between individuals who are assumed to have installed the app).

All the parameters of the compartmental model and of the interventions can be varied at the beginning of the script. In particular, the efficiency of the manual contact tracing is here set to p_ct=0.

The input file can be 
-tij_InVS15_1week.dat : one week of contact data collected in offices by the SocioPatterns collaboration (see www.sociopatterns.org/datasets), here aggregated on 15 minutes resolution: each line is of the form t i j w, meaning that at timestep t individuals i and j met for w seconds. 
-tij_InVS15_1week_0.25removed.dat (same with 25% of contacts removed)

The script 1-Spread_no_measures corresponds to an unmitigated spread.

The script 2-Spread_isolation_MCT_DCT contains measures of isolation of severe cases and a fraction p_md of mild cases, and manual and digital contact tracing. The efficiency of manual contact tracing is p_ct and the script loops over app adoption values from 0 to 1.

The output is a file containing as a function of the app adoption, at given contact tracing efficiency and other parameters,
-fraction of outbreaks reaching less than 10% of individuals
-epidemic size
-normalized number of quarantines
-normalized number of unnecessary quarantines
