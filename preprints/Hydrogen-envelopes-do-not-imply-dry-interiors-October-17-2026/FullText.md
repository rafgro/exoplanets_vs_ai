## Page 1

Hydrogen envelopes do not imply dry interiors:
conditional water constraints for young sub-Neptunes
Anonymous
Draft preprint - 17 October 2026
Numerical analysis frozen on 15 October 2026

ABSTRACT

The inflated radii of young planets can distinguish a light-gas envelope from a pure-steam envelope without
establishing whether the underlying planet is water-poor. We quantify this distinction in five benchmarks:
TOI-2076 b, c and d, and V1298 Tau c and d. We compare a steam-cooling grid with dry and water-bearing
H/He models evaluated through published BICEPS/plaNETic surrogates, and recycle released joint JWST
retrieval samples for V1298 Tau c. Under the baseline priors, mass-radius data give water-rich/dry evidence
ratios of 0.54-1.61 and broad conditional 95% bulk-water intervals extending to 37-49% by mass. At the central
properties of TOI-2076 c, both a nearly dry planet containing 4.0% H/He and a planet containing 30% water plus
9.2% H/He reproduce the radius. Conditioning the V1298 Tau c spectral posterior on its dynamical mass raises
the median atmospheric water volume fraction from 1.5% to 9.4% with informed stellar priors. The
corresponding fully mixed interior has a median water fraction of 16.3% and a 95% interval of 1.5-40.1%.
However, evidence for at least 10% water over a less-than-1%-water alternative is only 1.9:1; flexible stellar
priors increase this ratio to 23:1. Steam discrimination is sensitive to structural error and thermal prescriptions.
These exploratory, model-conditional results favor H/He in the most inflated benchmarks but do not yield a
model-independent bulk-water bound or a population water-rich fraction. Atmospheric-interior partitioning
remains an unresolved physical degree of freedom.
Keywords: planets and satellites: composition - interiors - atmospheres - individual: TOI-2076, V1298 Tau - methods: statistical

1. Introduction

A compositional inference from a planet's radius must separate two questions: does the planet require a
low-density envelope, and how much water does the whole planet contain? A refractory planet with H/He, a
water-dominated planet without H/He, and a water-bearing planet that also retains H/He are physically distinct
hypotheses. Comparing only the first two can turn evidence for light gas into an unjustified inference of a dry
interior. Joint water-H/He structure models already demonstrate that these alternatives can overlap in
observable space [1,2].
Young systems offer a useful test because their envelopes are thermally extended and their ages supply
evolutionary information. TOI-2076 has measured small-planet masses at an age near 210 Myr [3]. The much
younger V1298 Tau system contains low-mass planets with unusually large radii [4], and its planet c has a
released JWST transmission-spectrum retrieval [5]. These systems allow structural and atmospheric constraints
to be examined together. Their utility does not remove uncertainty in initial entropy, cooling, atmospheric loss,
host-star heterogeneity or volatile partitioning.
Here we ask what the adopted observations of these five planets constrain about present bulk water when both
water and H/He are allowed. We report conditional evidence ratios, the dependence of water posteriors on
priors, and explicit pairs of observationally degenerate structures. We then update the actual joint atmospheric
samples of V1298 Tau c rather than combining a marginalized abundance error bar with an independent mass
estimate.
This is a targeted reanalysis using existing physical grids and neural surrogates. It is not a new direct interior
solver, hydrodynamic calculation, raw-spectrum retrieval or hierarchical occurrence analysis. Its contribution is

## Page 2

Anonymous Hydrogen envelopes and bulk water in young planets
2
a reproducible quantification of what remains unidentified after adopting these models. Reported water
fractions refer to present H2O-equivalent inventory in the specified structure, not directly to primordial ice
accretion.

2. Observations and scope of the likelihood

