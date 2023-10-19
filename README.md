# SVSH-Registry-Dataset-Project
I first wanted to see if, for college students at UC Berkeley, does living in close proximity to campus-affiliated fraternity housing increase a given student’s chance of being a victim sexual assault (e.g., drugging, rape, coercion). I had issues finding an appropriate enough dataset on the Internet, so I instead framed my question differently and found public datasets for the Washington D.C. area.

Initial Hypothesis: 
H_0: Proximity to a school has no effect on the likelihood of an individual being on the sex offender registry (β = 0).
H_A: Proximity to a school increases the likelihood of an individual being on the sex offender registry (β > 0).

Data: 
I am using two datasets. The first dataset, from https://opendata.dc.gov/, is the complete sex offender registry listing for the Washington, D.C. area, with entries for offenders who are still alive as of 2022. Relevant information includes addresses, date of registry addition, and classification. The second dataset I am using, from the same site, is the entire compilation of Washington, D.C. public school campus locations. Locations are in global X, Y coordinates.

Results:
Registry = 1 + beta * distance_to_school
# beta = 0.049 < 0.05 STATISTICALLY SIGNIFICANT
# Intercept is 1 because there is no comparison to non-registered offenders. 

I used the GeoPy library to calculate minimum distances between each entry of the sex offender registry and their nearest school. In my regression, I found the coefficient to have p-value 0.049 < 0.05, meaning I rejected the null hypothesis. However, the dataset has no entries for people not on the sex offender registry, so the model is unreliable considering I have no comparison.

Takeaways:
In Washington, D.C. where this data is from, and in California where I am currently am, there cannot be restrictions on where someone on the sex offender registry works or lives unless otherwise ordered by the court, meaning a child rapist can live near a school if they wished to do so. By the results of this regression, we see that there is definitely a relationship between school proximity and location of a sex offender, so I think we should change the laws that should make a universal prohibition zone around schools for those on the sex offender registry.
