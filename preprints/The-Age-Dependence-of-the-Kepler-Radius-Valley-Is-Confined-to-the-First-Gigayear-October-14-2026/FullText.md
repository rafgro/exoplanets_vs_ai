## Page 1

The Age Dependence of the Kepler Radius Valley Is Confined to the
First Gigayear:
A Confounder-Controlled Re-analysis with Forward-Modelled Age Uncertainties
A. Author1
1Affiliation to be inserted
author@institution.edu
October 14, 2026

Abstract

The number ratio of super-Earths to sub-Neptunes has been reported to rise with host-star age by several groups and is widely read as
evidence for Gyr-long core-powered mass loss. Stellar age, however, is entangled with stellar mass, metallicity and transit detectability
in every Kepler sample, and isochrone ages carry uncertainties comparable to the intrinsic spread of log age. We re-analyse the
super-Earth fraction fSE for 2,007 Kepler planets with 1 < Rp < 4R⊕ (after scaling to the mass- and period-dependent valley) and
1 < P < 100 d around 1,510 hosts, combining the Gaia–Kepler Stellar Properties Catalog with the CKS VII sample, and introduce
three controls that have not been applied to this question: a per-star detectability covariate derived from the detected planet’s own
multiple-event statistic; a stratified permutation null that shuffles ages only within strata of mass, [Fe/H] and detectability; and
an errors-in-variables model that propagates each star’s age posterior into a constraint on the sub-Neptune conversion timescale
τ. The raw trend is not monotonic: fSE = 0.31±0.05 for hosts younger than 1 Gyr, 0.48±0.03 at 1–2 Gyr and 0.38–0.44 beyond.
The old-age decline in the full Kepler sample is a sensitivity effect, and the apparent rise in CKS is driven by the age–metallicity
anticorrelation; the confounders alone predict a young–old difference of the opposite sign (−0.07±0.05 against the observed +0.12,
z = 3.7). After nearest-neighbour matching in mass, [Fe/H], period and detectability, hosts younger than 1 Gyr have fSE = 0.31
against 0.47 for matched older hosts (∆ = −0.16, 68% interval [−0.22,−0.11], host-level bootstrap p = 0.007), a deficit present
independently in the CKS and non-CKS halves, located at 1.0–1.5R⊕ and mirrored by an excess just above the valley (1.8–2.3R⊕:
24% versus 12%). For hosts older than 2 Gyr the matched difference is −0.02±0.02. The errors-in-variables fit prefers a saturating
conversion with τ = 0.4 Gyr (2σ: 0.15–1.5 Gyr; ∆χ
2 = 7.7 against a static population), while continued log-linear evolution improves
on a static population by only ∆χ
2 = 2.7. A power analysis shows that a rise of fSE from 0.27 to 0.44 between 0.5 and 8 Gyr would
have produced a measured-age slope of +0.66±0.20 against +0.39±0.21 observed. The radius distribution therefore does evolve,
but the evolution that current data resolve is largely complete within 1–2 Gyr, and the age trend as measured with Kepler isochrone
ages does not discriminate between core-powered mass loss and photoevaporation.
Keywords: exoplanets — planetary atmospheres — stellar ages — methods: statistical

1. INTRODUCTION

The radius distribution of close-in planets smaller than Neptune
is bimodal, with a valley near 1.8R⊕ separating rocky super-Earths from sub-Neptunes that retain H/He envelopes (Fulton
and Petigura 2018; Fulton et al. 2017; Van Eylen et al. 2018).
Two families of models carve the valley by stripping envelopes:
photoevaporation by the host’s X-ray and ultraviolet flux, which
is strongest in the first ∼100 Myr (Lopez and Fortney 2013;
Owen and Wu 2013, 2017), and core-powered mass loss, which
is driven by the planet’s own cooling luminosity and proceeds
over gigayears (Ginzburg et al. 2018; Gupta and Schlichting
2019). The two make a differential prediction that is in principle
easy to test: under photoevaporation the relative abundance of
super-Earths should be set within ∼100–300 Myr, whereas
under core-powered mass loss it should keep rising, “especially
over periods from 500 Myr to 3 Gyr” (Gupta and Schlichting
2020).
Several groups have reported the predicted rise. Berger
et al. (2020a) found a super-Earth to sub-Neptune number ratio of 0.61±0.09 for Kepler hosts younger than 1 Gyr against
1.00±0.10 for older hosts, using Gaia-based isochrone ages.
David et al. (2021) found the valley emptier below ∼2–3 Gyr
in the California–Kepler Survey (CKS) sample and a deficit of
large super-Earths (1.5–1.8R⊕) around young hosts; Sandoval
et al. (2021) recovered the rise with a Monte-Carlo treatment of
age uncertainties. Chen et al. (2022) found the ratio increasing
with age and decreasing with [Fe/H] and [α/Fe] in a LAMOST–
Gaia–Kepler sample, Ho and Van Eylen (2023) a weak positive
dependence of the valley location on age, and two 2026 studies
report the same qualitative behaviour in a homogeneous spectroscopic host sample (Kamulali et al. 2026) and in a sample
with chemical and kinematic ages (Chen et al. 2026). The result
is now routinely cited as evidence for Gyr-long atmospheric
loss.

## Page 2

The age axis is, however, unusually exposed to confounding. First, isochrone ages are a function of position in the
Hertzsprung–Russell diagram and hence of mass: a dwarf
receives a young age because it sits near the zero-age main
sequence, and informative ages exist mainly for stars massive
enough to evolve within a Hubble time. In the full Kepler sample the median host mass falls from 1.28M⊙ in the < 1 Gyr
bin to 0.91M⊙ above 10 Gyr, and the valley location, the sub-Neptune size and the super-Earth/sub-Neptune ratio all depend
on mass (Berger et al. 2020a; Fulton and Petigura 2018; Petigura et al. 2022). Second, age anticorrelates with metallicity,
and metal-poor hosts have fewer sub-Neptunes (Owen and
Murray-Clay 2018; Petigura et al. 2018). Third, old hosts are
harder targets: in the full Kepler sample the oldest bins are
fainter by 1.8 mag in Kp, so the small planets that define the
super-Earth population are preferentially lost, which biases
the ratio downward with age. Petigura et al. (2022) found no
change of sub-Neptune size with age over 1–10 Gyr and warned
explicitly that metallicity and age trends are confounded with
mass. Previous analyses addressed these issues by matching
the mass distributions of two age bins (Berger et al. 2020a) or
by treating [Fe/H] as a second axis (Chen et al. 2022); none
quantified what the confounders alone would produce, none
controlled detectability star by star, and none propagated the
∼0.2–0.4 dex age uncertainties into a model of the evolution
itself.
Here we do those three things. We ask the question the
way the physics poses it—not “is there a trend” but “on what
timescale does the population change, and could the data see
a Gyr-scale change if it were there”. Section 2 describes the
samples, Section 3 the tests, Section 4 the results, Section 5 a
cross-check with stellar rotation, and Section 6 the implications.