Table 1. Benchmark measurements used for the structural comparison.
Planet Mass / M⊕ Radius / R⊕ T
eq
/ K Adopted age
TOI-2076 b 6.7 ± 1.8 2.59 ± 0.10 736 ± 16 210 ± 20 Myr
TOI-2076 c 7.2 ± 1.4 3.54 ± 0.14 581 ± 13 210 ± 20 Myr
TOI-2076 d 7.3 ± 2.7 3.27 ± 0.13 490 ± 11 210 ± 20 Myr
V1298 Tau c 4.7 ± 0.6 5.08 ± 0.37 953 ± 36 10-30 Myr
V1298 Tau d 6.0 ± 0.7 6.53 ± 0.42 831 ± 31 10-30 Myr
V1298 Tau mass errors summarize the measurements; the fit uses the released joint TTV mass-ratio samples. Sources: Wang et al.
[3] and Livingston et al. [4]. Gaussian approximations are used for TOI-2076.
The V1298 Tau mass input consists of 8,000 joint transit-timing-variation (TTV) samples [9]. Planet order is
retained as c, d, b, e. Mass ratios are converted using a stellar mass of 1.10 ± 0.05 M☉. Individual fits use the
corresponding marginal distribution and propagate the stellar-mass uncertainty. The archive retains interplanet
correlations, but we do not multiply individual evidences into a system or population probability. Radii and
stellar scale follow Livingston et al. [4].
For TOI-2076, mass, radius, equilibrium-temperature and age summaries are approximated by independent
Gaussian distributions. Their complete covariance is not reconstructed. Common stellar errors could correlate
several quantities, so this is a limitation. We do not combine measurements derived under different stellar
solutions. The reported fit is conditional on the scale in Table 1.
The H/He surrogate calculation is restricted to 0.5-15 M⊕. V1298 Tau b and e are omitted because their broad
mass distributions extend beyond the adopted coverage. The sample is selected for available constraints and
model compatibility, not by an occurrence-survey selection function. V1298 Tau d exceeds a conventional
present-day sub-Neptune radius range; it is included as an inflated low-mass benchmark and possible
progenitor.

2.1. Information used, and information not fitted

The three-way structural comparison uses mass, radius, irradiation and the declared thermal assumptions. It
does not include helium-line measurements, escape rates, detailed spectra or formation-track likelihoods. Wang
et al. [3] discuss reported metastable-helium outflows as evidence against a strictly pure-water interpretation. A
nonzero steam weight below therefore means that a steam model fits the adopted structural likelihood; it is not a
probability conditional on all observations. Helium evidence can support light gas while leaving total water
unresolved.
The spectrum enters a separate analysis of V1298 Tau c. Its archived retrieval already incorporates a radius
prior, which we retain. We do not multiply by the broader radius constraint in Table 1 a second time. Stellar
treatments are analyzed separately rather than assigned relative probabilities without the original spectral
evidences.

## Page 3

Anonymous Hydrogen envelopes and bulk water in young planets
3

3. Structural models and priors

3.1. Composition coordinates and competing families

Let M be total planet mass, f the H/He mass fraction, and w the H2O-equivalent mass fraction. Refractory
material occupies 1-f-w. We use q to describe the fraction of the non-H/He mass assigned to water:
(1)
In the continuous mixed model, f is log-uniform on [10-6, 0.5] and q is uniform on [0.001, 0.5]. Thus the prior is
not flat in w independently of f. The envelope mass fraction is f+w, and its water mass fraction is w/(f+w).
Water and H/He are uniformly mixed; we do not fit a separate deep water layer. The water-rich class W
conditions this prior on bulk w ≥ 0.10. Intermediate compositions remain in the continuous analysis.
The dry class D has a refractory interior and a nearly solar-composition envelope. Its envelope water mass
fraction is fixed at 0.005, giving w = (0.005/0.995)f. It is a low-water reference, not a mathematically
zero-water planet. For the spectral comparison we also fit a less restrictive alternative allowing total water
below 1%.
The steam-only class S contains an Earth-like refractory interior and a pure-water envelope, with f = 0 and w
uniform on [0.001, 1]. It uses the Aguichine et al. cooling models [6,7], without imposing the mixed model's
50% non-H/He water ceiling. These classes are specified hypotheses, not an exhaustive partition of possible
planets. Equal model priors are used to illustrate their relative weights.

3.2. Forward radii and thermal boundary conditions

