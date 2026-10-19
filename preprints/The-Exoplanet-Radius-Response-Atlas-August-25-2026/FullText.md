## Page 1

The Exoplanet Radius–Response Atlas
A candidate Hertzsprung–Russell-like organizing diagram for exoplanets
ChatGPT Mark August

25 August 2026

Abstract

A Hertzsprung–Russell-like diagram for exoplanets should organize the population into physically
interpretable sequences, transitions, and outliers rather than merely maximize a two-variable
correlation. We analyzed a 24 August 2026 snapshot of the NASA Exoplanet Archive Planetary
Systems table, screening 190 two-parameter projections, 1,365 four-parameter spaces, and 165
radius response surfaces. After precision cuts, the principal sample contains 1,217 transiting
planets with measured masses, radii, and incident fluxes; 1,141 also have host metallicities. The
best non-tautological organizer is a mass–irradiation control plane in which planet radius is the
response field. A collapsed atlas based on mass-corrected irradiation resolves five empirical zones:
high-forcing compact planets, moderate-forcing sub-Neptunes, a cool giant shelf, warm compact
giants, and hot inflated giants. The underlying response field changes character across a broad
transition at approximately 50–100 Earth masses: the radius–mass slope collapses, the irradiation
response changes from negative to positive, and the metallicity response changes from a localized
positive association at 10–30 Earth masses to a negative association among giants. A two-branch
mass–flux–metallicity model reduces host-grouped held-out radius error by 37.6% relative to a single
global plane. We state quantitative falsification tests for the transition mass, the two irradiation
slopes, the metallicity sign reversal, the sufficiency of the collapsed giant-planet coordinate, and
future out-of-sample performance. The atlas is proposed as an empirical population diagram, not
as a finalized taxonomy or a causal evolutionary model.

1 Introduction

The Hertzsprung–Russell (H–R) diagram is useful because it exposes sequences, turnoffs, evolutionary
states, and diagnostic outliers in a compact observational plane. Exoplanet population studies have
produced several important diagrams, including mass–radius relations, period–radius distributions,
radius-gap maps, and irradiation–radius relations [2, 5, 6, 11]. Each captures part of the population
structure, but no single diagram has become a comparably general organizer of planet structure and
environmental response.
An exoplanet analogue need not use the same kinds of axes as the stellar H–R diagram. Planetary
radius depends simultaneously on bulk mass, envelope fraction, composition, thermal state, irradiation
history, and age. A useful diagram should therefore separate control variables from the response
field. The analysis developed here identifies planet mass and bolometric incident flux as the most
informative two-dimensional control plane, with radius as the displayed response and host metallicity
as a composition-sensitive residual coordinate.
The most compact representation of this structure is the Exoplanet Radius–Response Atlas. It
folds mass and irradiation into one horizontal coordinate while retaining planet radius vertically. The
resulting chart reveals both the low-mass and giant-planet sequences, while the full mass–irradiation
diagram explains the response turnover that creates those sequences.

## Page 2

2 Data and search methodology

2.1 Catalog and precision cuts

The source catalog is the NASA Exoplanet Archive Planetary Systems table [1], restricted to transiting
planets and the archive-selected default solution for each object. The query returned 4,731 rows. Seven
controversially flagged entries were removed before feature construction. The principal analysis sample
comprises 1,217 planets satisfying all of the following conditions:
• measured planet mass and radius;
• fractional mass uncertainty no greater than 50%;
• fractional radius uncertainty no greater than 20%; and
• a measured or consistently derived bolometric incident flux.
Host metallicity is available for 1,141 of these planets. Incident flux was derived uniformly from
stellar radius, effective temperature, stellar mass, and orbital period when those inputs were available;
the archive flux value was used as a fallback. The analysis is therefore a study of the published
mass-measured transiting sample, not an occurrence-corrected census.

2.2 Parameter-space screen