2. DATA

2.1. Catalogs and samples

Three overlapping samples are analysed (Table 1); sample C
is the primary one. Sample A combines the Kepler Data Release 25 (DR25) Kepler Objects of Interest (KOIs; Thompson et al. 2018) with the Gaia–Kepler Stellar Properties Catalog (GKSPC; Berger et al. 2020b), whose isochrone masses,
radii, metallicities and ages derive from Gaia DR2 parallaxes, 2MASS K photometry and spectroscopic or photometric
[Fe/H]. Sample B is the CKS VII sample (Fulton and Petigura
2018): Keck-HIRES spectroscopic Teff and [Fe/H] (Johnson
et al. 2017), Gaia DR2 radii and grid-based isochrone ages.
Sample C takes the CKS ages and metallicities where available
and adds the sample-A planets whose hosts are not in CKS, so
that every host appears once with its best available age. All catalogs were retrieved from public GitHub mirrors of the original
tables.1
1GKSPC Tables 1–2 and the DR25 KOI list from https://github.
com/ExoJulia/SysSimData and https://github.com/ExoJulia/SysSimDataInputs
(Ford et al. 2020; Hsu et al. 2019); the CKS VII machine-readable tables from
https://github.com/California-Planet-Search/cksgaia; rotation periods of Mazeh
et al. (2015) matched to CKS from https://github.com/RuthAngus/kepler_ages.
Table 1. Samples analysed. Planet counts are after the radius and
period cuts of Section 2.4.
Sample Planets Hosts Median σ(log age)
A: DR25 KOIs × GKSPC 1,759 1,350 0.37 dex
B: CKS VII 1,019 639 0.19 dex
C: B + non-CKS part of A 2,007 1,510 0.29 dex

2.2. Cuts

For sample A we follow Berger et al. (2020a): DR25 pipeline
disposition CANDIDATE and no false-positive disposition;
Gaia RUWE ≤ 1.2; isochrone goodness-of-fit ≥ 0.99; main-sequence hosts (logg > 3.8, no red-giant or clump flag, Teff <

7900 K); and informative ages only (time to terminal-age main

sequence < 20 Gyr; no GKSPC unreliable-age flag). Planet
radii are recomputed as Rp = (Rp/R⋆)DR25 R⋆,GKSPC. For sample B we require no CKS or archive false-positive flag, a Gaia
8
′′ flux ratio below 1.1 (no dilution) and R⋆ < 2R⊙. Ages and
uncertainties are the catalog posterior medians and 16th/84th
percentiles, used in log age with σ = max(σ+,σ−).
In sample A the variance of measured log age (0.077 dex2)
is smaller than the mean squared age uncertainty (0.138 dex2);
in sample C the two are 0.088 and 0.121 dex2. Measured ages
therefore order the hosts only coarsely beyond ∼2 Gyr, which
is why Section 4.6 quantifies the power of every test before a
null is interpreted.

2.3. Detectability proxy

For each planet the DR25 multiple-event statistic (MES) is
rescaled to the value a 1R⊕ planet would have produced at the
same period around the same star,
MES1 = MES(R⊕/Rp)
2
. (1)
To first order MES1 depends only on the star’s noise, radius and transit count, not on the detected planet’s radius, so
logMES1 is a per-star sensitivity measure that can be used
as a regression covariate and as a matching variable without a completeness model. The DR25 detection probability pdet(MES) = 0.94Γ(30.87,MES/0.271), the Christiansen
(2017) parametrisation adopted by Hsu et al. (2019), defines a
detection-complete subsample with pdet(1R⊕) > 0.9.

2.4. The radius valley and the classification

Radii are scaled along the valley to P = 10 d and M⋆ = 1M⊙,
R
′ = Rp (P/10d)0.10 (M⋆/M⊙)−0.25
, (2)
with the period and mass slopes of Petigura et al. (2022) and
Ho and Van Eylen (2023). The valley is located at the kernel-density minimum of logR
′
in each full sample, 1.82R⊕ (A) and
1.83R⊕ (B); planets with 1 < R
′ < 1.82R⊕ are super-Earths
and 1.82 < R
′ < 4R⊕ sub-Neptunes, and only 1 < P < 100 d is
used. Section 4.3 repeats the key test with a fixed 1.8R⊕ boundary, period-only scaling, a mass slope of 0.10 and boundaries
of 1.7–2.0 R⊕.

## Page 3

3. METHODS

The statistic throughout is the super-Earth fraction fSE =
NSE/(NSE + NSN) among detected planets (the ratio used by
earlier work is fSE/(1 − fSE)). The covariate vector is x =
(logM⋆,[Fe/H],logP,logMES1).
Binned fractions. fSE in six log-age bins (edges 8.5, 9.0, 9.3,
9.6, 9.8, 10.0, 10.3) with bootstrap 68% intervals.
Logistic regressions. logitP(SE) = a+bage log(age) +b · x,
adding covariates one at a time, with standard errors cluster-robust by host star because multi-transiting systems contribute
correlated planets.
Stratified permutation null. Hosts are placed in 36 strata
(quartiles of logM⋆ × terciles of [Fe/H] × terciles of logMES1)
and the measured ages are shuffled within strata 4,000 times.
This destroys any dependence of the planet population on age
while preserving the joint distribution of age with mass, metallicity and sensitivity. The null distributions of the age-only
logistic slope and of fSE(> 1Gyr) − fSE(< 1Gyr) are compared with the observed values; z is quoted relative to the null
mean and spread. An unstratified shuffle is run alongside.
Matched comparison. Each planet around a host younger
than a cut (1, 2 or 3.2 Gyr) is matched to its k = 5 nearest older planets in standardised x space, and fSE(young) −
fSE(matched old) is bootstrapped over young host stars (3,000
resamples). Variants use k = 1 and 10 and add logR⋆ and Kp
to the matching space.
Errors-in-variables evolution model.
logitP(SE|t,x) = a+b· x+Dg(t; τ), (3)
with g = 1 − e
−t/τ
, a saturating conversion of sub-Neptunes
into super-Earths with timescale τ and asymptotic logit shift
D, bounded to |D| ≤ 3 (odds ratios up to e
3 ≈ 20); and, as the
opposite limiting case, g = log10(t/Gyr). Each star’s true age
is integrated out numerically with K = 128 draws from a lognormal approximation of its posterior truncated to 0.05–14 Gyr.
The likelihood is profiled over τ on a grid from 0.15 to 20 Gyr;
∆χ
2
is quoted against the static model D = 0.
Power analysis. Synthetic super-Earth labels are drawn from
the fitted covariate model plus an injected evolution (D, τ),
with true ages drawn from the stars’ posteriors, and the
naive measured-age slope (with covariates) and the errors-in-variables ∆χ
2
are recomputed over 120 realisations per scenario.