For D and W, radii come from the released plaNETic dense-network weights trained on BICEPS [1,2,8]. Inputs
include mass, irradiation, intrinsic luminosity, envelope mass and water fraction, and refractory composition.
Core fraction is uniform from 0.20 to 0.45 of refractory mass. Core sulphur molar fraction is 0.05; mantle
Si/Mg/Fe molar fractions are 0.45/0.45/0.10. These are assumptions, not host-specific abundance
measurements.
The mixed networks A_m1 and A_m2 are used below and above 6 M⊕, respectively; the released low-water B
network is used for D. The pinned author release includes a correction to its low-mass dry weights and is used
as supplied. We evaluate these networks rather than run a new BICEPS solve. Agreement with stored weights
does not establish physical accuracy at every young-planet boundary condition.
For TOI-2076, the age-luminosity mapping distributed with plaNETic is evaluated at 210 ± 20 Myr. Its
tabulated age range is 0.1-1 Gyr. A sensitivity calculation adds a uniform displacement of ±0.5 dex to log10L.
The mapping depends on mass and gas fraction; varying water does not independently recalibrate the cooling
relation. We do not extrapolate it to V1298 Tau.
For V1298 Tau, the headline prior is log10(L/[erg s-1]) uniform on [22, 23.525]. A broader [18, 23.525] interval
tests thermal sensitivity. These are chosen luminosity priors, not heat measurements or calibrated 20-Myr
tracks. Current composition is fitted conditional on thermal state; neither primordial envelope mass nor escape
history is inferred.
The steam comparison interpolates the extended-temperature SWEET release [7] in water fraction, equilibrium
temperature, mass and logarithmic age. We use its G-star irradiation grid and 20-mbar radius. TOI-2076 ages
follow Table 1; V1298 Tau ages are uniform from 10 to 30 Myr. The terminal exhaustion estimate is excluded
from each track before interpolation. The irradiation spectrum and fixed radius pressure are approximations,
especially for a K-type host. The 2026 grid is public, but its associated extension manuscript was listed as in
preparation; the original energetic model is published [6].

## Page 4

Anonymous Hydrogen envelopes and bulk water in young planets
4
Steam and H/He models do not share an identical cooling solver or radius definition. Their comparison tests
composition together with its thermal and atmospheric prescription. Error-floor sensitivity is essential, but
cannot replace a matched calculation of all families in one evolution framework.

4. Statistical inference

4.1. Conditional structural evidence

We condition on published dynamical data Ddyn, using p(M | Ddyn) as a common mass input across
composition families. For model C with remaining parameters θ, the conditional evidence is
(2)
The radius likelihood is Gaussian, centered on the forward radius RC, with measurement variance plus an
assumed fractional model discrepancy:
(3)
These discrepancy values are sensitivity assumptions. The 3% baseline is not a demonstrated total uncertainty
of young-planet structure, and the larger values are not inferred physical error bars. Discrepancy is treated as
independent zero-mean scatter; systematic model bias or correlated error need not be represented by that form.
Samples outside the adopted mass, temperature or luminosity domain, or returning invalid radii, are excluded.
Evidences are normalized over the valid prior subset, so they are conditional on model support. If VC denotes
this subset, the implemented prior is πCI(VC)/P(VC). This matters when families have different admissible
domains: support exclusions are not observational exclusions. Valid fractions are reported in Appendix A.
(4)
The second expression assumes equal prior probabilities for S, D and W. These weights are not population
fractions. Sensitivity tests replace the gas prior with a uniform prior or cap its maximum at 0.1 or 0.2.
Water-poor and water-rich priors multiply the baseline q density by (1-q/0.5)4 and (q/0.5)4, with normalization
recomputed within the valid domain.

4.2. Numerical integration and information gain

Each main family/scenario calculation uses 218 = 262,144 scrambled Sobol draws. Seven planet/thermal
scenarios across three internal branches generate approximately 5.5 million configurations. The full-water
steam grid is evaluated separately. Prior and error-floor sensitivities reuse forward predictions. A targeted
low-water fit uses 217 draws. Posterior quantiles, effective sample sizes and eight-block integration diagnostics
are recorded.
(5)
Here ā denotes normalized numerical weights, and pb and πb are posterior and prior probabilities in 25 equal
bins over w = 0-0.5. Effective sample size describes integration quality, not the number of observations. The
binned divergence is a descriptive prior-relative information measure, not a detection significance or a
prior-independent entropy reduction. Reweighted posteriors are compared with their corresponding priors.

## Page 5

Anonymous Hydrogen envelopes and bulk water in young planets
5

5. Results from mass and radius

5.1. Three-way comparison