The search included direct and transformed quantities describing planet mass, radius, period, irradiation,
equilibrium temperature, density, surface gravity, orbital scale, stellar properties, and composition. It
comprised three complementary screens:
1. all 190 eligible two-parameter projections;
2. all 1,365 eligible four-parameter combinations; and
3. 165 response surfaces in which radius was modeled using every three-variable combination drawn
from upstream controls.
Derived quantities containing planet radius were excluded from the radius-response search to prevent
target leakage. Algebraically redundant clusterings—for example, combinations of mass, radius,
density, gravity, and escape speed—were not treated as discoveries even when they produced visually
compact groups. The primary criterion was whether a projection preserved non-tautological population
structure and improved out-of-sample radius prediction.

2.3 Piecewise response model

The selected response family is
log10(
Rp
R⊕
)
= aj + bM,j log10( Mp
M⊕
)
+ bF,j log10(
F⋆
F⊕
)
+ bZ,j [Fe/H], (1)
where j denotes the low-mass or giant response branch. Candidate break masses were evaluated by
information criteria, host bootstrap, measurement-error perturbation, and host-grouped prediction.
The data support a broad transition band rather than a sharp universal boundary.

## Page 3

3 The Exoplanet Radius–Response Atlas

The collapsed coordinate is
I0.4 =
(
F⋆
F⊕
) ( Mp
M⊕
)−0.4
. (2)
The exponent is an empirical approximation to the giant-planet inflation ridge: more massive giant
planets require greater forcing to occupy the same radius sequence. Giant-only cross-validation favors
exponents near 0.45–0.50; the rounded value 0.4 provides a stable and interpretable projection. Both
axes of the atlas are logarithmic.
10
2 10
1 10
0 10
1 10
2 103 10
4
Mass-corrected irradiation, 0.4 = (F/F )(M/M )
0.4
10
0
10
1
Pla
n
et ra
diu
s, R
p/R
The fold is nearly sufficient for massive giants, but not for low-mass planets
A high-forcing compact/eroded
B moderate-forcing sub-Neptune
C cool giant shelf
D warm compact giants
E hot inflated giants
A
B
C
D
E
Collapsed exoplanet response diagram: five empirical zones
Figure 1: The Exoplanet Radius–Response Atlas. Planet radius is plotted against the mass-corrected irradiation
coordinate defined in Eq. (2). Five empirical zones summarize the observed morphology. The fold is nearly
sufficient for the giant inflation sequence but does not remove the independent importance of mass, envelope
fraction, and composition among low-mass planets.
The atlas in Fig. 1 separates five empirical zones. Their descriptive medians are given in Table 1.
These zones are population concentrations rather than hard class boundaries. Four- and five-component
Gaussian-mixture descriptions are nearly tied by Bayesian information criterion, and the cool giant
shelf is the least secure independent component. Host-bootstrap stability of the five-zone assignment
has a median adjusted Rand index of 0.79, with a 5–95% range of 0.65–0.92.
Zone A contains compact planets under strong present-day forcing and is consistent with a mixture
of rocky planets, stripped cores, and planets with thin surviving envelopes. Zone B contains the
broader sub-Neptune population. Zones C–E trace the giant-planet sequence from weakly irradiated,

## Page 4

Table 1: Empirical zones in the collapsed atlas. Values are sample medians and should not be interpreted as
defining boundaries.
Zone Description N Mp/M⊕ Rp/R⊕ F⋆/F⊕ P (d) ρ (g cm−3)
A high-forcing compact/eroded 221 6.4 2.02 209.9 4.6 4.51
B moderate-forcing sub-Neptune 286 10.7 3.16 31.8 10.7 2.03
C cool giant shelf 74 196.5 9.59 7.5 78.6 0.91
D warm compact giants 197 246.0 11.07 138.6 5.2 0.97
E hot inflated giants 439 311.5 14.46 1063.2 3.4 0.55
approximately Jupiter-sized planets to strongly irradiated, inflated giants. The atlas is most effective
as a morphology map; the full control plane is required to identify the response changes that produce
the morphology.

4 The full mass–irradiation response field

Figure 2 displays the parent diagram: planet mass versus bolometric incident flux, with radius
encoded by color. The broad transition between the low-mass and giant branches is centered near
Saturn/sub-Saturn masses.

## Page 5