4. RESULTS

4.1. The raw trend is not monotonic

In all three samples fSE is lowest for hosts younger than 1 Gyr
and highest at 1–2 Gyr; beyond 2 Gyr it declines in the full
Kepler sample and is flat in CKS (Figure 1, Table 2). The lower
panels of Figure 1 show what moves along the age axis: in
sample A the median host mass falls from 1.28 to 0.91M⊙ and
the sensitivity to a 1R⊕ planet drops by 0.3 dex; in CKS the
median [Fe/H] falls from +0.14 to −0.23.
The Berger et al. (2020a) split reproduces in sample A as
SE/SN = 0.56 (< 1 Gyr) against 0.71 (> 1 Gyr), but the >

1 Gyr value is an average over a bin-to-bin decline from 1.0

at 1–2 Gyr to 0.45 above 10 Gyr. The David et al. (2021) rise
reproduces in sample B only between the < 1 Gyr bin and
∼2 Gyr.

4.2. Confounders explain the old-age behaviour and predict

the opposite sign
Adding mass and metallicity to the logistic model barely moves
the age coefficient; adding the per-star detectability term does
(Table 3, Figure 3). In sample A the age-only coefficient is
−0.51±0.18—fSE falls with measured age, p = 0.006—and
becomes +0.25 ± 0.28 with logMES1. Within detectability
tertiles the decline largely disappears (Figure 2): the low-sensitivity tertile has fSE ≈ 0.13 at every age because only
sub-Neptunes are detectable there, and the high-sensitivity tertile has fSE ≈ 0.6–0.7. In sample B the raw coefficient of
+0.25 ± 0.22 drops to +0.06 when [Fe/H] is added and recovers to +0.43±0.30 with detectability. The full-covariate
coefficient in sample C is +0.39±0.21 (p = 0.07).
The stratified permutation null makes the direction of the
confounding explicit (Figure 4). Shuffling ages within mass ×
[Fe/H] × sensitivity strata, the expected fSE(> 1Gyr)− fSE(<
1Gyr) is −0.08 ± 0.06 (A), −0.04 ± 0.06 (B) and −0.07 ±
0.05 (C): the host population alone would make old hosts look
poorer in super-Earths. The observed differences are +0.06,
+0.14 and +0.12, i.e. z = +2.3, +2.8 and +3.7 above the
confounder-only expectation. The age-only slope tells the same
story with less power (z = +1.5, +2.7, +2.1). An unstratified
shuffle gives the familiar but misleading answer that sample A’s
negative slope is “significant” (p = 0.005) and sample B’s
positive slope is not.

4.3. A robust deficit of super-Earths around hosts younger than

∼1 Gyr
Matching each young planet to its five nearest older planets
in (logM⋆,[Fe/H],logP,logMES1) gives the cleanest number.
In sample C, hosts younger than 1 Gyr (78 planets, 55 stars;
median M⋆ = 1.00M⊙, [Fe/H] = +0.11, Teff = 5600 K, Kp =
13.7) have fSE = 0.31 against 0.47 for their matched older
counterparts: ∆ = −0.16, 68% interval [−0.22,−0.11], host-level bootstrap p = 0.007. The covariate means of the young
and matched sets agree to within 0.01–0.02 in every dimension.
With the cut at 2 Gyr the difference is −0.05 [−0.08,−0.03]
(p = 0.04); at 3.2 Gyr it is −0.02 [−0.04,−0.01] (p = 0.16).

## Page 4

0.20
0.25
0.30
0.35
0.40
0.45
0.50
0.55
0.60
su
per-E
arth fractio
n
fSE
n=53
n=257
n=597
n=499n=276
n=77
A: Kepler DR25 × GKSPC (N=1759)
0.20
0.25
0.30
0.35
0.40
0.45
0.50
0.55
0.60
n=54
n=129 n=290
n=213
n=229 n=104
B: CKS VII (N=1019)
0.20
0.25
0.30
0.35
0.40
0.45
0.50
0.55
0.60
n=78
n=251
n=626
n=479
n=415
n=158
C: combined best-age (N=2007)
9.0 9.5 10.0
log10 isochrone age [yr]
0.6
0.8
1.0
1.2
1.4
host-star covariates
median M* [M⊙ ]
median [Fe/H] + 1
median log MES(1 R ⊕ )
9.0 9.5 10.0
log10 isochrone age [yr]
0.6
0.8
1.0
1.2
1.4
9.0 9.5 10.0
log10 isochrone age [yr]
0.6
0.8
1.0
1.2
1.4
Figure 1. Top: super-Earth fraction in log-age bins for the three samples, with bootstrap 68% intervals and bin counts; the grey band marks 1 Gyr.
Bottom: median host mass, [Fe/H] and logMES1 in the same bins, showing the demographic and sensitivity gradients that run along the age axis.
Table 2. Super-Earth fraction in log-age bins (bootstrap 68% uncertainties; planet counts in parentheses).
Sample < 1 Gyr 1–2 Gyr 2–4 Gyr 4–6.3 Gyr 6.3–10 Gyr > 10 Gyr
A 0.36±0.06 (53) 0.50±0.03 (257) 0.44±0.02 (597) 0.38±0.02 (499) 0.38±0.03 (276) 0.31±0.05 (77)
B 0.30±0.06 (54) 0.42±0.04 (129) 0.43±0.03 (290) 0.47±0.03 (213) 0.43±0.03 (229) 0.42±0.05 (104)
C 0.31±0.05 (78) 0.48±0.03 (251) 0.44±0.02 (626) 0.40±0.02 (479) 0.41±0.02 (415) 0.38±0.04 (158)
The deficit is present in the two disjoint halves of sample C—
the CKS hosts (−0.17, p = 0.02) and the non-CKS Kepler
hosts (−0.13, p = 0.09)—whose ages come from different
spectroscopic inputs and isochrone pipelines.
Table 4 shows the robustness grid. The sign and size are
stable; the subsample p-values track the number of young
planets. The deficit is not a hot-star or high-mass effect (it
is the same below 6300 K and below 1.2M⊙), not a vetting
effect (it persists at MES > 20, where the DR25 Robovetter
completeness is high) and not a boundary artefact.

