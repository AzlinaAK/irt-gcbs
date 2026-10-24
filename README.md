# IRT analysis of the Generic Conspiracist Beliefs Scale (GCBS)

Polytomous item response theory analysis of the 15-item Generic Conspiracist Beliefs Scale (Brotherton, French & Pickering, 2013) in R, using the mirt package.

## Questions
1.  Can the GCBS be treated as measuring a single latent trait, or is there evidence of more than one dimension?
2. Do any items function differently for men and women (DIF)?
3. Which respondents do not fit the model?

## Methods
1. Unidimensional graded response model (GRM): item parameters, global fit (M2) and item fit (S-X2 with Benjamini-Hochberg correction)
2.  Exploratory two- and three-factor models (oblimin rotation), compared with the one-factor model
3.  Gender DIF using a multiple-group GRM, with sequential purification (BIC)
4.  Person fit (Zh)

## Key findings
1. A one-factor GRM fitted acceptably (RMSEA = .043, CFI = .97, TLI = .96), supporting use of a single total score.
2.  More than one dimension was also supported: fit improved from one to two and from two to three factors. The Extraterrestrial Cover-up and Malevolent Global Conspiracies facets formed clear separate factors; factors were strongly correlated (r = .61 to .80).
3. No items showed meaningful misfit after correction for multiple comparisons.
4. Two of 15 items (Q3 and Q8, both Extraterrestrial Cover-up) showed gender DIF: at the same level of overall belief, women were more likely to endorse them, by roughly 0.3 to 0.5 response points.
5. 17 respondents had |Zh| > 3; several showed contrasting patterns on the Extraterrestrial Cover-up items compared with the rest of the scale.

## Files
1. `index.html`: rendered report
2.  `GCBS_IRT_Analysis.Rmd`: analysis code

## Data
Open Source Psychometrics Project (2016), GCBS responses: https://openpsychometrics.org/_rawdata/ (file GCBS.zip). Online convenience sample; N = 2,269 after excluding missing responses and gender codes other than male or female (1,086 women, 1,183 men). Items scored 1 (definitely not true) to 5 (definitely true).

To reproduce the analysis, download GCBS.zip from the link above, unzip it, and place `data.csv` in the same folder as the .Rmd file.

## Limitations
1. Convenience sample with no check for careless responding 
2. A four-factor model did not converge, and the published five-facet structure was not tested confirmatorily
3. DIF effect sizes were read from expected-score plots rather than computed formally.

## Reference
Brotherton, R., French, C. C., & Pickering, A. D. (2013). Measuring belief in conspiracy theories: The Generic Conspiracist Beliefs Scale. *Frontiers in Psychology, 4*, 279.