10
1 10
0 10
1 10
2 103 10
4
Planet mass, Mp/M
10
1
10
0
10
1
10
2
10
3
10
4
B
olo
m
etric in
cid
e
nt flu
x, F /F
selected break

79 M

LOW-MASS BRANCH
irradiation radius
metallicity radius (10 30 M )
GIANT BRANCH
irradiation radius
metallicity radius (fixed M, F)
1,217 transiting planets with mass and radius precision cuts; point color is radius
radius-response turnover band
0.5
1.0
2.0
4.0
8.0
12.0
16.0
24.0
Pla
n
et ra
diu
s, R
p/R
Exoplanet Radius-Response Phase Diagram
Figure 2: The Exoplanet Radius–Response Diagram. Planet mass and incident flux are the control coordinates;
planet radius is the response field. The gray interval represents the broad response-turnover region supported
by resampling, and the dashed line marks the selected break near 79 M⊕.
At a fixed break of 80 M⊕, the branch coefficients are listed in Table 2. Three changes occur across
the transition:
1. the radius response to mass decreases from a steep positive slope to a value statistically consistent
with zero;
2. the radius response to irradiation changes from negative to positive; and
3. the metallicity response changes from a localized positive association in the 10–30 M⊕ interval to
a negative association among giant planets.
The coefficients have direct effect-size interpretations. On the low-mass branch, a factor of ten
increase in incident flux corresponds to an 8.9% decrease in radius at fixed mass and metallicity.
On the giant branch, the same flux increase corresponds to a 17.8% increase in radius. Within the
10–30 M⊕ subset, a +0.5 dex metallicity difference corresponds to a 25.5% larger radius at fixed mass
and flux; above 80 M⊕, the corresponding change is an 8.5% smaller radius.
The moving-window fits in Fig. 3 show that these changes are gradual. The irradiation coefficient
becomes securely positive near the Saturn-mass regime, the metallicity coefficient becomes negative at

## Page 6

Table 2: Host-clustered coefficients for Eq. (1). The 10–30 M⊕ row is a diagnostic subset of the low-mass
branch.
Regime N bM pM bF pF bZ pZ
Mp < 80 M⊕ 509 +0.527 1.9 × 10−163 -0.040 3.4 × 10−6 +0.048 0.186
10–30 M⊕ 149 +0.657 1.3 × 10−15 -0.039 0.048 +0.197 0.0045
Mp ≥ 80 M⊕ 632 +0.005 0.531 +0.071 1.2 × 10−66 -0.077 6.2 × 10−9
a somewhat lower mass, and the mass coefficient approaches the giant-planet radius plateau over a
broad mass interval. The term response turnoff is therefore more appropriate than a discrete class
boundary.
0.2
0.0
0.2
0.4
0.6
0.8
coefficient
growth with mass
radius plateau
Mass response logR/ log M
0.10
0.05
0.00
0.05
0.10
coefficient
irradiation shrinks/strips
irradiation inflates
Irradiation response logR/ log F
10
1 10
2 103
Median planet mass in overlapping 180-planet window, Mp/M
0.2
0.1
0.0
0.1
0.2
0.3
coefficient
metal-rich hosts: larger
metal-rich hosts: smaller
Host-metallicity response logR/ [Fe/H]
A three-response turnover: mass, irradiation and metallicity change roles
Shading: host-clustered 95% intervals. Gray band: 50 100 Earth-mass transition region.
Figure 3: Mass-dependent response coefficients estimated in moving 180-planet windows. Shaded intervals are
host-clustered 95% confidence intervals. The broad turnover consists of a collapse in the mass coefficient, an
irradiation sign reversal, and a metallicity sign reversal.

## Page 7

5 Validation and robustness

5.1 Breakpoint stability