4.4. Where in radius the change happens

The young hosts’ planets are missing at the small end and
piled up just above the valley (Figure 5). Fractions of planets
by scaled radius, young versus matched old, are: 1.0–1.5R⊕,
0.21 versus 0.34 (∆ = −0.14 [−0.19,−0.09]); 1.5–1.82R⊕,
0.10 versus 0.13; 1.82–2.3R⊕, 0.24 versus 0.12 (∆ = +0.12
[+0.07,+0.18], p = 0.02); 2.3–3R⊕, 0.28 versus 0.27; 3–4R⊕,
0.17 versus 0.13. The sub-Neptune peak of the young sample
is at ∼2.4 R⊕ rather than ∼2.7 R⊕. This is the pattern expected
if a population of thin-envelope planets sitting just above the
valley has not yet been stripped at < 1 Gyr and ends up below it
later; it differs from David et al. (2021), who located the young
deficit at 1.5–1.8R⊕.

4.5. Timescale of the change

Propagating the age posteriors, the saturating model is preferred
over a static population with ∆χ
2 = 7.7 (two extra parameters,
p = 0.02) in sample C, 4.6 in A and 4.8 in B (Figure 6, Table 5).
The best timescale is τ = 0.38 Gyr in C (0.30 in A, 0.48 in B);
the 2σ interval in C is 0.15–1.5 Gyr, and τ = 3 Gyr is worse
than the best fit by ∆χ
2 = 5.2. The implied intrinsic fSE at
mean covariates rises from 0.23 at 0.5 Gyr to 0.35 at 1 Gyr and
0.40 by 2 Gyr, then stays flat. The log-linear alternative—a
continued rise of 0.33 in logit per dex, i.e. fSE from 0.30 to 0.41
between 0.3 and 8 Gyr—improves on the static model by only

## Page 5

9.0 9.2 9.4 9.6 9.8 10.0
log10 isochrone age [yr]
0.1
0.2
0.3
0.4
0.5
0.6
0.7
fSE
A: Kepler DR25 × GKSPC (N=1759)
MES(1 R ⊕ ) tertile
low sensitivity to 1 R ⊕
mid
high
9.0 9.2 9.4 9.6 9.8 10.0
log10 isochrone age [yr]
C: combined best-age (N=2007)
Figure 2. Super-Earth fraction versus age inside tertiles of logMES1 for samples A and C. Sensitivity, not age, sets most of the old-age decline
of Figure 1.
Table 3. Logistic coefficient on log age, bage (cluster-robust standard
errors), as covariates are added, and the stratified-permutation results.
Model A B C
age only −0.51±0.18 +0.25±0.22 −0.16±0.16
+ logM⋆ −0.51±0.21 +0.31±0.22 −0.12±0.17
+ [Fe/H] −0.51±0.22 +0.06±0.26 −0.16±0.17
+ logP −0.48±0.26 −0.07±0.29 −0.13±0.20
+ logMES1 +0.25±0.28 +0.43±0.30 +0.39±0.21
Stratified null, fSE(> 1Gyr)− fSE(< 1Gyr):
observed +0.06 +0.14 +0.12
null mean ± sd −0.08±0.06 −0.04±0.06 −0.07±0.05
z +2.3 +2.8 +3.7
Stratified null, age-only slope:
observed −0.51 +0.25 −0.16
null mean ± sd −0.70±0.13 −0.15±0.15 −0.42±0.12
z +1.5 +2.7 +2.1
∆χ
2 = 2.7 (p = 0.10) and is worse than the saturating model
by 5.0 with one fewer parameter. The amplitude D sits at its
bound of 3 in samples A and C, so the 1σ ranges in τ are not
meaningful; the 2σ ranges and the comparisons at fixed τ are.

4.6. Could the data have seen a Gyr-scale change?

Yes, for a change of the size claimed in the literature (Figure 7, Table 6). With sample C’s own hosts, age posteriors
and covariates, a static population yields a naive measured-age slope of 0.00 ± 0.20, and an injected core-powered-like
evolution with D = 1, τ = 3 Gyr (fSE 0.27 → 0.33 → 0.44
at 0.5, 2 and 8 Gyr) yields +0.66 ± 0.20 and an errors-in-variables ∆χ
2 > 6 in 88% of realisations. The observed full-covariate slope, +0.39±0.21, lies between the static and the
age only + M* + [Fe/H] + period + detectability
−0.8
−0.6
−0.4
−0.2
0.0
0.2
0.4
0.6
0.8
logistic coe
fficient on log age
(d lo
git fSE / d lo
g
a
ge)
A: Kepler DR25 × GKSPC (N=1759)
B: CKS VII (N=1019)
C: combined best-age (N=2007)
Figure 3. Logistic coefficient on log age as covariates are added, with
cluster-robust errors (Table 3).
D = 1, τ = 1 Gyr scenario (+0.37±0.18) and 1.3σ below the
τ = 3 Gyr scenario; a stronger late evolution (D = 2, τ = 3 Gyr,
fSE 0.17 → 0.50) would have given +1.2±0.2 and is excluded.
Mild continued evolution (D = 0.6, τ = 3–8 Gyr; expected
+0.25 to +0.39) is fully consistent with the data: the measurement cannot yet separate “finished by 1–2 Gyr” from “mostly
finished by 2 Gyr with a slow tail”.

5. CROSS-CHECK WITH STELLAR ROTATION

Rotation periods from Mazeh et al. (2015) exist for 217 of
the CKS hosts with Teff < 6250 K. Rotation is an age indicator whose systematics are unrelated to the isochrone age–
mass degeneracy, so it can test whether the isochrone-young
hosts are physically young and whether the deficit follows an
independent age proxy. The isochrone ages are physically
meaningful: the rotation residual ∆logProt (log period minus a quadratic fit in Teff) correlates with isochrone log age
at ρ = 0.41 (p = 4 × 10−10), and the isochrone-young hosts
rotate faster (median ∆logProt = −0.10 against +0.03). On the