Table 2. Illustrative equal-prior structural model weights.
Planet 3% floor: S / D / W (%) 10% floor: S / D / W (%) BWD, 3%
TOI-2076 b 62.56 / 14.32 / 23.12 49.78 / 16.66 / 33.56 1.61
TOI-2076 c 0.03 / 60.04 / 39.93 16.26 / 48.86 / 34.88 0.67
TOI-2076 d 6.44 / 56.18 / 37.38 35.30 / 34.57 / 30.13 0.67
V1298 Tau c <0.01 / 64.89 / 35.11 0.21 / 63.77 / 36.02 0.54
V1298 Tau d <0.01 / 61.95 / 38.05 <0.01 / 61.28 / 38.72 0.61
S: steam-only; D: nearly dry + H/He; W: mixed-envelope model restricted to bulk w ≥ 10%. Weights condition on thermal
prescriptions and valid model support. They omit helium-line and spectral likelihoods.
The baseline W/D evidence ratios are 0.54-1.61. None of the five structural comparisons decisively selects a
dry or water-rich H/He-bearing interior. The largest V1298 Tau radii are difficult to reproduce with the adopted
steam grid, producing small steam weights at the 3% floor. That distinction concerns the requirement for an
extended light envelope within these thermal models, not a measurement of low bulk water.
Steam discrimination depends strongly on the assumed discrepancy. For TOI-2076 c, the dry/steam evidence
ratio decreases from approximately 2,060 at the 3% floor to 3.0 at the 10% floor. For d, all three families have
substantial weight at 10%. TOI-2076 b has a steam solution with median w = 76.5% and a 95% interval of
42.6-98.4%. A 50% water ceiling would eliminate a structural alternative by construction. This does not
override external helium evidence (Section 2.1).
At a 20% discrepancy, steam weights for V1298 Tau c and d rise to 17.3% and 7.6%. It would be misleading to
quote the extreme baseline evidence ratios without this sensitivity. Physical adequacy of cooling and
photospheric-radius prescriptions is more consequential than numerical integration precision.

5.2. Water posteriors and explicit degenerate structures

Table 3. Bulk-water constraints within the continuous mixed family.
Planet Median w (%) 95% interval (%) I
w
(bits)
TOI-2076 b 38.2 3.1-49.4 0.38
TOI-2076 c 23.8 0.9-44.2 0.10
TOI-2076 d 24.8 1.0-45.3 0.07
V1298 Tau c 21.2 0.9-41.0 0.18
V1298 Tau d 16.6 0.7-37.1 0.32
Baseline 3% radius floor and headline V1298 Tau luminosity prior. These are conditional mixed-family intervals, not
model-averaged measurements. Positive lower endpoints do not exclude the dry family. Upper water support is imposed through q
≤ 0.5.
The continuous mixed posteriors span large fractions of the allowed water range. Their approximate
prior-relative water information is only 0.07-0.38 bits. Endpoints approaching 40-50% are not upper limits

## Page 6

Anonymous Hydrogen envelopes and bulk water in young planets
6
independent of the imposed prior. Positive lower endpoints do not constitute water detections: the continuous
family excludes exactly zero water, while the discrete dry model remains competitive.
Figure 1. Forward-model solutions at fixed central measured mass and radius. Left: TOI-2076 with the 210-Myr age-luminosity
mapping. Right: V1298 Tau at illustrative L = 1023 erg s
-1. Changing water can be compensated by H/He. These are evaluations
of the released surrogate, not evolutionary trajectories; small kinks are not evidence of phase transitions.
For each planet we solve for f while fixing central measured mass and radius, and vary w. For TOI-2076 c, a
nearly dry solution requires f ≈ 4.0%, whereas w = 30% requires f ≈ 9.2%. Both reproduce the radius.
Analogous dry/30%-water gas fractions are 0.74%/2.97% for TOI-2076 b and 3.18%/7.63% for d. At L = 1023
erg s
-1, V1298 Tau c and d give 4.01%/13.58% and 11.07%/20.89%, respectively.
In a mixed envelope, water changes molecular weight, opacity and thermal-density structure. Its effect is not
equivalent to increasing a solid core radius beneath an unchanged H/He layer. At fixed mass and external
conditions, the local radius constraint is
(6)
A single radius leaves at least one composition direction unconstrained even if luminosity were fixed, unless
physical priors or another observable remove that freedom. Improved radius precision can narrow the allowed
curve without selecting a unique position along it.

## Page 7

Anonymous Hydrogen envelopes and bulk water in young planets
7

5.3. Dependence on water and gas priors

Figure 2. Prior dependence for representative planets. Dashed curves are alternative priors and solid curves their resulting
posteriors. The V1298 Tau panel uses the broader log-luminosity interval [18, 23.525], rather than the headline interval, to
display sensitivity without restricting heat to its upper range.
For TOI-2076 c, median water changes from 5.2% to 23.8% to 39.6% under water-poor, broad and water-rich
priors. For d the medians are 5.8%, 24.8% and 40.7%. Under the broad thermal prior, V1298 Tau c gives 4.9%,
19.7% and 34.2%. These shifts exceed numerical integration uncertainty. At the 10% radius floor, the
broad-prior water information for TOI-2076 c and d is about 0.04 bits each.
Gas priors can manufacture a strong dry preference. For V1298 Tau d, a log-uniform gas prior with f ≤ 0.5
gives BWD = 0.61. Restricting f ≤ 0.1 reduces it to 0.0089: water-rich solutions need more gas to maintain the
radius. A uniform gas prior over the wider interval gives BWD ≈ 1.24. A gas-retention cap may be a formation
hypothesis, but its effect is not an additional water measurement.

