## Dataset Usage Information

This dataset is available for public use. If you plan to use the dataset, we ask that you kindly fill out the following form to help us understand the usage:

[Dataset Usage Form](https://docs.google.com/forms/d/e/1FAIpQLSextpx9mkF1-JKA9ldpy5wZv6SC-ZmJ9VSPmf5nu5vtkpLRyQ/viewform?usp=header)

Please cite it as follows:

Airaudo, Florencia S., François de Soyres, Keith Richards, and Ana Maria Santacreu (2025). "Fragmentation? Revisiting the Ideal Point Distance measure of geopolitical distance," FEDS Notes. Washington: Board of Governors of the Federal Reserve System, March 21, 2025, https://doi.org/10.17016/2380-7172.3749. [Link to article](https://www.federalreserve.gov/econres/notes/feds-notes/fragmentation-revisiting-the-ideal-point-distance-measure-of-geopolitical-distance-20250321.html)

For any questions or feedback, please reach out to kpr36@georgetown.edu.


---

# Ideal Point Distance Dataset
```
Variables
year : year variable
Code_1 & Code_2: 3 Letter ISO-3166-1 Alpha 3 codes for Country A and Country B respectively. In our analysis Code_1 denotes the importer
sorted : Concatonated string where ISO3 code that is alphabetically first in the pair is the first in the sorted string. Example if Code_1 is DEU and Code_2 is CHN OR Code_1 is CHN and Code_2 is DEU, sorted would be CHN_DEU for both cases.
Country A: Name of Code_1 country.
Country B: Name of Code_2 country.
ipd_all_full: Ideal Point Distnance (IPD) measure using the full sample of UN votes for all vote categories.
ipd_econ_full: IPD measure using the subset of only economic votes. By construction these votes start in the 1971.
ipd_all_short: IPD measure using the sample of all UN votes but beginning after 1991. 
net_allign_af, net_allign_ef, net_allign_as: US-China IPD normalized to [-1,1] for Country A, where 1 indicates complete US allingment and -1 indicates complete China allignment. Suffixes af, ef, as refer to which IPD (all votes-full, economic votes-full, or all votes-short) was used to generate the segmented distribution.
net_allign_af_b, net_allign_ef_b, net_allign_as_b: US-China normalized IPD for Country B.
eu: dummy variable indicating if at elast one country in the country-pair is part of the EU27.
```
Here you can access our dataset containing various Ideal Point Distances measures along with documentation on variable definition and IPD generation process. 
Due to size constraints, we had to split our IPD dataset by year, though the process of reconstrucrting the full panel is straightforward. IPD.7z contains csvs for all years.

Ideal Point Distances are generated using a Bayesian estimation approach based on observed UN voting behavior from Bailey et al 2017. UN Voting data and associated code for the Markov Chain Monte Carlo simulation can be found at the link below.

[UN Voting Data and Associated Code](https://github.com/evoeten/United-Nations-General-Assembly-Votes-and-Ideal-Points/tree/master)

For a more in depth description of the methodology used to generate ideal point distances, see [Bailey et al., 2017](https://www.jstor.org/stable/26363889?seq=1).

Citation: Bailey, Michael A., Anton Strezhnev, and Erik Voeten. "Estimating dynamic state preferences from United Nations voting data." Journal of Conflict Resolution 61, no. 2 (2017): 430-456.