## Page 6

−0.2 −0.1 0.0 0.1
fSE(>1 Gyr) − fSE(<1 Gyr)
0
50
100
150
200
250
300
350
400
permutations
young–old difference, z = +3.7
stratified null
(age shuffled within M* ×[Fe/H]×MES strata)
observed
−0.8 −0.6 −0.4 −0.2 0.0
logistic slope on log age (no covariates)
0
50
100
150
200
250
300
age-only slope, z = +2.1 (null mean -0.42)
stratified null
observed
Figure 4. Sample C: stratified-null distributions of the young–old difference (left) and of the age-only logistic slope (right), with the observed
values. The confounders alone predict the opposite sign.
1 1.5 2 3 4
planet radius scaled to P = 10 d, M* = 1 M⊙ [R ⊕ ]
0.0
0.5
1.0
1.5
2.0
2.5
density (per dex)
matched older hosts (5 NN each; 390 draws) valley
hosts < 1 Gyr (78 planets, 55 stars)
Figure 5. Scaled-radius distributions (kernel density, per dex) of
planets around hosts younger than 1 Gyr and around their matched
older counterparts, sample C. The dashed line marks the valley at
1.82R⊕.
rotation axis itself fSE is flat: 0.44, 0.36 and 0.40 in the fast, intermediate and slow terciles, and the fastest-rotating quartile differs from its matched slow counterpart by +0.03±0.06. This
null has no power against the isochrone result: the fastest quartile contains only 20% isochrone-young (< 1 Gyr) hosts against
7% in the rest, so the isochrone-based deficit predicts a fast–
slow difference of only −0.03, consistent with +0.03±0.07
observed. Among the 22 isochrone-young hosts that have rotation periods, fSE = 0.32, the same as in the full young sample.
A decisive rotation-based test needs rotation periods for a few
hundred hosts younger than 1 Gyr, i.e. the TESS young-host
samples rather than Kepler.

6. DISCUSSION

6.1. Does the radius distribution change with age?

Yes, and the change is not an artefact of host-star demographics: the confounders present in Kepler samples push the apparent trend the other way, so the genuine young–old difference
(≈ +0.14 to +0.19 in fSE) is larger than the raw one. But the
change that the data resolve is a deficit of super-Earths, with an
excess of planets just above the valley, around hosts younger
than ∼1 Gyr. Between 2 and 14 Gyr the matched difference
is −0.02±0.02, and the errors-in-variables fit places the conversion timescale at τ ≈ 0.4 Gyr with a 2σ upper bound of

1.5 Gyr under a saturating model. The “Gyr-long” character of

the published trend comes from averaging a 1–2 Gyr peak with
lower, detection-biased or metallicity-biased values at old ages,
not from a measured rise beyond 2 Gyr.

6.2. Implications for the mass-loss mechanism

Photoevaporation models place the super-Earth population after
∼100–300 Myr but with a tail: planets with marginal envelopes,
and envelopes that keep contracting, continue to cross the valley
for up to ∼1 Gyr (Owen and Wu 2017; Rogers and Owen
2021). Core-powered mass loss predicts the ratio to keep rising
especially from 0.5 to 3 Gyr (Gupta and Schlichting 2020),
and the two mechanisms hand over to each other in different
parts of the mass–flux plane (Owen and Schlichting 2024). A
conversion largely complete by 1–2 Gyr sits at the boundary of
both predictions, and the excess at 1.8–2.3R⊕ at < 1 Gyr is the
natural signature of the last planets to be stripped under either
mechanism. The data therefore do not discriminate between
the mechanisms, contrary to the usual reading of the age trend.
What is excluded is a Gyr-scale continued rise of the size
that would make the discrimination (fSE increasing by ≳ 0.15
between 2 and 8 Gyr); a rise of ≲ 0.08 is not.

## Page 7

Table 4. Matched comparison of hosts younger than 1 Gyr with their five nearest older hosts in (logM⋆,[Fe/H],logP,logMES1), sample C,
under variations of the sample, matching and classification. ∆ = fSE(young)− fSE(matched old) with 68% host-bootstrap interval and two-sided
bootstrap p.
Variant N fSE young fSE matched old ∆ [68%] p
baseline (k = 5) 2007 0.31 0.47 −0.16 [−0.22,−0.11] 0.007–0.013
k = 1 / k = 10 2007 0.31 0.46 / 0.47 −0.15 / −0.16 0.047 / 0.005
match also on logR⋆, Kp 2007 0.31 0.43 −0.13 [−0.19,−0.07] 0.047
MES > 12 (vetting-complete) 1501 0.25 0.39 −0.14 [−0.21,−0.09] 0.020
MES > 20 952 0.19 0.32 −0.13 [−0.18,−0.08] 0.008
pdet(1R⊕) > 0.5 493 0.39 0.57 −0.18 [−0.31,−0.07] 0.105
exclude 3–4R⊕ 1668 0.37 0.56 −0.19 [−0.27,−0.12] 0.013
P < 30 d 1640 0.37 0.53 −0.17 [−0.24,−0.11] 0.017
fixed 1.8R⊕ boundary, unscaled radii 1989 0.28 0.44 −0.16 [−0.22,−0.10] 0.004
period-only scaling / mass slope 0.10 1979 / 1992 0.31 0.47 / 0.46 −0.16 / −0.15 0.001 / 0.007
valley at 1.7 / 1.9 / 2.0 R⊕ 2007 0.29 / 0.35 / 0.38 0.42 / 0.48 / 0.51 −0.13 / −0.14 / −0.12 0.02–0.03
Teff < 6300 K / ≥ 6300 K 1817 / 190 0.29 / 0.35 0.47 / 0.49 −0.18 / −0.14 0.02 / 0.19
M⋆ < 1.2 / ≥ 1.2M⊙ 1732 / 275 0.30 / 0.36 0.45 / 0.53 −0.16 / −0.17 0.03 / 0.23
single / multi-transiting hosts 1159 / 848 0.30 / 0.32 0.49 / 0.42 −0.20 / −0.11 0.015 / 0.21
CKS-only / non-CKS hosts 1019 / 988 0.30 / 0.33 0.47 / 0.47 −0.17 / −0.13 0.024 / 0.092
Table 5. Errors-in-variables fits. ∆χ
2
is the improvement over a static
population (D = 0); the saturating model adds two parameters, the
log-linear model one.
A B C
best τ (Gyr) 0.30 0.48 0.38
2σ range of τ (Gyr) 0.15–4.9 0.15–7.9 0.15–1.5
∆χ
2
, saturating (best τ) 4.6 4.8 7.7
∆χ
2
at τ = 1 Gyr 1.8 4.4 5.1
∆χ
2
at τ = 3 Gyr 0.7 2.1 2.4
∆χ
2
at τ = 8 Gyr 0.5 0.9 1.4
∆χ
2
, log-linear 1.0 2.0 2.7
implied fSE at 0.5 Gyr 0.26 0.22 0.23
implied fSE at 1 Gyr 0.36 0.34 0.35
implied fSE at 2 Gyr 0.39 0.42 0.40
implied fSE at 8 Gyr 0.39 0.43 0.40