The selected break is not an exact physical constant. Host bootstrap resampling gives a median of
79.1 M⊕ and a 95% interval of 53.2–101.2 M⊕. Measurement-error perturbations give a median of
74.8 M⊕ and a 95% interval of 56.6–88.0 M⊕. These distributions are shown in Fig. 4.
50 60 70 80 90 100 110
Selected mass breakpoint, Mp/M
0.00
0.02
0.04
0.06
0.08
0.10
0.12
0.14
density
The response turnover is broad, but it repeatedly lands near Saturn/sub-Saturn mass
host bootstrap (selection + host dependence)
measurement-error Monte Carlo
host-bootstrap median 79.1 Earth masses
Figure 4: Breakpoint stability under host bootstrap resampling and measurement-error perturbation. Both
analyses support a broad Saturn/sub-Saturn transition rather than a unique, sharply determined mass.

5.2 Out-of-sample prediction

One hundred host-grouped train/test splits were used to prevent planets around the same star from
appearing in both training and test sets. The global mass–flux–metallicity model achieved a mean
held-out radius RMSE of 0.1610 dex. The fixed-80 M⊕ two-branch model achieved 0.1005 dex, a mean
reduction of 37.6%. When the break was reselected within each training set, the piecewise model
outperformed the global model in every split; the median training-selected break was 82.6 M⊕.
The principal coefficient directions also persist in Kepler, K2, TESS, ground-discovered, radial-velocity-mass, FGK-host, and discovery-era subsets where the sample size is adequate. They remain
under direct archive fluxes, additional stellar controls, facility and mass-method fixed effects, radius-error weighting, and Huber robust regression. A metallicity permutation test stratified by discovery
facility and stellar-mass quintile gives p = 0.00166 for the observed low- versus high-mass metallicity-slope contrast.

5.3 Comparison with alternative diagrams

The mass–irradiation plane ranked first in a common projection benchmark for the latent state
(Rp, Mp, F⋆, [Fe/H]). Its mean information score was 0.858, compared with 0.853 for metallicity–radius,

## Page 8

0.848 for radius–irradiation, 0.830 for the collapsed atlas, and 0.802 for mass–radius. The benchmark
combines neighborhood trustworthiness, reverse continuity, distance-rank preservation, and out-of-fold
recovery of a common coarse partition. It is a comparative diagnostic rather than a likelihood.
The leading response surfaces are shown in Fig. 5. Several alternatives involving orbital geometry
or stellar temperature are statistically close to the selected model. The claim therefore rests on the
stability of the response topology and its predictive gain, not on a uniquely dominant set of covariates.
0 200 400 600 800 1000
BIC improvement of best broken response surface over one global plane
logM, logMstar, logAoverRstar
logM, logS, logRstar
logM, logS, multiplicity
logM, logS, logMstar
logM, Teff_kK, logAoverRstar
logM, logS, Teff_kK
logM, logS, logP
logM, logP, logMstar
logM, logP, Teff_kK
logM, FeH, logAoverRstar
logM, logS, logAoverRstar
logM, logS, FeH
Several orbit-geometry alternatives are statistically close.
1038
1042
1050
1051
1052
1052
1053
1055
1059
1059
1061
1063
Wide four-parameter search: mass irradiation metallicity is the narrow leader
Figure 5: Leading four-variable radius response surfaces. The mass–irradiation–metallicity surface is the
narrow information-criterion leader, while several orbital-geometry alternatives are close.

6 Falsifiable predictions

The atlas and the full response field imply the quantitative tests in Table 3. Predictions P1–P6 follow
directly from the fitted response topology. P7 and P8 test whether the atlas also captures population
structure beyond the regression coefficients.
Table 3: Falsifiable predictions derived from the Exoplanet Radius–Response Atlas.
ID Prediction Quantitative test Failure criterion
P1 Low-mass irradiation response In a homogeneous sample of
approximately 5–30 M⊕ planets, the conditional coefficient
∂ log Rp/∂ log F⋆ should be negative, with a target value near
−0.04.
A common-pipeline sample
yields a non-negative low-mass
coefficient after controlling for
mass and host composition.

## Page 9