6. Joint atmospheric and interior information for V1298 Tau c

6.1. Recycling the released spectral posterior

The KRONOS archive [5,10] contains 5,912 and 6,162 equally weighted samples for informed and flexible
stellar-heterogeneity priors. Its mass prior is uniform on 1-100 M⊕, and its log10 water-volume-fraction prior is
uniform on [-12, -0.3]. The radius prior is Gaussian, 5.1 ± 0.1 R⊕. Archived radii are in Jupiter units and
converted using 71,492/6,378.2. Mass, radius and abundance are retained jointly.
The independent dynamical constraint is introduced into the original posterior samples using importance
weights
(7)
The denominator is constant inside the original mass support. The dynamical density is a Gaussian mixture over
the actual TTV mass-ratio draws, with widths set by stellar-mass uncertainty. This update inherits the original
atmosphere and nuisance priors. It is not a rerun of the raw spectral likelihood.

## Page 8

Anonymous Hydrogen envelopes and bulk water in young planets
8
Figure 3. Released joint spectral samples and dynamical-mass update. Left: the informed-stellar retrieval has mass-log-water
correlation -0.63. Right: conditioning on mass changes water for both stellar treatments. Dashed curves show the original
retrieval and solid curves the reweighted result. Smoothing is for display only.
Table 4. Atmospheric H2O volume fraction before and after conditioning on mass.
Stellar prior Original median X (%) Updated median X (%) Updated 68% interval (%) Neff
Informed 1.48 9.4 3.5-16.5 621
Flexible 2.50 23.0 13.8-34.7 284
X is a volume fraction, not a fraction of planetary mass. Effective sample size measures numerical overlap between the existing
retrieval and dynamical constraint.
Mass-log-water correlations are -0.63 and -0.66 for informed and flexible stellar treatments. The informed
median water volume fraction shifts from 1.48% to 9.4%, with 68% interval 3.5-16.5%. The flexible treatment
gives 23.0%, with 68% interval 13.8-34.7%. At lower gravity, the same modulation can require higher
molecular weight, or changes in temperature and aerosols. The archive contains these covariances; independent
Gaussian abundance errors would discard them.
Importance effective sample sizes are 621 and 284. Bootstrap resampling places the informed median log
abundance within [-1.050, -0.984] and the flexible median within [-0.667, -0.609] at 95% numerical confidence.
This measures Monte Carlo stability of the update, not a new observational uncertainty or validation of stellar
modeling.

6.2. Connecting atmospheric abundance to the mixed interior

We approximate the original joint density in x = log10X(H2O), M and R by a three-dimensional Gaussian
kernel mixture. A radius-discrepancy variance (ε × 5.1 R⊕)2 is added to the radius covariance. Bandwidth
multipliers 0.6, 1 and 1.4 test the density approximation. Interior samples drawn with the dynamical mass
distribution are evaluated against this original joint density; the mass-reweighted density is not applied again.
(8)
Equation (8) maps the mixed model to a two-component H2O-H/He number fraction, with H/He mean
molecular weight 2.35. Trace retrieved species are included in the atmospheric water/HHe mass ratios, but are

## Page 9

Anonymous Hydrogen envelopes and bulk water in young planets
9
not separate bulk constituents in this interior model. The mapping assumes atmospheric abundance represents
the entire mixed envelope.
The original mass and log-abundance priors are constant and cancel in within-retrieval composition ratios. The
radius prior is retained. The integrated quantity is the original normalized spectral posterior density evaluated
on the structure model, weighted by the dynamical mass density and composition prior. It is proportional to a
spectral likelihood marginalized under the original nuisance priors, multiplied by the retained radius prior. It
does not recover raw spectral evidence.
These normalized-density integrals cannot rank informed versus flexible stellar models: the omitted raw
spectral normalization constants differ. The archive's H2/He background and molecular-abundance ceiling X ≤
0.5 also prevent a fair pure-steam test at X = 1. We therefore do not report a spectral steam Bayes factor.
Figure 4. Conditional water intervals for the structural sample and V1298 Tau c spectral-interior fits. Thin and thick segments
show 95% and 68% intervals; dots mark medians. Every row conditions on the continuous mixed-envelope family. A positive
endpoint does not exclude the separate dry family.
Table 5. Spectrum-plus-structure constraints with the headline young heat prior.
Stellar prior Bulk water median [95%] (%) H/He median [95%] (%) BW,L
Informed 16.3 [1.5-40.1] 11.1 [4.2-17.7] 1.86
Flexible 27.2 [4.7-41.4] 13.6 [6.0-18.3] 22.99
BW,L compares ≥10% bulk water with a separate <1%-water alternative. Quantiles refer to the continuous mixed model; the
evidence ratio uses the restricted classes. Baseline ε = 0.03 and bandwidth multiplier 1.
The informed fit gives median w = 16.3% and 95% interval 1.5-40.1%; the flexible fit gives 27.2% and
4.7-41.4%. Median H/He fractions are 11.1% and 13.6%. At a 10% radius floor, median water changes to 16.6%