6.3. Why earlier analyses saw a monotonic rise

In GKSPC-based work, matching the mass distributions of
two age bins leaves the brightness and sensitivity differences
in place (replacing the mass-scaled valley by a fixed 1.8R⊕
boundary changes the young–old contrast by only ∼0.01 in our
sample, so the classification is not the issue). In CKS-based
work the metal-poor old hosts contribute fewer sub-Neptunes.
In both, the < 1 Gyr bin carries most of the signal while the axis
beyond 2 Gyr carries little information: the intrinsic spread of
measured log age is comparable to the age uncertainties, which
compresses any late trend toward zero and makes bin-to-bin
comparisons at 3–10 Gyr mostly noise and demographics.

6.4. Caveats

(i) The young sample is small and its ages are soft: 55 host stars
carry the main result, with isochrone ages of 0.46–0.98 Gyr and
σ ≈ 0.45 dex, so their true ages plausibly span 0.2–2.5 Gyr;
Table 6. Power analysis on sample C: measured-age logistic slope
(with covariates) and the fraction of realisations with errors-in-variables ∆χ
2 > 6 under injected evolution scenarios. The observed
slope is +0.39±0.21.
D τ (Gyr) fSE(0.5) fSE(8) slope P(∆χ
2 > 6)
0 – 0.38 0.38 0.00±0.20 0.04
1 0.3 0.34 0.38 +0.14±0.21 0.12
1 1 0.27 0.41 +0.37±0.18 0.40
1 3 0.27 0.44 +0.66±0.20 0.88
1 8 0.30 0.43 +0.52±0.18 0.72
2 0.4 0.27 0.40 +0.33±0.18 0.56
2 3 0.17 0.50 +1.22±0.21 1.00
0.6 3 0.31 0.42 +0.39±0.20 0.40
“< 1 Gyr” means “near the zero-age main sequence for its mass
and metallicity”. The obvious systematics that would mislabel
such stars push planet radii the wrong way to mimic a super-Earth deficit (a hotter Teff makes R⋆ and Rp smaller, not larger).
(ii) Young stars are active; unocculted spots bias transit depths
by a few per cent and activity raises the noise. The MES1
covariate captures the noise but not spot bias or Robovetter
behaviour on variable stars; the deficit survives at MES > 20,
which limits but does not eliminate this channel. (iii) Samples
A and B share stars and are not independent confirmations; the
CKS and non-CKS halves of sample C are, and give −0.17 and
−0.13. (iv) MES1 inherits the Eddington-type upward fluctuation of detected signals near threshold; this affects super-Earths
more than sub-Neptunes but is not age dependent, and the MES
cuts give the same answer. (v) Age posteriors are approximated
as truncated log-normals; asymmetric or multimodal posteriors
and the GKSPC grid edge at 14–20 Gyr are not modelled, and
D reaches its prior bound in two samples. (vi) The saturating
g(t) is a summary of conversion histories that in reality depend on core mass, envelope fraction and flux. (vii) The valley

## Page 8

10
0 101
conversion timescale τ [Gyr] (g = 1 − e
−t/τ
, |D| ≤ 3)
−8
−7
−6
−5
−4
−3
−2
−1
0
Δχ² relative to static model
(negative = evolving model better)
best(C) + 4 (≈2σ)
A: Kepler DR25 × GKSPC (N=1759)
B: CKS VII (N=1019)
C: combined best-age (N=2007)
10
−1 100 101
true age [Gyr]
0.1
0.2
0.3
0.4
0.5
0.6
fSE
at mea
n co
v
ariates
best fit: τ = 0.38 Gyr
τ = 3 Gyr (Δχ² worse by 5.2)
static
raw bins (measured age)
Figure 6. Left: profile likelihood over the conversion timescale τ for the three samples, with |D| ≤ 3; the dotted line is the sample-C minimum
plus 4 (≈ 2σ). Right: implied intrinsic fSE(t) at mean covariates for the best sample-C fit, for τ = 3 Gyr, and the static model, with the raw
measured-age bins overlaid.
slopes are uncertain by ∼0.03 (period) and ∼0.1 (mass); the
robustness grid covers that range. (viii) No kinematic or asteroseismic ages are used; a stratified re-analysis of the Chen et al.
(2022) kinematic-age sample with the detectability covariate is
the obvious next step.

6.5. Predictions

If the conversion saturates by 1–2 Gyr, TESS young-host samples with gyrochronological or cluster ages should show fSE
rising steeply between 0.2 and 1 Gyr and little change thereafter, with the valley shallowest at a few hundred Myr and
the excess just above it. If the log-linear tail is real, PLATO’s
asteroseismic ages (σ ≈ 10%) for a few thousand hosts would
detect the ∼0.1 change in fSE between 2 and 8 Gyr that Kepler
cannot.

7. SUMMARY

1. The raw super-Earth fraction of Kepler planets is not

monotonic in isochrone age: lowest below 1 Gyr (0.31±
0.05), highest at 1–2 Gyr (0.48±0.03), flat or declining
beyond.

2. The old-age behaviour is set by host demographics and

transit sensitivity, not by age; a stratified permutation null
shows the confounders alone would produce a young–old
difference of the opposite sign (z = 3.7 in the combined
sample).
3. After matching in mass, metallicity, period and detectability, hosts younger than 1 Gyr have fSE = 0.31 against
0.47 (∆ = −0.16, p = 0.007), independently in CKS
and non-CKS hosts and across fifteen analysis variants;
the deficit sits at 1.0–1.5R⊕ with a compensating excess
at 1.8–2.3R⊕. Beyond 2 Gyr the matched difference is
−0.02±0.02.