Table 3: Falsifiable predictions derived from the Exoplanet Radius–Response Atlas (continued).
ID Prediction Quantitative test Failure criterion
P2 Giant-planet irradiation response Above approximately 150 M⊕, the
conditional irradiation coefficient
should be positive and near +0.07,
corresponding to roughly 18%
greater radius per decade in flux.
The giant-branch coefficient is
consistent with zero or negative
in a large homogeneous sample.
P3 Collapse of the mass response The radius–mass coefficient
should decrease from at least 0.4
below the transition to less than
0.05 on the giant branch.
The giant branch retains a substantial positive mass slope, or
the low- and high-mass slopes
become statistically indistinguishable.
P4 Metallicity sign reversal The 10–30 M⊕ population should
have a positive conditional metallicity coefficient, while giant planets should have a negative coefficient.
Homogeneous stellar spectroscopy yields the same
sign in both mass regimes or
eliminates the slope contrast.
P5 Location of the response
turnoff
Moving-window or hierarchical
varying-coefficient fits should
place the irradiation zero crossing
and mass-slope collapse within a
broad 50–100 M⊕ interval.
The transition is absent, or
its center lies outside approximately 30–150 M⊕ after selection effects are modeled.
P6 Sufficiency of the giant-planet foldFor giant planets, a model based
on I0.4 and metallicity should capture most radius variation; an additional free mass term should
provide little held-out improvement. The preferred folding exponent should remain within approximately 0.35–0.55.
Explicit mass substantially improves giant-only prediction, or
the preferred exponent moves
well outside the stated interval.
P7 Persistence of the cool giant
shelf
New low-irradiation transiting
and radial-velocity-mass giants
should continue to concentrate
near 9–10 R⊕ rather than filling
the atlas uniformly.
A larger homogeneous sample
turns Zone C into a smooth, featureless continuation of Zones
D and E.
P8 Predictive replication In a future independent sample, a
branch-dependent response model
should reduce host-grouped radius
RMSE by at least 20% relative to
one global mass–flux surface.
The piecewise or smoothly varying model provides no meaningful out-of-sample improvement.
A particularly discriminating extension is to replace present-day bolometric flux with reconstructed
time-integrated XUV exposure. Atmospheric-loss interpretations predict that this substitution should
strengthen the negative low-mass response, whereas giant-planet inflation should remain tied more
closely to present-day bolometric forcing. Failure to separate those dependencies would favor a common
selection or formation explanation over two distinct evolutionary mechanisms.

## Page 10

7 Physical interpretation and relation to prior work

The response turnover is consistent with a transition between two radius-governing regimes. Below the
turnover, radius is strongly mass-sensitive and the negative flux coefficient is compatible with envelope
loss, inhibited retention, or correlated survival selection. The localized positive metallicity signal at
10–30 M⊕ may reflect larger cores, larger primordial envelopes, or greater resistance to atmospheric
loss in metal-rich systems [7, 8]. The association is not significant when all planets below 80 M⊕ are
combined, so it should not be interpreted as a universal low-mass metallicity law.
Above the turnover, radius becomes nearly independent of total mass in the aggregate population.
Irradiation-driven inflation and heavy-element loading can therefore dominate the residual radius
variation. Positive giant-planet irradiation responses and negative metallicity responses are consistent
with multivariate studies of hot-Jupiter radii and giant-planet enrichment [3, 9, 10].
The irradiation sign reversal itself has precedent. Weiss et al. [11] fitted opposite incident-flux
exponents below and above a substantially higher, visually selected mass boundary. Structural mass–
radius studies also identify transitions in the Saturn-mass neighborhood [2, 4, 5]. The distinctive
contribution of the atlas is the joint organization of three effects—mass-slope collapse, irradiation sign
reversal, and metallicity sign reversal—within one broad response turnoff.
The atlas is not an evolutionary track for individual planets. Migration, cooling, mass loss, tidal
heating, formation location, and survey selection can all move or select objects in the underlying
control space. The diagram should therefore be interpreted as an empirical population response field
whose causal decomposition remains to be established.

8 Limitations