## Page 10

Anonymous Hydrogen envelopes and bulk water in young planets
10
and 26.6%. Stability within a fixed atmospheric-interior mapping does not account for uncertainty in that
mapping.

6.3. A low-water alternative is a more informative comparison

A dry rocky interior does not require an exactly solar-composition atmosphere. We therefore fit a low-water
model L with w uniform on [10-6, 0.01], retaining the gas and young-luminosity priors. The low-water
surrogate is used where envelope water mass fraction is ≤1%; elsewhere the mixed surrogate is used. This
calculation has 131,072 samples and baseline effective sample sizes 353 and 315.
Against L, the continuous mixed model gives evidence ratios 2.18 and 20.12 for informed and flexible stellar
treatments. Restricting the numerator to bulk w ≥ 0.10 gives 1.86 and 22.99. Bandwidth sensitivity changes the
continuous ratios to 1.76-2.63 and 11.83-32.84. At a 10% radius floor they are 2.01 and 18.75. The preference is
conditional on both stellar treatment and the low-water competitor.
A fixed solar-water envelope is a narrow null model. Rejecting it does not establish that at least one tenth of the
planet is water. The lower bounds in Table 5 must be interpreted alongside these alternative-model comparisons
and the assumption of uniform mixing.

7. Physical interpretation and limitations

7.1. Atmospheric enrichment versus bulk water

A transmission spectrum measures atmospheric abundances under a retrieval model. A total inventory requires
a relation between observable atmosphere and interior. For an idealized H/He-water mixture,
(9)
Using the mass-updated samples and subtracting all six retrieved molecular species from the background
number fraction gives a median visible water/HHe mass ratio of 0.79, with 68% interval 0.27-1.51, for the
informed case. The flexible case gives 2.30 and 1.24-4.07. Neither is the planet's total water mass fraction.
If only a fraction η of total water participates in the observable reservoir, the abundance ratio instead constrains
approximately
(10)
A ratio of 0.79 with f = 0.10 corresponds to w ≈ 0.079 when η = 1, but w ≈ 0.395 when η = 0.2. These are
identifiability examples, not additional fitted equilibrium structures. Sequestration also changes density,
chemistry and cooling and must be treated self-consistently. Coupled thermal-chemical models motivate such a
treatment [11].
The fits do not provide a model-independent upper bound on all interior water. They constrain a particular
mixed volatile reservoir over finite prior support. An interpretation of primordial ice acquisition requires
chemical and evolutionary assumptions: atmospheric hydrogen, present H2O-equivalent mass and formation
beyond an ice line are not interchangeable observables.

7.2. Sources of systematic uncertainty

Thermal modeling. The youngest planets are structurally fitted with free luminosity, not evolved from
formation. Luminosity priors couple to gas and water. Steam uses a separate cooling grid and a specified
pressure-level radius. Matched cooling and atmospheric calculations are required before extreme evidence
ratios can be physically calibrated.

## Page 11

Anonymous Hydrogen envelopes and bulk water in young planets
11
Emulator and composition. Checks validate evaluation of released weights and consistency of roots, not
accuracy against direct interiors over every corner. The mixed/dry switch, extreme envelope compositions and
fixed refractory abundances introduce uncertainty. Broad gas and water priors are computational choices, not an
established formation distribution.
Covariance and stellar effects. TOI-2076 errors are Gaussianized and stellar covariance is incomplete. V1298
Tau results condition on one stellar scale. Stellar-heterogeneity priors change atmospheric water and
composition evidence. A future joint model should propagate stellar nuisance parameters into dynamical
conversion and transit spectra rather than assume independence.
Posterior recycling. Kernel smoothing retains a projected three-dimensional density and inherits source
nuisance priors. It is not a new chemical or cloud model fitted to raw spectra. Effective sample size quantifies
finite overlap with the dynamical mass; bandwidth tests probe a numerical approximation. Neither validates
atmosphere models absent from the original retrieval.
Population inference. Five selected benchmarks do not determine the water-rich fraction of young planets. No
survey completeness function, population mixture, shared formation history or interplanet composition
correlation is fitted. More numerical samples cannot remedy this limitation.