4. An errors-in-variables fit gives a conversion timescale

τ = 0.4 Gyr (2σ: 0.15–1.5 Gyr); continued log-linear evolution is only marginally preferred over a static population
(∆χ
2 = 2.7).

5. A power analysis shows Kepler isochrone ages would

have detected the Gyr-scale rise claimed in the literature;
its absence limits late evolution to ∆fSE ≲ 0.08 between
2 and 8 Gyr, which does not discriminate between core-powered mass loss and photoevaporation.
DATA AND CODE AVAILABILITY
All inputs are public (GKSPC, DR25 KOI table, CKS VII,
Mazeh et al. 2015 rotation periods; mirrors listed in Section 2).
The analysis scripts, the derived planet tables with scaled
radii, classifications, ages and covariates, and every number
quoted in this paper are provided as supplementary material
(radius_age_analysis.zip).
ACKNOWLEDGEMENTS
This research made use of the NASA Exoplanet Archive catalogs through their public mirrors, of data from the European
Space Agency mission Gaia and of the Kepler mission data
products.

REFERENCES

T. A. Berger, D. Huber, E. Gaidos, J. L. van Saders, and L. M. Weiss.
The Gaia-Kepler Stellar Properties Catalog. II. Planet Radius Demographics as a Function of Stellar Mass and Age. The Astronomical
Journal, 160(3):108, 2020a. doi: 10.3847/1538-3881/aba18a.
T. A. Berger, D. Huber, J. L. van Saders, E. Gaidos, J. Tayar, and A. L.
Kraus. The Gaia-Kepler Stellar Properties Catalog. I. Homogeneous

## Page 9

D = 0.0
τ = 1.0 Gyr
0.38 → 0.38
D = 1.0
τ = 0.3 Gyr
0.34 → 0.38
D = 1.0
τ = 1.0 Gyr
0.27 → 0.41
D = 1.0
τ = 3.0 Gyr
0.27 → 0.44
D = 1.0
τ = 8.0 Gyr
0.30 → 0.43
D = 2.0
τ = 0.4 Gyr
0.27 → 0.40
D = 2.0
τ = 3.0 Gyr
0.17 → 0.50
D = 0.6
τ = 3.0 Gyr
0.31 → 0.42
injected scenario: D, τ, and implied fSE(0.5 Gyr) → fSE(8 Gyr)
−0.2
0.0
0.2
0.4
0.6
0.8
1.0
1.2
1.4
naive logistic slope on measured log age
observed (sample C, full covariate model) ±1σ
simulated naive slope (mean ± sd over realisations)
Figure 7. Naive measured-age slopes (mean ± scatter over realisations) produced by injected evolution scenarios in sample C, against the
observed value with its 1σ band.
Fundamental Properties for 186,301 Kepler Stars. The Astronomical
Journal, 159(6):280, 2020b. doi: 10.3847/1538-3881/159/6/280.
D.-C. Chen, J.-W. Xie, J.-L. Zhou, S. Dong, C. Liu, H.-F. Zhang, A. L.
Luo, W. Zhu, J.-Y. Yang, and Y.-Z. Wu. Planets Across Space and
Time (PAST). III. Morphology of the Planetary Radius Valley as
a Function of Stellar Age and Metallicity in the Galactic Context
Revealed by the LAMOST-Gaia-Kepler Sample. The Astronomical
Journal, 163(6):249, 2022. doi: 10.3847/1538-3881/ac641f.
X. Chen, T. Sun, Y. Lu, Z. Lu, and L. Ye. Insights into the Exoplanet
Radius Valley from Host-Star Ages, Activity, Chemistry, and Birth
Radius. The Astrophysical Journal, 2026. doi: 10.3847/1538-4357/
ae5633. arXiv:2603.21581.
J. L. Christiansen. Planet Detection Metrics: Pixel-Level Transit
Injection Tests of Pipeline Detection Efficiency for Data Release

25. Technical report, Kepler Science Document KSCI-19110-001,

2017.
T. J. David, G. Contardo, A. Sandoval, R. Angus, Y. L. Lu, M. Bedell,
J. L. Curtis, D. Foreman-Mackey, B. J. Fulton, S. K. Grunblatt, and
E. A. Petigura. Evolution of the Exoplanet Size Distribution: Forming Large Super-Earths Over Billions of Years. The Astronomical
Journal, 161(6):265, 2021. doi: 10.3847/1538-3881/abf439.
E. B. Ford, M. Y. He, and D. C. Hsu. ExoJulia/SysSimData: input
catalogs for the Exoplanet System Simulator. https://github.com/
ExoJulia/SysSimData, 2020.
B. J. Fulton and E. A. Petigura. The California-Kepler Survey. VII.
Precise Planet Radii Leveraging Gaia DR2 Reveal the Stellar Mass
Dependence of the Planet Radius Gap. The Astronomical Journal,
156(6):264, 2018. doi: 10.3847/1538-3881/aae828.
B. J. Fulton, E. A. Petigura, A. W. Howard, H. Isaacson, G. W. Marcy,
P. A. Cargile, L. Hebb, L. M. Weiss, J. A. Johnson, T. D. Morton,
E. Sinukoff, I. J. M. Crossfield, and L. A. Hirsch. The California-Kepler Survey. III. A Gap in the Radius Distribution of Small
Planets. The Astronomical Journal, 154(3):109, 2017. doi: 10.
3847/1538-3881/aa80eb.
S. Ginzburg, H. E. Schlichting, and R. Sari. Core-powered mass-loss
and the radius distribution of small exoplanets. Monthly Notices
of the Royal Astronomical Society, 476(1):759–765, 2018. doi:
10.1093/mnras/sty290.
A. Gupta and H. E. Schlichting. Sculpting the valley in the radius
distribution of small exoplanets as a by-product of planet formation:
the core-powered mass-loss mechanism. Monthly Notices of the
Royal Astronomical Society, 487(1):24–33, 2019. doi: 10.1093/
mnras/stz1230.
A. Gupta and H. E. Schlichting. Signatures of the core-powered
mass-loss mechanism in the exoplanet population: dependence on
stellar properties and observational predictions. Monthly Notices
of the Royal Astronomical Society, 493(1):792–806, 2020. doi:
10.1093/mnras/staa315.
C. S. K. Ho and V. Van Eylen. A deep radius valley revealed by
Kepler short cadence observations. Monthly Notices of the Royal
Astronomical Society, 519(3):4056–4073, 2023. doi: 10.1093/
mnras/stac3802.
D. C. Hsu, E. B. Ford, D. Ragozzine, and K. Ashby. Occurrence Rates
of Planets Orbiting FGK Stars: Combining Kepler DR25, Gaia
DR2, and Bayesian Inference. The Astronomical Journal, 158(3):
109, 2019. doi: 10.3847/1538-3881/ab31ab.
J. A. Johnson, E. A. Petigura, B. J. Fulton, G. W. Marcy, A. W.
Howard, H. Isaacson, L. Hebb, P. A. Cargile, T. D. Morton, L. M.
Weiss, J. N. Winn, L. A. Rogers, E. Sinukoff, and L. A. Hirsch. The
California-Kepler Survey. II. Precise Physical Properties of 2025
Kepler Planets and Their Host Stars. The Astronomical Journal,
154(3):108, 2017. doi: 10.3847/1538-3881/aa80e7.
J. Kamulali, V. Adibekyan, B. Nsamba, S. G. Sousa, T. L. Campante,
A. Weiss, B. Kabugho, N. Moedas, N. C. Santos, and O. Trust.
Revisiting the exoplanet radius valley with host stars from SWEET-Cat. Astronomy & Astrophysics, in press, 2026. arXiv:2601.12396.
E. D. Lopez and J. J. Fortney. The Role of Core Mass in Controlling
Evaporation: The Kepler Radius Distribution and the Kepler-36
Density Dichotomy. The Astrophysical Journal, 776(1):2, 2013.