The analysis is subject to several limitations:
• the sample is not corrected for transit detection, mass-measurement follow-up, or publication
selection;
• planet and stellar parameters are heterogeneous literature measurements with non-uniform covariance information;
• host metallicities are drawn from multiple spectroscopic scales;
• bolometric incident flux is an imperfect proxy for atmospheric escape, which depends strongly on
stellar XUV history;
• ages are incomplete and imprecise for many systems; and
• the parameter-space screen creates an exploratory multiplicity burden, even though validation was
performed on the selected response family.
The central result would require substantial revision if a homogeneous, selection-modeled sample
removed the low- versus high-mass irradiation contrast, eliminated the metallicity sign reversal, or
failed to recover a broad transition in the Saturn/sub-Saturn mass range.

9 Conclusions

The Exoplanet Radius–Response Atlas provides a compact view of the current mass-measured transiting
population. Its five empirical zones summarize the progression from compact irradiated planets and
sub-Neptunes to cool, warm, and inflated giants. The atlas is generated by a more fundamental

## Page 11

mass–irradiation response field in which three radius sensitivities reorganize across a broad 50–100 M⊕
transition: the mass coefficient collapses, the irradiation coefficient changes sign, and the metallicity
coefficient changes from a localized positive association to a negative giant-planet association.
The diagram is useful because it is both descriptive and falsifiable. It predicts branch-specific
irradiation slopes, a metallicity sign reversal, a bounded transition mass, approximate sufficiency of
the giant-planet folding coordinate, and measurable out-of-sample gains over a global response surface.
Independent recovery of those features in homogeneous, occurrence-aware samples would support the
atlas as an H–R-like organizing diagram for exoplanets. Their failure would define how the diagram
must be revised.
Data and code availability
The archive snapshot, feature-construction scripts, parameter-space screens, validation outputs, figures,
and planet-level atlas table are contained in the accompanying reproducibility bundle. The NASA
Exoplanet Archive query was
select * from ps where tran_flag=1 and default_flag=1 order by pl_name
The query was executed on 24 August 2026.

References

[1] Akeson, R. L., Chen, X., Ciardi, D., et al. 2013, “The NASA Exoplanet Archive: Data and Tools for
Exoplanet Research,” Publications of the Astronomical Society of the Pacific, 125, 989.
[2] Chen, J., & Kipping, D. 2017, “Probabilistic Forecasting of the Masses and Radii of Other Worlds,” The
Astrophysical Journal, 834, 17.
[3] Enoch, B., Collier Cameron, A., & Horne, K. 2012, “Factors Affecting the Radii of Close-in Transiting
Exoplanets,” Astronomy & Astrophysics, 540, A99.
[4] Hatzes, A. P., & Rauer, H. 2015, “A Definition for Giant Planets Based on the Mass–Density Relationship,”
The Astrophysical Journal Letters, 810, L25.
[5] Müller, S., Otegi, J. F., Hoyer, S., et al. 2024, “The Mass–Radius Relation of Exoplanets Revisited,”
Astronomy & Astrophysics, 686, A296.
[6] Neil, A. R., & Rogers, L. A. 2020, “A Joint Mass–Radius–Period Distribution of Exoplanets,” The
Astrophysical Journal, 891, 12.
[7] Owen, J. E., & Murray-Clay, R. 2018, “Metallicity-dependent Signatures in the Kepler Planets,” Monthly
Notices of the Royal Astronomical Society, 480, 2206.
[8] Petigura, E. A., Isaacson, H., Marcy, G. W., et al. 2022, “The California–Kepler Survey. X. The Radius
Gap as a Function of Stellar Mass, Metallicity, and Age,” The Astronomical Journal, 163, 179.
[9] Sestovic, M., Demory, B.-O., & Queloz, D. 2018, “Investigating Hot-Jupiter Inflated Radii with Hierarchical
Bayesian Modelling,” Astronomy & Astrophysics, 616, A76.
[10] Thorngren, D. P., Fortney, J. J., Murray-Clay, R. A., & Lopez, E. D. 2016, “The Mass–Metallicity Relation
for Giant Planets,” The Astrophysical Journal, 831, 64.
[11] Weiss, L. M., Marcy, G. W., Rowe, J. F., et al. 2013, “The Mass of KOI-94d and a Relation for Planet
Radius, Mass, and Incident Flux,” The Astrophysical Journal, 768, 14.