7.3. A discriminating next calculation

The immediate test is a raw-spectrum retrieval jointly conditioned on dynamical constraints, with stellar
contamination marginalized and consistent radius priors. Carbon-bearing molecules and broader wavelength
coverage would test the chemical mapping rather than only the water feature. Interior models should permit
water-H/He partitioning and be checked directly against the surrogate at surviving compositions.
Intrinsic-luminosity constraints, if obtainable, would remove part of the structural degeneracy. More precise
radius alone cannot resolve the null direction in Figure 1.

8. Conclusions

We compared steam-only, nearly dry H/He-bearing and water-rich H/He-bearing hypotheses for five young
low-mass planets, and combined the released V1298 Tau c atmospheric posterior with dynamical information.
Four conclusions follow within the declared models.
(1) The mass-radius likelihood distinguishes extended light envelopes from the adopted steam models more
effectively than it distinguishes dry from wet H/He-bearing planets. Water-rich/dry evidence ratios of 0.54-1.61
do not select either interior class. Steam discrimination depends on the discrepancy and thermal prescription.
(2) Water content is prior-sensitive and admits explicit alternatives with tens of percent water. TOI-2076 c
reproduces its central properties with either approximately 4.0% H/He and a nearly dry interior or 30% water
plus approximately 9.2% H/He. Conditional intervals do not provide prior-independent water upper bounds.
(3) Atmospheric abundance must be combined with mass through their joint distribution. Updating V1298 Tau
c with its dynamical mass raises the informed-stellar median atmospheric water from 1.5% to 9.4% by volume.
Evidence for ≥10% bulk water over a <1% alternative is only 1.9:1 under that stellar treatment and 23:1 under
the flexible treatment.
(4) The observable atmosphere does not uniquely determine buried water. H/He retention and substantial water
remain compatible. A decisive bulk-water result requires joint atmospheric, dynamical, thermal and
partition-aware interior inference rather than equating light gas with a dry formation history.

## Page 12

Anonymous Hydrogen envelopes and bulk water in young planets
12
Data and code availability
All inputs are public and identified in the accompanying reproducibility bundle. It contains analysis scripts,
numerical summaries, figures, input URLs and SHA-256 checks. Approximately 569 MB of neural weights are
fetched from the pinned author release rather than redistributed in the compact bundle. Figures derive from the
frozen analysis; no new observations were obtained. Source archives retain their licenses and attribution. No
public archival identifier has been assigned to this reanalysis.
Acknowledgements and preparation statement
This work uses the openly released models and posterior samples of the cited authors. The manuscript and
computational reanalysis were prepared with OpenAI Codex assistance. Authorship is anonymized at the
requester's direction. This is an unsubmitted, unreviewed draft; no independent external validation is claimed.

References

