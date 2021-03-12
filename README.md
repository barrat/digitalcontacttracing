# digitalcontacttracing
This scripts corresponds to the results of the manuscript "Effect of manual and digital contact tracing on COVID-19 outbreaks: a 
study on empirical contact data" by Alain Barrat, Ciro Cattuto, Mikko Kivelä, Sune Lehmann, Jari Saramäki
(medRxiv:2020.07.24.20159947v1), for the SocioPatterns data sets.

The script takes as input the temporal contact data, simulates the spread of a compartmental model of SARS-Cov2 propagation, as well as several 
mitigation measures: 
(i) detection and isolation of severe cases and of a fraction of mild cases
(ii) contact tracing
(iii) digital contact tracing (for contacts between individuals who are assumed to have installed the app).

The parameters are:

The output is a file containing the epidemic size and fraction of quarantines as a function of the app adoption, 
at given contact tracing efficiency and other parameters. 