## Page 10

doi: 10.1088/0004-637X/776/1/2.
T. Mazeh, H. B. Perets, A. McQuillan, and E. S. Goldstein. Photometric Amplitude Distribution of Stellar Rotation of KOIs—
Indication for Spin-Orbit Alignment of Cool Stars and High Obliquity for Hot Stars. The Astrophysical Journal, 801(1):3, 2015. doi:
10.1088/0004-637X/801/1/3.
J. E. Owen and R. Murray-Clay. Metallicity-dependent signatures
in the Kepler planets. Monthly Notices of the Royal Astronomical
Society, 480(2):2206–2216, 2018. doi: 10.1093/mnras/sty1943.
J. E. Owen and H. E. Schlichting. Mapping out the parameter space
for photoevaporation and core-powered mass-loss. Monthly Notices
of the Royal Astronomical Society, 528(2):1615–1629, 2024. doi:
10.1093/mnras/stad3972.
J. E. Owen and Y. Wu. Kepler Planets: A Tale of Evaporation. The
Astrophysical Journal, 775(2):105, 2013. doi: 10.1088/0004-637X/
775/2/105.
J. E. Owen and Y. Wu. The Evaporation Valley in the Kepler
Planets. The Astrophysical Journal, 847(1):29, 2017. doi:
10.3847/1538-4357/aa890a.
E. A. Petigura, G. W. Marcy, J. N. Winn, L. M. Weiss, B. J. Fulton,
A. W. Howard, E. Sinukoff, H. Isaacson, T. D. Morton, and J. A.
Johnson. The California-Kepler Survey. IV. Metal-rich Stars Host a
Greater Diversity of Planets. The Astronomical Journal, 155(2):89,
2018. doi: 10.3847/1538-3881/aaa54c.
E. A. Petigura, J. G. Rogers, H. Isaacson, J. E. Owen, A. L. Kraus,
J. N. Winn, M. G. MacDougall, A. W. Howard, B. Fulton, M. R.
Kosiarek, L. M. Weiss, A. Behmard, and S. Blunt. The California-Kepler Survey. X. The Radius Gap as a Function of Stellar Mass,
Metallicity, and Age. The Astronomical Journal, 163(4):179, 2022.
doi: 10.3847/1538-3881/ac51e3.
J. G. Rogers and J. E. Owen. Unveiling the planet population at
birth. Monthly Notices of the Royal Astronomical Society, 503(1):
1526–1542, 2021. doi: 10.1093/mnras/stab529.
A. Sandoval, G. Contardo, and T. J. David. The Influence of Age on
the Relative Frequency of Super-Earths and Sub-Neptunes. The
Astrophysical Journal, 911(2):117, 2021. doi: 10.3847/1538-4357/
abea9d.
S. E. Thompson, J. L. Coughlin, K. Hoffman, F. Mullally, J. L. Christiansen, C. J. Burke, S. Bryson, N. Batalha, M. R. Haas, J. Catanzarite, J. F. Rowe, G. Barentsen, D. A. Caldwell, B. D. Clarke,
J. M. Jenkins, J. Li, D. W. Latham, J. J. Lissauer, S. Mathur, R. L.
Morris, S. E. Seader, J. C. Smith, T. C. Klaus, J. D. Twicken, J. E.
Van Cleve, B. Wohler, R. Akeson, D. R. Ciardi, W. D. Cochran,
C. E. Henze, S. B. Howell, D. Huber, A. Prsa, S. V. Ramirez, T. D.
Morton, T. Barclay, J. R. Campbell, W. J. Chaplin, D. Charbonneau,
J. Christensen-Dalsgaard, J. L. Dotson, L. Doyle, E. W. Dunham,
A. K. Dupree, E. B. Ford, J. C. Geary, F. R. Girouard, H. Isaacson, H. Kjeldsen, E. V. Quintana, D. Ragozzine, M. Shabram,
A. Shporer, V. Silva Aguirre, J. H. Steffen, M. Still, P. Tenenbaum,
W. F. Welsh, A. Wolfgang, K. A. Zamudio, D. G. Koch, and W. J.
Borucki. Planetary Candidates Observed by Kepler. VIII. A Fully
Automated Catalog with Measured Completeness and Reliability
Based on Data Release 25. The Astrophysical Journal Supplement
Series, 235(2):38, 2018. doi: 10.3847/1538-4365/aab4f9.
V. Van Eylen, C. Agentoft, M. S. Lundkvist, H. Kjeldsen, J. E. Owen,
B. J. Fulton, E. Petigura, and I. Snellen. An asteroseismic view of
the radius valley: stripped cores, not born rocky. Monthly Notices
of the Royal Astronomical Society, 479(4):4786–4795, 2018. doi:
10.1093/mnras/sty1783.