[1] Egger, J. A., Osborn, H. P., Kubyshkina, D., et al. (2024). Unveiling the internal structure and formation history of the three
planets transiting HIP 29442 (TOI-469) with CHEOPS. Astronomy & Astrophysics, 688, A223.
doi:10.1051/0004-6361/202450472.
[2] Haldemann, J., Dorn, C., Venturini, J., Alibert, Y., & Benz, W. (2024). BICEPS: An improved characterization model for low-and intermediate-mass exoplanets. Astronomy & Astrophysics, 681, A96. doi:10.1051/0004-6361/202346965.
[3] Wang, M.-T., Dai, F., Liu, H.-G., et al. (2026). An adolescent and near-resonant planetary system near the end of
photoevaporation. Nature Astronomy. doi:10.1038/s41550-026-02795-9.
[4] Livingston, J. H., et al. (2026). A young progenitor for the most common planetary systems in the Galaxy. Nature.
doi:10.1038/s41586-025-09840-z.
[5] Murphy, M. M., Nixon, M. C., Feinstein, A. D., et al. (2026). KRONOS I: The 1-2.8 μm JWST transmission spectrum of the 23
Myr V1298 Tau c. The Astronomical Journal, 172, 66. doi:10.3847/1538-3881/ae7a32.
[6] Aguichine, A., Batalha, N., Fortney, J. J., Nettelmann, N., Owen, J. E., & Kempton, E. M.-R. (2025). Evolution of steam worlds:
energetic aspects. The Astrophysical Journal, 988, 186. doi:10.3847/1538-4357/add935.
[7] Aguichine, A., Fortney, J., Batalha, N., et al. (2026). Evolutionary tracks for Steam Worlds, Extended in Temperature (SWEET
model), version 5. Zenodo. Dataset; associated extension manuscript listed as in preparation. doi:10.5281/zenodo.21403288.
[8] Egger, J. A. plaNETic public model release. Pinned commit d710acdd1e2aaedb7aa604b01e195379e2522db8; accessed 15
October 2026. github.com/joannegger/plaNETic.
[9] Masuda, K., and collaborators. jnkepler V1298 Tau joint mass-ratio archive associated with Livingston et al. Pinned commit
ef1bc64b6fda657ca40d23053978bd0c7ecf0b7b; accessed 15 October 2026. github.com/kemasuda/jnkepler.
[10] KRONOS collaboration. KRONOS-I-V1298-Tau-c-NIRISS retrieval archive associated with Murphy et al. Pinned commit
56ff480b7e5c8816a31c0284158897e8152c08e0; accessed 15 October 2026.
github.com/kronos-jwst/KRONOS-I-V1298-Tau-c-NIRISS.
[11] Steinmeyer, M.-L., Dorn, C., Werlen, A., & Grimm, S. L. (2026). Coupled thermal-chemical evolution models of sub-Neptunes
reveal atmospheric signatures of their formation location. The Astrophysical Journal. doi:10.3847/1538-4357/ae4c47.

## Page 13

Anonymous Hydrogen envelopes and bulk water in young planets
13
Appendix A. Numerical support and validation
Table 6. Adopted numerical domain and baseline effective sample size.
Planet Mass support (%) D/W valid prior (%) S valid prior (%) Mixed Neff
TOI-2076 b 99.97 96.67 99.97 41,305
TOI-2076 c 100.00 96.15 100.00 8,020
TOI-2076 d 99.19 93.02 99.19 8,800
V1298 Tau c 100.00 100.00 100.00 1,827
V1298 Tau d 100.00 100.00 100.00 1,612
D/W fractions describe the baseline domain before the young-luminosity and w ≥ 0.10 restrictions. V1298 Tau mixed effective
sample sizes use the headline heat prior. Small differences between D and W domain fractions are below the relevant precision.
Mass support retains 99.97%, 100%, 99.19%, 100% and 100% of the five mass inputs, in table order. TOI-2076
D/W valid fractions are smaller mainly because the age-luminosity mapping can leave the adopted luminosity
interval. The code conditions on its domain rather than assigning likelihoods to an undefined model.
Source neural-weight hashes match the pinned Git LFS files. Independent float64 evaluation of the layer
operations agrees with float32 evaluation to relative differences below 10-7 in checked cases. Fixed-mass/radius
solutions have maximum residual 2.6 × 10-6 R⊕ when re-evaluated through the surrogate. These tests validate
numerical consistency, not agreement with a newly computed physical training set.
Eight-block diagnostics and effective sample sizes are retained in the summaries. They are approximate
integration diagnostics; subblocks of one scrambled Sobol realization are not independent experiments.
Spectral-interior mixed fits have effective sample sizes near 600, and low-water fits near 300 at baseline.
Bandwidth and discrepancy sensitivities accompany nominal ratios, whose precision is intentionally limited.
Appendix B. Reproduction and interpretation of result files
The compact bundle contains a pinned input manifest, numerical inputs except large networks, analysis
programs and summaries. Input downloads verify SHA-256 hashes. The sequence is: composition sampling;
fixed-radius profiles and validation; spectral recycling; low-water fitting; figure generation; and comparison
audit. This paper uses those frozen results. The earlier exploratory report is a separate artifact.
The primary summaries are fit_summary.json, spectral_summary.json, lowwater_summary.json and
audit_and_comparisons.json. BICEPS result keys named steam refer to a restricted auxiliary water-only check.
The reported S family uses external_steam, allowing the full cooling-grid water range. Confusing those
branches would change the interpretation of TOI-2076 b.
Kernel-density log-evidence values are meaningful only as relative composition ratios within a fixed stellar
retrieval. They omit source spectral normalization and cannot provide stellar-model odds. Mixed-family
intervals, the ≥10%-water class and the <1%-water competitor have distinct supports. A positive lower quantile
of one continuous posterior cannot replace comparison against the other families.
The bundle makes these choices inspectable. The calculations do not establish a new physical law or
population-level discovery; their result is a quantified non-uniqueness of bulk water under observations that can
favor H/He retention.
