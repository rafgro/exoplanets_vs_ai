## Page 1

Where to look for life and technology:
An audited decision analysis of confirmed exoplanets
Computational research preprint • 17 October 2026
Catalog and literature cutoff: 17 October 2026

Abstract

Which confirmed exoplanets should be prioritized when both environmental plausibility and
observational access matter? Individual probabilities of life or civilization are not identified by present
data, so a numerical “probability of life” ranking would obscure the dominant uncertainty. We instead
construct a reproducible, conditional decision audit. A frozen NASA Exoplanet Archive query contains
6,451 planet records; explicit provenance, status, size and flux checks leave 190 planets for an Earth-adjacent atmospheric screen. Fifteen sourced parameter overrides correct distances, reconcile stellar
measurements and preserve dynamical mass information. We propagate 8,192 physical realizations
per planet over 128 orbital phases through 648 environmental and instrument scenarios. Eligibility
and recoverability are evaluated on the same latent states, and a global minimax calculation examines
equal-time portfolios. Proxima Cen b ranks first in 92.4% of scenarios accessible to a southern 39 m
telescope. GJ 887 d supplies an alternative when larger temperate worlds are admitted. A corrected
distance nearly doubles the nominal angular separation of Gl 725 B c, but its declination excludes
it from the southern telescope. A separate injection experiment uses ten published photochemical
transmission spectra. At 20 ppm white plus 5 ppm correlated noise, recovery among six inhabited
models ranges from 2.99% to 89.36%, despite complete atmospheric-feature recovery in the simulated
trials. Omitting airless alternatives yields a 99.53% false-positive rate for a flat spectrum; admitting
them reduces that rate to 0.035%. A radio experiment covering 4,792 confirmed-planet hosts shows
strong dependence on assumed transmitter power, duty cycle and persistent beaming. The deliverable
is a set of auditable priorities and discriminating follow-up questions, not a claim that any world is
probably inhabited or that a modeled molecular feature establishes life.
Keywords: exoplanets; biosignatures; technosignatures; target selection; uncertainty; injection and
recovery

1 The scientific question and the contribution

The attractive target is often described as a planet that is both likely to host life and easy to observe.
The two parts of that description have very different evidential foundations. Distance, orbital period,
apparent brightness, and sometimes mass and radius are measured. Atmospheric survival, surface
water, the emergence of life, biological productivity, and technological activity are usually unknown. An
observing program must act despite this asymmetry. It should preserve the uncertainty rather than
replace it with a precise-looking score.
This study asks a narrower, operational question: which confirmed planets remain useful observing
targets across explicitly different environmental preferences and observational assumptions, and which
apparently favorable cases fail when the source data or the null hypotheses are audited? The restriction
to confirmed planets refers to a dated archive and a stated status rule. It does not establish that every
retained signal is indisputable, nor that other undiscovered planets in the same systems are absent.

## Page 2

Confirmed exoplanets: a decision audit 17 October 2026
The distinction between habitability, detectable biology, and evidence for biology is well established
(Catling et al., 2018; Walker et al., 2018). Earth-history arguments can inform particular models of
abiogenesis, but depend on conditioning and model assumptions and do not calibrate the relative
probability of life on an arbitrary M-dwarf planet and a water-rich super-Earth (Spiegel & Turner, 2012;
Kipping, 2020). The same difficulty is larger for civilization: neither technological emergence, survival,
transmitter design, nor the fraction of time a signal crosses Earth is measured for another civilization.
We consequently avoid assigning empirical probabilities to these unknown steps.

1.1 What is already known, and what is new here

Habitable-zone catalogs, orbital completeness calculations, and simulated atmospheric spectra are
extensive areas of prior work. Single-visit completeness combines geometry and photometric access
(Brown, 2005); orbital Monte Carlo has long propagated phase, inclination and brightness (Greco &
Burrows, 2015). LIFE X already applies such reasoning to the confirmed-planet catalog and compares
future thermal and reflected-light access (Carrión-González et al., 2023). Relative biosignature yields,
population simulations, and information-based survey design are developed by Tuchow & Wright (2020),
Bixel & Apai (2021), and Fields et al. (2023). The recent rocky habitable-zone catalog of Bohl et
al. (2026) is a particularly close target-list comparator. Photochemical simulations already include
inhabited atmospheres, abiotic false positives, and different observing modes (Currie & Meadows, 2025;
Eager-Nash et al., 2024a).
Our contribution is the new numerical audit of their conjunction: a frozen 2026 confirmed catalog
with traceable corrections; the measured size of the error from multiplying separately averaged eligibility
and observability; scenario-dependent ranks and an exact portfolio optimization; a finite-family spectral
test that explicitly challenges missing alternatives; and a radio calculation that separates observing cost
from occurrence assumptions. We do not claim the first habitable-zone ranking, the first inhabited-versus-abiotic spectrum, or the first Bayesian interpretation of a SETI null. Nor do we assert that
an individual candidate was overlooked by all prior literature. A planet can be underweighted by a
particular catalog query without having been overlooked by its discovery authors.
Three simulation modules are deliberately kept distinct. The catalog module estimates recovery
of a stipulated spectral feature. The atmospheric module measures discrimination within published
model families at achieved noise levels. The radio module measures recovery of specified narrowband
transmitter populations. Their numerical outputs are not interchangeable, and multiplying them into
an overall life probability would require additional, unsupported population assumptions.

1.2 Time horizon and scope

We use 2026–2036 as the near-future planning interval. Radio facilities and JWST already support
relevant observations. A 39 m ground-based scenario is conditional on the relevant instrumentation
becoming available: ESO lists planned ELT telescope first light in 2029 and scientific first light in 2030,
while ANDES is a later instrument (ESO, 2025; Pallé et al., 2025). The high-contrast ANDES mode is
specified in approximately 0.95–1.8 µm, even though the full spectrograph covers a wider range (ANDES
Consortium, 2026). We therefore use 1.27 µm for the ground-based comparison and do not assign the
visible oxygen A band to the baseline high-contrast mode.
A 6 m Habitable Worlds Observatory (HWO) comparison is included only to reveal a geometric change
with aperture and wavelength. HWO remains an architecture-development program; it is not assumed
operational within our near-future interval (NASA, 2026). LIFE offers a complementary longer-horizon
thermal route, but we do not implement a new interferometric noise model. Broadband thermal detection
forecasts must not be substituted for atmospheric retrieval requirements (Carrión-González et al., 2023;
Konrad et al., 2022).

## Page 3

Confirmed exoplanets: a decision audit 17 October 2026

2 Estimands: what can and cannot be ranked

Let xj be the available data for planet j, zj its latent physical state, Lj the presence of life, and a an
observing design. A discovery-oriented quantity would be
Uj (a) = Zp(zj | xj ) p(Lj = 1 | zj ) P(validated life evidence | Lj , zj , a) dzj . (1)
Neither the second factor nor the complete third factor is known. In particular, an atmospheric line
can be recovered when both biotic and abiotic models fit it. Even perfect precision cannot distinguish
hypotheses that predict identical data distributions. The archive alone therefore does not identify a
most-probably-inhabited planet. Different admissible biological assignments can reverse its ordering
without changing any measured catalog value.
We replace Eq. (1) with a declared conditional decision weight,
Jjm = Ezj |xj ,m[wm(zj )Dm(zj , a)] , 0 ≤ wm, Dm ≤ 1, (2)
where m indexes the scenario, wm encodes environmental eligibility and preferences, and Dm is the
power to recover the stipulated feature under the observation surrogate. A value of J = 0.1 is not a
10% life probability. It is an expectation within an explicitly chosen model. We retain the underlying
eligibility and recovery terms so that a reader can substitute different preferences.

2.1 Why separate averages can be misleading

The shortcut Je
jm = E[wm]E[Dm] discards shared states. The exact identity
Jjm − Je
jm = Cov(wm, Dm) (3)
is elementary, but its numerical size for catalog target selection deserves measurement. A nearly face-on
radial-velocity solution can be geometrically favorable while implying a much larger true mass. A
larger inferred radius brightens the planet while a mass gate excludes the same realization. An orbit or
luminosity realization can improve reflected flux while moving outside a temperature-related eligibility
interval. Coupling all factors to the same draw retains these effects. Independent shuffling is a useful
negative control, not a physical alternative universe.
The uncertainty model used below is a simulation distribution assembled from published marginal
uncertainties and declared completions. It is not a reconstruction of every original joint likelihood.
Accordingly, Eq. (2) should not be read as a fully hierarchical posterior estimate. The notation emphasizes
conditioning and shared variables; the limitations of the approximation remain material.

2.2 Robustness is a property of a stated scenario set

For each scenario we normalize by its best target and record ranks. The fraction of scenarios in which a
planet ranks in the first five is a scenario frequency; equal weighting of the grid is a reporting convention.
It is not a posterior probability, and it would change if the scenario dictionary were expanded or
duplicated.
For an equal-time portfolio A of three different planets, each receiving 100 hours, define
R(A) = max
m
"
1 −
P
j∈A Jjm
P
j∈A⋆m
Jjm #
, (4)
where A⋆
m contains the three best planets in scenario m. A mixed-integer linear program minimizes R(A)
over all candidates with a nonzero score. The sum is an additive conditional utility; it does not claim

## Page 4

Confirmed exoplanets: a decision audit 17 October 2026
that discovery events or biospheres are independent. Optimizing the chance of at least one life detection
would require those additional probabilities and correlations. The oracle is hypothetical knowledge of
the scenario, not a feasible adaptive observation schedule.

3 A frozen catalog and an explicit evidence audit

We queried the NASA Exoplanet Archive Planetary Systems Composite Parameters table on 17
October 2026 at 17:17 UTC, retrieving 113 columns for 6,451 planet rows and 4,847 host labels (NASA
Exoplanet Archive, 2026). The composite table increases completeness by combining literature values;
it is not guaranteed to represent one internally consistent stellar/planetary solution. The archive
query, unmodified CSV, source references, retrieval timestamp and SHA-256 checksum accompany this
manuscript.
The initial status rule requires the archive controversy flag to be zero, leaving 6,393 planet rows. The
atmospheric screen then requires either a measured transit radius Rp ≤ 3R⊕, or, where no measured
radius is available, a measured mass or minimum mass ≤ 10M⊕. Archive radii marked as calculated,
mass–radius predictions, and quoted upper limits are not treated as direct measurements. A radius is
admitted as measured in this screen only when a transit and a non-calculated, non-limit radius are
present. This intentionally excludes unsupported radius claims for nearby nontransiting radial-velocity
planets.
We require positive distance and semimajor axis, a host temperature between 2,500 and 7,200 K,
and a luminosity estimate. Missing semimajor axes are completed from orbital period and stellar mass;
missing luminosities from radius and temperature. We recompute incident flux rather than accepting an
isolated insolation cell:
Sa =
L∗/L⊙
(a/AU)2
, S =
Sa √
1 − e
2
, (5)
where the second expression is the orbital time average for a Keplerian orbit. The broad screen is
0.1 ≤ S ≤ 3 in Earth-flux units. It is a computational inclusion rule, not a claim that the entire
interval permits a habitable surface. Nominal cuts can miss uncertainty tails; we do not infer population
occurrence from the selected set.
After the numerical updates below, the mechanical screen contains 191 planets. We retain a traceable
exception for GJ 682 b: although unflagged in the frozen archive, a primary radial-velocity reanalysis
failed to recover the proposed signals and conservatively treated the system as having no planets (Tuomi
et al., 2019). We exclude it from the curated atmospheric core while preserving its catalog row and the
reason. This leaves 190 planets in 167 host systems, including 66 planets within 30 pc and 133
with measured transit radii. Nineteen have both measured mass and radius; 43 fall nominally in our
conservative habitable-zone interval and 88 in the empirical interval. These counts differ from narrower
rocky catalogs because the scope, date, parameter reconciliation and composition gates differ.

3.1 Corrections that change decisions

Fifteen overrides are applied to a working copy, with each original value retained. They include three
distance entries; coherent stellar luminosity, radius and temperature updates for three hosts; a shared
inclination for GJ 1061; and eccentricity plus pericenter updates for Ross 128 b (Liebing et al., 2024).
They are sourced corrections or alternative stellar measurements, not adjustments made to obtain a
preferred ranking. Table 1 summarizes the most consequential cases.
For GJ 273, the original large luminosity uncertainty is present in the discovery literature; it is not
an archive transcription error. We use an independent SED/interferometric determination (Rabus et al.,
2019). Luminosity and radius are rescaled to the adopted parallax as L ∝ d
2 and R ∝ d, retaining the

## Page 5

Confirmed exoplanets: a decision audit 17 October 2026
Table 1: Selected audit findings. Angular separation is the nominal a/d scale, not a guarantee of access at an
observation epoch. All calculations preserve measured apparent brightness.
Object Audited input or identity Consequence and provenance
GJ 273 d : 5.9215 → 3.7861 pc;
updated L∗, R∗, T∗
a/d : 15.4 → 24.1 mas for b. A more precise stellar solution
gives S ≃ 1.23, warmer than the adopted conservative
interval. Gaia EDR3 (Gaia Collaboration, 2020); Rabus et al.
(2019).
Gl 725 B d : 6.8424 → 3.5230 pc a/d : 20.3 → 39.5 mas for c; radio power threshold improves
by 3.77×. Northern declination excludes this target from the
southern 39 m scenario. Cristofari et al. (2022); Ould-Elhkim
et al. (2026).
Wolf 1061 L∗ ≃ 0.01109L⊙ with much
tighter uncertainty
Removes a broad artificial tail of conservative-zone eligibility
for c; the planet still enters warm-edge empirical scenarios.
Interferometry and SED: Kane et al. (2017).
GJ 3323 L∗ = 0.003606L⊙ from
measured bolometric flux and
distance
c moves to Sa ≃ 0.226; b moves beyond the broad upper flux
cut. Mann et al. (2015).
GJ 1061 Shared i = 77+9
−13 deg in the
adopted dynamical solution
c and d have model-dependent true masses; dividing those
masses again by sin i would be incorrect. Dreizler et al.
(2025).
HD 20794 Archive f ↔ paper d at
P = 647.6 d
Match host and period. The archive’s d label refers to a
different, approximately 90-day signal. Nari et al. (2025).
GJ 414 A b Nontransiting; catalog radius
is a prediction
Preserve its radial-velocity mass information and do not infer
a measured terrestrial radius. Dedrick et al. (2021).
published fractional uncertainty conservatively. The Wolf 1061 update follows the same procedure using
Kane et al. (2017). For GJ 3323, the measured bolometric flux of Mann et al. (2015) is converted using
L = 4πd2Fbol, and radius follows from the Stefan–Boltzmann relation. These are coherent nominal
solutions, although full correlated uncertainty matrices are unavailable.
Distance corrections have different observational consequences in different channels. Reflected-light
photon counts use measured J magnitude, so they must not receive an additional inverse-square brightness
boost when distance changes. The corrected angular separation affects access and stellar leakage. A
radio power threshold is an inferred source luminosity for a fixed received flux, so its d
2
scaling does
change directly.
The audit also identifies a strongly inconsistent insolation entry for TOI-178 f; recomputed luminosity
and orbit remove it from the temperate screen. Source identity matters beyond isolated numbers: GJ
887 d is now a confirmed 50.77-day planet (Hartogh et al., 2026); GJ 3378 b has a revised 21.45-day
orbit and lower minimum mass (Robertson et al., 2026); and the archive includes GJ 251 c despite
“candidate” wording in its discovery paper (Beard et al., 2025). We state those distinctions rather than
silently mixing epochs or labels.

4 Catalog simulation and observing surrogates

4.1 Physical states, uncertain inclinations, and missing parameters

The main run draws 8,192 physical states for each of 190 planets, with 128 equally spaced mean-anomaly
nodes per state. The result is 1,556,480 physical draws and 199,229,440 orbital state evaluations, reused
across the scenario grid. Phase nodes are deterministic integration points, not independent posterior
samples.

## Page 6

Confirmed exoplanets: a decision audit 17 October 2026
Quoted upper and lower uncertainties define a two-sided Gaussian perturbation: a standard normal
variate is multiplied by the corresponding signed-side scale, then physically invalid states are rejected.
This preserves the reported asymmetric scales but is not a recovered publication posterior. Missing errors
are replaced by explicit defaults: 3% in semimajor axis, 0.05 dex in luminosity, 75 K in temperature, 1%
in distance, 20% in mass, and 8% in radius. Measured eccentricities are sampled on [0, 0.85]; otherwise a
Rayleigh distribution of scale 0.05 is used, truncated by any valid upper limit. Fixed-zero eccentricities
are therefore treated as uncertain rather than as measured circularity. A sensitivity test uses scales zero
and 0.15.
For a nontransiting radial-velocity planet with unknown inclination, true mass and geometry share
the same i:
Mp =
m0
sin i
, m0 = Mp sin i. (6)
At fixed m0, an isotropic orientation prior and a mass-density factor proportional to M−γinduce
p(i | m0, γ) ∝ sinγi. We use γ = 0, 1, 2 as a local inclination-prior stress test. Because the measured m0
is also perturbed without reconstructing its full likelihood and reference prior, this is not a complete
reanalysis under three mass-population posteriors.
To avoid unstable weights near a face-on orbit, states are drawn from the bounded mixture proposal
q(i) = 1
2
sin i +
1
π
, 0 ≤ i ≤
π
2
, ωγ(i) ∝
sinγi
q(i)
. (7)
This mixes isotropic and uniform-inclination draws. Every reported scenario average uses its matching
normalized importance weights; baseline observability uses γ = 1. The weights are bounded for the
tested γ values. Analytic inclination moments independently check the implementation.
Measured transit inclinations are retained. When a transiting object lacks one, a uniform impact
parameter between zero and one gives a circular transit-conditioned approximation. For GJ 1061 the
adopted common inclination is drawn once per system realization, and catalog dynamical true masses
are retained without a second deprojection. The missing mass–inclination covariance in that solution
remains a limitation (Dreizler et al., 2025).
For an unmeasured radius we compare two compositions. The compact case uses the Zeng et al.
(2016) relation with core mass fraction 1/3,
Rp/R⊕ = (Mp/M⊕)
1/3.7
, (8)
with 0.05 scatter in natural log radius, through 10M⊕. The published fit is calibrated for 1–8 M⊕; its
use below 1 and from 8 to 10 M⊕ is a stipulated extrapolation. A bounded continuation above 10M⊕ is
needed only for marginal observability; such draws fail every mass eligibility gate. The second case uses a
continuous, two-slope population surrogate inspired by Chen & Kipping (2017): R = 1.008M0.279 below
2.04M⊕ and a continuous M0.589 branch above, with 0.15 log scatter. It is not the Forecaster posterior.
For transiting planets with no measured mass, the compact inverse relation with 0.3 log scatter supplies
an assumed high-density completion; genuine mass upper limits truncate this distribution rather than
create a point mass at the limit. High density itself reduces scale height at fixed radius. No imputed
radius is subsequently described as a measurement.

4.2 Environmental scenario grid

Each environment weight is a product of an eligibility indicator and a chosen host-type weight:
wm = 1(size gate) 1(flux/climate gate) sm(T∗). (9)

## Page 7

Confirmed exoplanets: a decision audit 17 October 2026
This product defines a preference rule; it is not a factorization of empirically independent biological
causes. In particular, age, activity, stellar type and atmospheric escape are not multiplied as independent
survival probabilities.
The size gates are (Mmax/M⊕, Rmax/R⊕) = (3, 1.6),(5, 2),(10, 3), named small, standard and extended.
A measured radius uses its radius gate; otherwise a true-mass draw uses its mass gate. The extended
case admits larger temperate worlds without assuming their surfaces resemble Earth.
Conservative and empirical flux intervals use the one-Earth-mass polynomial boundaries of Kopparapu
et al. (2013, 2014). The conservative interval runs from maximum greenhouse to runaway greenhouse;
the empirical interval from early Mars to recent Venus. Coefficients are included in the reproducibility
package. Temperature is clamped to the calibrated 2,600–7,200 K range; TRAPPIST-1 lies slightly
below the lower boundary. These polynomials are not a climate model for each composition or planet
mass.
For each interval we compare an orbit-mean criterion using Eq. (5) with a condition requiring at least
90% of orbital time inside the flux interval. The latter is a climate-persistence stress test, not a claim
that organisms die whenever instantaneous flux crosses a boundary. Seasonal heat storage, atmospheric
circulation, ocean depth, tidal heating, spin state and greenhouse feedbacks require dedicated climate
calculations.
Host weights are flat (1, 1, 1), mildly penalizing (0.3, 0.7, 1), or strongly penalizing (0.03, 0.3, 1) for
T∗ < 3300 K, 3300 ≤ T∗ < 4000 K, and warmer hosts, respectively. These factors are deliberately
transparent. They are not atmospheric-retention probabilities, and hard temperature bins should not be
interpreted as physical discontinuities. Current cosmic-shoreline extrapolations provide a reason to stress
stellar assumptions, not a calibrated individual-world prior (Berta-Thompson et al., 2026). Counting
three size gates, two flux intervals, two climate rules, three stellar weights, two radius completions, three
inclination cases, and three instruments gives 648 scenarios per planet.

4.3 Reflected-light geometry and feature recovery

We solve Kepler’s equation at each phase. With star–planet distance r, phase angle α, and observer
distance d,
θ =
r sin α
d
, C = AgΦL(α)
(
Rp
r
)2
, ΦL(α) = sin α + (π − α) cos α
π
. (10)
The physical separation r, not projected separation, enters illumination. The stellar-reflex versus
planetary pericenter convention is reconciled for radial-velocity arguments of pericenter. Geometric
albedo is uniform from 0.05 to 0.35. A Lambert sphere and a fixed feature depth do not reproduce
wavelength-dependent clouds or surface reflection; more detailed alternatives already exist (Currie &
Meadows, 2025; Houelle et al., 2026).
The observing surrogate uses a 39 m aperture at λ = 1.27 µm, throughput 0.05, total exposure
100 hours, and an effective feature width of 0.04 µm. Stellar photon counts N∗ follow the observed J
magnitude with a local blackbody color correction. The J-band zero point is 1,594 Jy at 1.235 µm
(2MASS, 2008). A stipulated feature removes 20% of planet continuum flux over that effective interval.
This is a transparent equivalent-feature approximation; it does not include resolved molecular line lists,
telluric masks, detector noise, Doppler overlap, sky emission or a full high-resolution cross-correlation
pipeline. Consequently, it is not an ANDES exposure-time forecast or an oxygen detection prediction.
The contrast uncertainty and noncentral signal-to-noise ratio are
σ
2
C =
C + ℓ(θ)
N∗
+ c
2
sys, ρ =
0.2C
σC
, (11)

## Page 8

Confirmed exoplanets: a decision audit 17 October 2026
Table 2: Ground-based performance stress cases, all at 1.27 µm. The consortium raw-contrast benchmark
motivates the reference leakage; the remaining values are assumptions, not delivered specifications.
Case IWA / (λ/D) IWA (mas) Leakage at 20 mas csys
Ambitious 1 6.72 1.5 × 10−4 3 × 10−10
Reference 2 13.43 1.5 × 10−3 10−9
Difficult 3 20.15 1.5 × 10−3 3 × 10−9
where raw stellar leakage contributes photon noise and csys is a nonintegrating residual contrast floor.
The adopted leakage decreases as θ
−2
from its value at 20 mas, with a floor at one-hundredth of
that value. We keep this extrapolation explicit rather than treating the consortium’s single quoted
raw-contrast benchmark as a validated full curve.
For a one-sided five-sigma threshold, excess feature power is max{0, ΦN (ρ − 5) − ΦN (−5)}, multiplied
by the angular-access indicator, where ΦN is the standard-normal cumulative distribution function,
distinct from the Lambert phase law ΦL. This baseline-subtracted utility differs from literal detection
power by at most 2.87 × 10−7. Subtracting the noise-only baseline prevents distant, signal-free objects
acquiring nominal utility merely through false alarms. Random-phase recovery averages over phase;
best-phase recovery takes the maximum within each physical realization. Both assume that the full
exposure can be coadded at the chosen phase over repeated orbital cycles. They do not describe a
continuous 100-hour stare at a stationary orbital position. Real ephemerides, seasons, weather, telluric
velocity separation and scheduling may substantially reduce feasibility.
A southern-site access cut uses latitude −24.6 deg and requires maximum altitude of at least 30 deg.
It is a coarse visibility gate, not an airmass or calendar-time integration. All-sky scores are retained
only as comparisons for an otherwise similar observing capability. For HWO we adopt a notional 6 m
aperture, IWA 3λ/D and OWA 64λ/D at 0.76 µm, and continuum contrast at least 10−10, following
the LIFE X comparison (Carrión-González et al., 2023). This uses a gray-albedo approximation and
reports geometry plus contrast access only, not spectral recovery.

4.4 A transmission-feature ceiling

For transiting planets we calculate an intentionally simplified high-mean-molecular-weight atmosphere
with µ = 28, T = 255S
1/4 K and surface gravity from each mass–radius draw. A five-scale-height feature
has amplitude
H =
kBT
µmug
, ∆tr ≃
2Rp(5H)
R2
∗
. (12)
This is a feature envelope, not a biosignature amplitude, and the chosen temperature is a scaling
convention rather than a computed climate. A 4.3 µm bin of width 0.043 µm, collecting area 25.4
m2, throughput 0.3 and observed K magnitude estimate photon noise, using a 666.7 Jy zero point at
2.159 µm with the local blackbody color correction (2MASS, 2008). Equal in- and out-of-transit photon
budgets give the √2 noise factor. A circular duration with impact parameter 0.5 is used.
After 20 transits, we add residual floors of zero, 10 or 30 ppm in quadrature and compare feature
attenuation factors 1 and 0.3. These floors and attenuation factors are scenarios, not universal properties
of JWST. The output records 20P as an approximate cadence scale; twenty consecutive transit centers
actually span 19P, and visibility, observatory allocation and instrument scheduling add further constraints.
Unknown transit masses completed with Eq. (8) can be especially misleading for volatile-rich planets, so
these results are used to identify bottlenecks and reconnaissance targets, not to certify habitability.

## Page 9

Confirmed exoplanets: a decision audit 17 October 2026
10
−1 10
0
Orbit-mean stellar flux (Earth = 1)
10
0
10
1
10
2
Semimajor axis / distance (mas)
1 λ/D
2 λ/D
3 λ/D
6 m, 3λ/D at 0.76 μm
The geometric bottleneck is wavelength dependent
GJ 1002 c GJ 1061 d
GJ 251 c GJ 273 b
GJ 3378 b
GJ 514 b
GJ 887 d Gl 725 B c
HD 20794 f
LHS 1140 b
Proxima Cen b
TRAPPIST-1 e
Teegarden's Star c
Wolf 1069 b
3000
3500
4000
4500
5000
5500
Host effective temperature (K)
Figure 1: Audited planets within 80 pc in flux–angular-scale space. The ordinate is a/d; inclination, phase and
eccentricity determine actual projected separation. Horizontal lines illustrate the wavelength-dependent angular
bottleneck. Colors indicate stellar effective temperature, not habitability. HWO’s line is a long-horizon geometry
comparison.

5 Target results and their sensitivity

5.1 A nearby anchor and alternative habitat classes

Proxima Cen b is the strongest observational anchor in this scenario dictionary. It is first in 92.4%
and in the first five in 99.2% of southern-telescope scenarios. The result expresses unusually favorable
distance, angular scale and contrast combined with permissive compact-temperate states. It does not
establish atmospheric survival around an active late-M star. Evolutionary models permit very different
volatile and atmospheric outcomes depending on starting conditions (Ribas et al., 2016; Meadows et al.,
2018).
GJ 887 d is the most consequential recently confirmed alternative in our accessible sample. At
approximately 3.29 pc, its 0.212 AU orbit gives a nominal angular scale near 64.5 mas. Its minimum
mass, about 6.1M⊕, weakens a narrowly terrestrial interpretation but allows a larger reflecting area
in extended scenarios. The 3,688 K host also receives a different preference from late-M stars in the
penalized cases. These facts make it useful as a test of a different habitat class, not a demonstrated rocky
world. It is in the first five in 59.9% of the southern scenarios. Its discovery paper already identifies its
temperate interest (Hartogh et al., 2026).
Gl 725 B c is the clearest example of an input-driven promotion that does not translate into a southern
observing recommendation. The corrected 3.523 pc distance gives a 39.5 mas nominal separation instead
of 20.3 mas. It ranks in the all-sky first five in 91.5% of our scenarios. However, its declination near

## Page 10

Confirmed exoplanets: a decision audit 17 October 2026
Table 3: Representative audited targets. Values are nominal catalog/override inputs; derived quantities are not
new measurements.
Planet d (pc) M/M⊕ R/R⊕ S a/d (mas) South
Proxima Cen b 1.30 1.05† — 0.64 37.3 Yes
GJ 887 d 3.29 6.10† — 0.82 64.5 Yes
Gl 725 B c 3.52 3.40† — 0.47 39.5 No
GJ 273 b 3.79 2.89† — 1.24 24.1 Yes
GJ 1061 d 3.67 1.67 — 0.58 14.7 Yes
GJ 251 c 5.58 3.88† — 0.40 35.1 Yes
GJ 1002 c 4.85 1.36† — 0.26 15.2 Yes
Teegarden’s Star c 3.83 1.05† — 0.35 11.9 Yes
Wolf 1061 c 4.31 3.41† — 1.41 20.7 Yes
Ross 128 b 3.37 1.40† — 1.51 14.7 Yes
GJ 3323 c 5.37 2.31† — 0.23 23.5 Yes
TRAPPIST-1 e 12.43 0.69 0.92 0.65 2.4 Yes
TRAPPIST-1 f 12.43 1.04 1.04 0.37 3.1 Yes
LHS 1140 b 14.99 5.60 1.73 0.42 6.3 Yes
HD 20794 f 6.04 5.82† — 0.42 224.1 Yes
GJ 514 b 7.62 5.20† — 0.27 55.4 Yes
†: minimum mass M sin i, not true mass. Dashes mark unmeasured quantities. South means culmination at least 30 deg
at latitude −24.6 deg; it does not imply calendar or spectral feasibility. GJ 1061 d's true mass is conditional on the
coplanar dynamical model. HWO comparison targets remain longer-horizon cases.
+59.6 deg gives a maximum altitude of only 5.8 deg at the adopted southern site. Its near-term roles are
radio observations and supporting characterization; a northern future direct-imaging capability would
need its own performance and schedule analysis. The discovery authors already recognize the planet’s
habitable-zone location (Ould-Elhkim et al., 2026).
GJ 1061 d is a complementary compact-world case, because the selected dynamical model constrains
its true mass under coplanarity (Dreizler et al., 2025). Its nominal angular scale is only about 14.7 mas,
close to the reference IWA, making performance assumptions decisive. GJ 251 c offers a larger angular
scale but culminates at only about 32 deg at the southern site, just above our crude cutoff. A genuine
observing proposal must treat that low elevation more carefully. GJ 1002 c and Teegarden’s Star c
provide cooler compact scenarios, yet small separations and lower reflected flux limit their scores. Good
environmental arguments do not remove the geometric bottleneck.

5.2 A ranking is not a single durable ordering

Figure 2 makes several reversals visible. A permissive composition gate increases the role of GJ 887 d,
while an empirical warm-edge interval restores GJ 273 b and Wolf 1061 c. A late-M penalty can change
which of these physically different cases dominates. These reversals are informative: they identify the
assumptions that a future measurement or a better population model would need to resolve.
The all-grid, equal-time minimax portfolio is GJ 887 d, Proxima Cen b, and Wolf 1061 c, with
maximum fractional regret 46.0% relative to the scenario-specific three-target oracle. The solver reports
a zero optimization gap over 35 candidates with nonzero utility. This mathematical result should be
interpreted as an audit of the scenario set: the warm-edge member protects against empirical-zone
scenarios, even though it is weak under the conservative interval. It is not a recommendation to allocate
300 actual telescope hours before validating atmosphere, albedo, contrast suppression and seasonal
access. A conservative-zone-only calculation is also provided in the results package and discussed in
Appendix A.

## Page 11

Confirmed exoplanets: a decision audit 17 October 2026
Reference
standard, CHZ
Ambitious
standard, CHZ
Ambitious
extended, CHZ
Ambitious
late-M penalty
Reference
extended, EHZ
Ambitious
inclination stress
γ = 2
Proxima Cen b
GJ 887 d
GJ 273 b
Gl 725 B c
GJ 251 c
HD 20794 f
GJ 1061 d
GJ 1002 c
GJ 3378 b
Wolf 1069 b
Teegarden's Star c
GJ 514 b
Ross 128 b
HN Lib b
1.00 1.00 1.00 0.30 1.00 0.18
0.00 0.03 0.29 0.86 0.35 1.00
0.00 0.00 0.00 0.00 0.30 0.00
0.00 0.23 0.34 1.00 0.18 1.00
0.00 0.01 0.03 0.08 0.01 0.37
0.00 0.00 0.00 0.00 0.00 0.01
0.00 0.16 0.16 0.05 0.00 0.03
0.00 0.00 0.00 0.00 0.00 0.00
0.00 0.00 0.00 0.00 0.00 0.02
0.00 0.00 0.00 0.00 0.00 0.00
0.00 0.06 0.06 0.02 0.00 0.01
0.00 0.00 0.00 0.00 0.00 0.04
0.00 0.00 0.00 0.00 0.03 0.00
0.00 0.00 0.03 0.07 0.02 0.45
Conditional yield changes with the stipulated world and instrument
0.0
0.2
0.4
0.6
0.8
1.0
Yield / best yield in the same scenario
Figure 2: Selected all-sky scenarios, normalized separately to the best target in each column. CHZ and EHZ
denote the conservative and empirical flux intervals. Cells compare the conditional weight in Eq. (2); neither the
colors nor the ranks are probabilities of life. The all-sky view deliberately includes northern planets that fail the
southern-site cut.
Table 4: Reference, standard-size, conservative-zone, orbit-mean comparison with compact radii and γ = 1. SE
is numerical Monte Carlo error for the coupled expectation.
Planet E[w] E[D] E[wD] E[w]E[D] Ratio SE(J )
Proxima Cen b 0.978 0.428 0.408 0.419 1.0 2.65 × 10−3
Gl 725 B c 0.702 0.0155 1.41 × 10−3 0.0109 7.7 5.63 × 10−5
GJ 887 d 0.0861 0.0413 1.83 × 10−4 3.56 × 10−3 19.4 2.00 × 10−5
GJ 1061 d 1 2.69 × 10−5 2.69 × 10−5 2.69 × 10−5 1.0 6.29 × 10−7
GJ 251 c 0.581 1.67 × 10−3 4.51 × 10−6 9.68 × 10−4 214.7 1.35 × 10−7
GJ 1002 c 0.924 2.54 × 10−4 1.21 × 10−6 2.34 × 10−4 193.3 3.18 × 10−8
All-sky values are shown, so Gl 725 B c is retained even though the southern-site score is zero. Very large ratios at tiny
absolute scores are diagnostics, not strong discovery prospects.

5.3 Coupling errors are large for some attractive targets

The baseline values in Table 4 illustrate why marginal habitability and observability cannot simply be
multiplied. For GJ 887 d the product approximation is 19.4 times the coupled score, and for Gl 725 B c
it is 7.7 times the coupled score. The low-inclination, large-radius states that help marginal detectability
are often the same states that fail a terrestrial mass preference. Proxima’s correction is much smaller.

## Page 12

Confirmed exoplanets: a decision audit 17 October 2026
10
−4 10
−3 10−2 10
−1
Conditional yield
Proxima Cen b
Gl 725 B c
GJ 887 d
GJ 1061 d
Reference instrument / standard CHZ
E[w] E[D]
Coupled E[wD]
2.5 5.0 7.5 10.0 12.5 15.0 17.5 20.0
Product approximation / coupled yield
Shared latent states cannot be discarded
Figure 3: The product of marginal averages versus the coupled expectation in the reference instrument, standard-size, conservative-zone, orbit-mean scenario. All-sky values are shown. The right panel is a ratio diagnostic;
confidence intervals for the paired covariance and the joint estimator are supplied in the numerical tables. Ratios
involving very small denominators require particular care.
Table 5: Effect of the documented catalog-parameter policy in the baseline scenario. Both runs use 8,192 draws,
128 phases and the same base seed.
Planet Raw E[w] Audited E[w] Raw J Audited J
GJ 273 b 0.26 0 6.02 × 10−5 0
Gl 725 B c 0.702 0.702 1.91 × 10−5 1.41 × 10−3
Wolf 1061 c 0.231 0 1.34 × 10−3 0
GJ 3323 c 0.277 0.345 5.67 × 10−7 6.56 × 10−7
Zero denotes no eligible recovery in this finite simulation under this gate; it is not a zero probability of life. This joint
audit changes every documented parameter for each host, so it is not a distance-only experiment. Source policies are
retained in the supplement.
The sign and size of the effect are target- and scenario-dependent; covariance is not universally negative.
Neither the product approximation nor the corrected score is a life probability. Correcting this
statistical error improves internal consistency, but cannot repair a wrong climate gate, a wrong radius
completion, or an unrealistic instrument floor. Paired Monte Carlo uncertainties are reported for the
difference using physical-state draws as the independent sampling units.

5.4 The stellar-data ablation

The raw-versus-audited experiment in Table 5 changes only the documented parameter policy under
otherwise matching simulation choices. It separates two mechanisms that a naive uncertainty ranking
can conflate. A corrected distance can improve angular access. A more precise luminosity can remove
apparently favorable eligibility that arose from an unrealistically broad or superseded distribution. The
Wolf 1061 and GJ 273 examples show why a large uncertainty tail is not positive evidence for a habitable

## Page 13

Confirmed exoplanets: a decision audit 17 October 2026
Table 6: Illustrative high-µ, five-scale-height envelopes with a 10 ppm residual floor and no feature attenuation.
The noise is per effective 4.3 µm bin.
Planet Feature (ppm) Noise, 20 transits (ppm) Duration (h) 20P (yr)
TRAPPIST-1 e 72.5 34.1 0.76 0.33
TRAPPIST-1 f 61.5 32.0 0.88 0.50
TRAPPIST-1 g 55.3 30.7 0.97 0.68
LHS 1140 b 16.3 15.6 1.74 1.35
TOI-700 d 5.3 13.4 2.88 2.05
TOI-700 e 6.8 13.6 2.63 1.52
No atmospheric presence or biosignature is assumed to have been established. 20P is an approximate cadence scale;
visibility and allocated telescope time are additional constraints. The spectrum-injection experiment uses a separate
achieved-noise grid.
state. Coherent measurements can reduce a score while improving the quality of the decision.

5.5 Transmission reconnaissance and the longer-horizon comparison

The transmission ceiling supports TRAPPIST-1 e/f and LHS 1140 b as atmospheric reconnaissance cases,
while showing why a feature-scale calculation cannot establish that a biological attribution is feasible.
Table 6 reports selected envelopes and the modeled 20-transit noise. The assumed scale height, clouds,
mass completion and stellar residuals all matter. TOI-700 d/e are useful environmental comparisons,
but their larger host and small atmospheric depth impose a strong signal penalty in this calculation.
Current observations justify caution in a specific, evidential way. Four JWST PRISM visits of
TRAPPIST-1 e have variable stellar contamination and permit both bare-rock and secondary-atmosphere
interpretations (Espinoza et al., 2025; Glidden et al., 2025). Five NIRISS visits of f contain flares; the
reported absence of detectable unocculted-heterogeneity contamination in those visits does not guarantee
universally clean spectra, and high-mean-molecular-weight atmospheric limits depend on reduction
choices (Lim et al., 2026). Differential observations in a shared system can therefore be valuable for
learning about stellar nuisance and atmosphere retention even before life attribution becomes possible.
LHS 1140 b has measured bulk properties compatible with several interior and envelope interpretations,
with tentative atmospheric inferences rather than a confirmed nitrogen atmosphere (Cadieux et al.,
2024a,b). A 2026 ground-based helium report (Cherubim et al., 2026) is challenged by analyses of four
noncontemporaneous JWST visits (Bennett et al., 2026; Radica, 2026). Those reanalyses share the
same visits and must not be counted as independent observing campaigns. Helium nondetection is not a
demonstration that no atmosphere exists. This makes the target useful for resolving an atmospheric
question, not evidence that life is present.
For the 6 m, 0.76 µm geometry comparison, HD 20794 f—the 647.6-day planet called d in Nari et al.
(2025)—has modeled access 55.1%, far above GJ 514 b at 8.9%. Its nearby G-star host and larger angular
separation merit longer-horizon characterization. However, minimum mass near 5.8M⊕, unknown radius
and eccentricity near 0.45 leave composition and climate unresolved. An orbit-mean habitable-zone
position is not proof of a stable surface ocean; the residence criterion and a dedicated thermal-inertia
model ask different questions. This case is not promoted as a near-future HWO observation.

6 Simulated inhabited atmospheres versus observed spectra

The catalog surrogate assigns a feature to each eligible world, but a living planet need not produce
that feature. To test this failure directly we use published, physically calculated transmission spectra

## Page 14

Confirmed exoplanets: a decision audit 17 October 2026
rather than an invented oxygen/methane cartoon. The experiment reuses a finite set from Eager-Nash
et al. (2024a), archived by the authors at Zenodo (Eager-Nash et al., 2024b). It is a new observation-and-classification experiment on existing atmospheric calculations; we do not claim to have run a new
photochemical or general circulation model.

6.1 Physical templates and observation model

The archive contains ten PSG transmission spectra: four abiotic atmospheres, four ecosystem-1 inhabited
models at hydrogen outgassing rates of 0.1, 1, 10 and 100 Tmol yr−1, and two ecosystem-2 variants at
0.1 and 1 Tmol yr−1that include oxygen-consuming metabolisms. The code labels the latter oxic, but
this does not mean a modern oxygen-rich atmosphere. The source calculations use a prescribed common
early-Earth climate profile, a one-dimensional atmosphere and no cloud/haze treatment, with historical
model parameters for TRAPPIST-1 e. They do not establish which of those states the actual planet
occupies.
The headerless deposited total atmospheric transit contributions are fractional depths; multiplying
by 106 gives ppm, despite a saved GENERATOR-RADUNITS=ppm configuration flag. The approximately
0.004922 solid-disk depth is not in that column and is removed as a continuum nuisance in the experiment.
The units were checked against the source’s Figure 17 plus the configured solid-disk baseline, rather
than trusting the inconsistent units flag. We integrate the already R = 200 spectra into 184 logarithmic
bins between 0.8 and 5 µm, corresponding to R ≃ 100.4, with a flat within-bin response.
For wavelength bins k, l the declared covariance is
Kkl = σ
2
wδkl + σ
2
c
exp [−
| ln(λk/λl)|
0.05 ]
. (13)
We test σw = 2, 5, 10, 20, 30, 50 ppm and σc = 0, 5 ppm. These are achieved measurement scenarios, not
a claim that a given number of JWST visits reaches those precisions across the band. A free constant
and a slope in log wavelength are projected out before whitening. Known covariance and an exactly
specified finite template family make this an optimistic discrimination experiment.
Four spotted-star abiotic variants use an unocculted 3% blackbody spot fraction at 2,300 K against a
2,566 K photosphere. Airless continua with and without the same spots are also included. This is a
continuum stress test; stellar molecular lines, flares and evolving heterogeneity require richer models.
The admitted null therefore has ten members: four abiotic atmospheres, four spotted variants, and two
airless cases.

6.2 Finite-family likelihood and calibration

For a measured spectrum y, the test statistic is
T(y) = log


1
6
X
b∈B
p(y | b)

 − log "
1
10
X
a∈A
p(y | a)
#
. (14)
Here p(y | template) is the density of the continuum-projected spectrum: for an orthonormal projection Q
removing constant and slope, the mean is QTµ and covariance is QTKQ. Equal weights are computational
choices within each model family, not frequencies of biological ecosystems. The threshold is the largest
empirical 99th percentile obtained from 20,000 independent calibration draws for each admitted null. A
separate 20,000 draws per injected state estimate recovery and false-positive rates. Wilson intervals
quantify test-sample binomial uncertainty, conditional on the fitted threshold; they omit calibration and
model uncertainty. The nominal 1% target is not a finite-sample guarantee.

## Page 15

Confirmed exoplanets: a decision audit 17 October 2026
1 2 3 4 5
Wavelength (μm)
0
10
20
30
40
50
60
70
80
Atmospheric transit contribution (ppm)
(a) Published models; dashed = abiotic
Biotic 0.1 Tmol/yr
Biotic 1 Tmol/yr
Biotic 10 Tmol/yr
Biotic 100 Tmol/yr
1 2 3 4 5
Wavelength (μm)
−60
−40
−20
0
20
40
60
80
100
Atmospheric transit contribution (ppm)
(b) 20 ppm white + 5 ppm correlated
Biotic, 100 Tmol/yr
Abiotic, 100 Tmol/yr
Injection (1 in 4 bins shown)
2 5 10 20 50
White noise per R ≈ 100 bin (ppm)
0.0
0.2
0.4
0.6
0.8
1.0
Recovery fraction
(c) Biotic-model discrimination

0.1 Tmol/yr

1 Tmol/yr

10 Tmol/yr

100 Tmol/yr

Hidden biosphere
2 5 10 20 50
White noise per R ≈ 100 bin (ppm)
0.0
0.2
0.4
0.6
0.8
1.0
Recovery fraction
(d) One model, different questions
Atmospheric features
Biotic-model discrimination
With identical-spectrum null
Figure 4: Published atmospheric models under a new declared observation experiment. (a) Six inhabited and
four abiotic source spectra are used; the panel shows the four ecosystem-1 pairs. (b) One noisy realization; only
every fourth bin is plotted. (c) Biotic-family recovery at 5 ppm correlated noise, with a hidden-life counterfactual.
(d) Atmospheric-feature recovery, discrimination within the admitted finite families, and discrimination when an
identical-spectrum null is admitted. The precision axis is not an exposure-time forecast.
We also test an atmospheric-feature question against the two airless alternatives. This is separate
from biotic-family discrimination. To expose nonidentifiability we add two counterfactual diagnostics:
an inhabited but spectrally hidden state with an abiotic template, and an abiotic-labeled state with
exactly the spectrum of the strongest inhabited case. The latter is a mathematical adversary, not a
newly discovered abiotic production mechanism. If life and no-life hypotheses give identical distributions,
every decision rule satisfies TPR = FPR; increasing collecting area cannot remove that equality.

6.3 A living atmosphere can be easy to see and hard to identify

At σw = 20 ppm and σc = 5 ppm, all six inhabited atmospheres show atmospheric-feature recovery in
all 20,000 held-out trials. Yet the corresponding biotic-family recoveries range from 2.99% to 89.355%
(Table 7). The result demonstrates a difference between questions, not an observed atmospheric detection
on TRAPPIST-1 e.

## Page 16

Confirmed exoplanets: a decision audit 17 October 2026
Table 7: Independent held-out recovery at 20 ppm white plus 5 ppm correlated noise. Intervals are 95% Wilson
intervals for 20,000 trials and condition on the calibrated threshold and model family. Ecosystem 2 includes
oxygen-consuming metabolisms.
H2 outgassing Inhabited state Recovery (%) 95% interval (%)

0.1 Tmol yr−1 Ecosystem 1 5.665 5.35–5.99

0.1 Tmol yr−1 Ecosystem 2 2.990 2.76–3.24

1 Tmol yr−1 Ecosystem 1 9.495 9.10–9.91

1 Tmol yr−1 Ecosystem 2 6.135 5.81–6.48

10 Tmol yr−1 Ecosystem 1 25.660 25.06–26.27

100 Tmol yr−1 Ecosystem 1 89.355 88.92–89.77

Hidden-life counterfactual (abiotic-equivalent spectrum) 0.810 0.69–0.94
Strongest state with identical-spectrum null admitted 0.980 0.85–1.13
The strongest source state is recovered in 89.355% of trials against the admitted ten-model null,
falling to 0.98% after adding the identical-spectrum alternative. Its atmospheric features remain visible.
The source authors’ own twenty-transit NIRSpec/PRISM PandExo experiment did not robustly recover
the modeled methane features (Eager-Nash et al., 2024a); our uniform achieved-noise experiment is not
a revision of that instrument forecast. The hidden-life state gives only 0.81% apparent biotic recovery.
Such a state is not physically predicted by this counterfactual construction, but spectrally cryptic
biospheres are independently motivated by Earth-history modeling (Reinhard et al., 2017). A biological
population model that assigns every inhabited world a modern-Earth-like observable atmosphere would
omit an important class of false negatives.
Even 2 ppm white noise with the assumed 5 ppm correlated component recovers the weak ecosystem-2,
0.1 Tmol yr−1state in only 11.795% of trials. More precise white-noise measurements do not necessarily
solve a correlated-shape or model-degeneracy problem. Conversely, the strong source state is nearly
always recovered at sufficiently low noise within this finite null. Both outcomes matter; the experiment
is not designed to conclude that all atmospheric inference is impossible.

6.4 A missing null can dominate an apparently decisive result

An initial null set containing only the eight atmospheric abiotic/spot models gives a 99.53% biotic-call
rate for a flat spectrum and 97.495% for a spotted airless continuum at 20+5 ppm. Adding the two
missing airless alternatives reduces those rates to 0.035% and 0.030%, while strongest-state biotic
recovery remains 89.355%. The apparent certainty came from comparing several wrong atmospheric
explanations: the biotic family could be relatively closer to a flat spectrum even though the planet had
no atmosphere in the injection. This failure is retained as a named diagnostic rather than suppressed
after correcting the main analysis.
The largest false-positive rate among the ten admitted nulls is 1.125%. Other omissions are not
uniformly innocuous, but are much smaller than the airless failure. Omitting the highest-outgassing
abiotic family gives 1.285% at 10+5 ppm and 1.195% at 20+5 ppm. Test-only Wilson intervals for
those cases exclude 1%, but calibration uncertainty and multiple comparisons are not included. The
appropriate inference is modest miscalibration in those tested omissions, not proof that the untested
abiotic space is safe. Likelihood ratios should be accompanied by checks of absolute model adequacy
and an explicit accounting of missing hypotheses.

## Page 17

Confirmed exoplanets: a decision audit 17 October 2026
2 5 10 20 30 50
White noise per bin (ppm)
0.1, ecosystem 1
0.1, ecosystem 2
1, ecosystem 1
1, ecosystem 2
10, ecosystem 1
100, ecosystem 1
H₂ outgassing (Tmol/yr), biosphere
55% 32% 15% 6% 4% 2%
12% 8% 5% 3% 2% 1%
74% 50% 25% 9% 5% 3%
45% 28% 15% 6% 4% 2%
99% 90% 64% 26% 12% 4%
100% 100% 100% 89% 57% 17%
(a) Recovery across all six published inhabited models
0.1 1 10 100
Largest null-family false-positive rate (%)
All 10 admitted nulls
Omit 10^11 mol/yr
Omit 10^12 mol/yr
Omit 10^13 mol/yr
Omit 10^14 mol/yr
Omit spotted stars
Omit airless continua
(b) Omitted-null audit: 20 + 5 ppm
Nominal 1% target
Figure 5: Recovery and model-misspecification audit. Left: all six inhabited source states at 5 ppm correlated
noise. Right: the largest false-positive rate for each held-out null family at 20+5 ppm. Removing airless continua
creates a catastrophic failure; removing the tested geological or spotted families gives much smaller excesses. The
main analysis includes both airless alternatives. The finite admitted null is still not exhaustive.

7 Technosignatures: targets, power assumptions, and null information

Technology does not need to reside on the catalog planet that supplied a system’s discovery label.
A civilization could use another planet, an orbital platform, or an artifact; the probability of such
behavior is unknown. We therefore run the radio screen over all positive-distance, noncontroversial
confirmed-planet hosts, not just the atmospheric sample. This yields 4,792 unique host names. It is a
controlled targeting universe, not a claim that confirmed-planet hosts should be favored over equally
nearby stars lacking known planets.
We restrict numerical technosignature simulations to unresolved narrowband radio emission. Atmospheric pollutants, optical pulses, artificial illumination and waste heat have different signal and
background models; an Earth-technology comparison demonstrates how widely their detectable distances
differ (Sheikh et al., 2025). Our outputs are consequently radio-family priorities, not an all-technologies
civilization ranking.

7.1 A transparent radio sensitivity comparison

For an unresolved line, the minimum equivalent isotropic radiated power is
Pmin = 4πd2qr SEFD 10−26s
∆ν
npolt
, (15)
with SEFD in Jy, distance in meters, channel width ∆ν in Hz and dwell time t in seconds. The intrinsic
linewidth cancels when it is narrower than the matched channel; a broadband leakage signal cannot use
this formula unchanged (Price et al., 2020; Tusay et al., 2024). For SEFD=10 Jy, qr = 10, ∆ν = 1 Hz,
two polarizations and t = 300 s,
Pmin = 4.88467 × 108(d/pc)2 W. (16)

## Page 18

Confirmed exoplanets: a decision audit 17 October 2026
10
9 1010
Minimum detectable narrowband EIRP (W)
GJ 9066
Wolf 1061
Teegarden's Star
GJ 273
YZ Cet
GJ 1061
ε Indi A
GJ 15 A
Gl 725 B
Gl 725 A
Ross 128
GJ 887
ε Eridani
Barnard's star
Proxima Centauri
4.471 pc
4.306 pc
3.831 pc
3.786 pc
3.712 pc
3.673 pc
3.639 pc
3.562 pc
3.523 pc
3.521 pc
3.375 pc
3.287 pc
3.203 pc
1.827 pc
1.301 pc
Nearest confirmed-planet hosts: distance controls radio sensitivity
Audited distance
Raw catalog distance
Generic all-sky comparison: SEFD 10 Jy · 1 Hz · 300 s · 2 polarizations · S/N 10
Host labels are not independent pointings: Gl 725 A and B share the illustrative beam.
Figure 6: Illustrative narrowband source-power thresholds for nearby confirmed-planet hosts, with distance-audit
changes retained. Apparent radio attractiveness is conditional on the searched signal being emitted toward Earth
at an observed frequency and time. The model is not an actual all-sky instrument or a new SETI observation.
This generic all-sky comparison is grounded in a published receiver benchmark. It is not a claim that
one telescope sees every host with identical sensitivity. A 34 Jy column illustrates linear SEFD scaling.
EIRP is beam-equivalent power, not total civilization energy consumption.
Proxima’s threshold is 8.27 × 108 W, Barnard’s star’s is 1.63 × 109 W, and those of ϵ Eridani and GJ
887 are about 5.0–5.3 × 109 W. These last systems illustrate why a system radio target need not have
the highest score for contemporary terrestrial surface habitability. The corrected distances reduce Gl
725 B’s threshold by a factor 3.77 and GJ 273’s by 2.45. No probability of local life follows from these
received-flux comparisons.

7.2 Mock inhabited systems with explicit emitters

Conditional on a system producing a transmitter of the modeled family, let
x = log10(P/W), 7 ≤ x ≤ 15, p(x | β) ∝ 10−β(x−7), β = 0, 1, 2. (17)
Thus β = 0 is log-flat and dN/dP ∝ P
−(β+1). These are illustrative luminosity distributions, not
measured extraterrestrial priors. A Gaussian matched-filter response gives ppass(P) = ΦN [qr(P/Pmin−1)].
We apply a pipeline-recovery factor r = 0.94, motivated by a published injection experiment but not
assumed universal across facilities (Margot et al., 2023).
If the transmitter is on with duty fraction u, visits sample independent temporal states, and a

## Page 19

Confirmed exoplanets: a decision audit 17 October 2026
10
0 10
1 10
2 103
Distance (pc)
10
−12
10
−10
10
−8
10
−6
10
−4
10
−2
10
0
Conditional probability of detection
A Power distribution controls reach
p(log10 P) ∝ P
−β
β = 0
β = 1
β = 2
10
−3 10−2 10
−1 10
0
Per-visit transmitter duty probability
0.0
0.2
0.4
0.6
0.8
1.0
Detections per unit cost / one-visit value
B Revisits have diminishing returns
1 visit
3 visits
10 visits
A: Duty 0.1; 3 visits; beam intersects Earth. B: Above-threshold fixed power;
300 s per visit and equal source priors. All transmitter populations are hypothetical.
Figure 7: Dependence of conditional radio recovery on the assumed power population and temporal sampling.
The revisiting comparison assumes independent duty states, fixed power and beam geometry, equivalent target
priors, and no overheads. Real confirmation requirements and cadence correlations can alter the allocation tradeoff.
persistent beam intersects Earth with probability b, completeness after n visits is
cs = b
Z
p(x | β) [1 − (1 − ur ppass(10x))n] dx. (18)
Power and beam direction remain fixed across revisits. Putting b inside the exponent would incorrectly
resample the beam direction at each epoch. We test duty fractions 0.01, 0.1 and 1; one, three or ten
visits; and beam fractions 1, 10−2 and 10−4. Frequency coverage, Doppler-search bounds, residual
interference, signal lifetime and the retarded emission epoch remain additional conditioning variables.
We do not infer that a civilization exists “now” from a signal emitted a light-travel time d/c earlier.
For three 300-second visits at duty 0.1, conditional on the beam crossing Earth, Proxima’s completeness
is 0.195 for the log-flat power distribution, 0.00315 for β = 1, and 3.91×10−5for β = 2. The approximately
5,000-fold range comes from the stipulated emitter population, without changing the telescope or host.
There is no evidential basis for presenting the first value alone as the detection chance for an actual
civilization.
Numerical integration is checked against one million importance-sampling draws over 540 nearby-host
scenarios: twenty hosts, three power slopes, three duties and three visit counts. The largest quadrature–
Monte Carlo discrepancy is 3.40 Monte Carlo standard errors. The full host table retains thresholds;
the expensive population simulation is restricted to the nearest twenty labels. Other checks reproduce
radiometer scaling, normalized power densities, Gaussian amplitude recovery and the fixed-beam revisit
formula.

7.3 The same null observations can be informative or nearly empty

The nearest twenty host names occupy nineteen illustrative 9-arcmin-FWHM pointing groups because Gl
725 A and B share a beam. Sharing a beam saves observing time; it does not prove that host occurrence
states are dependent. We calculate both twenty independent-host occurrence trials and a nineteen-group

## Page 20

Confirmed exoplanets: a decision audit 17 October 2026
Table 8: Targets promoted by a stated scientific role. These are research priorities, not approved observing
proposals or inferred inhabited-world probabilities.
Role Targets Measurement or assumption that controls the next
decision
Near-future
reflected-light anchor
Proxima Cen b Validate achievable contrast and molecular-template
recovery; constrain atmospheric and stellar alternatives.
Alternative temperate
habitat
GJ 887 d Radius/composition, inclination, atmospheric survival
and realistic phase-dependent spectrum.
Compact-world
comparison
GJ 1061 d; conditional GJ
1002 c and Teegarden c
Small-IWA performance, ephemeris knowledge, radius
completion and cool-climate atmospheric requirements.
Northern opportunity Gl 725 B c; GJ 251 c Correct source parameters, northern facility
performance and actual elevation/scheduling; neither is
an automatic southern recommendation.
Warm-edge controls GJ 273 b; Wolf 1061 c; Ross
128 b
Climate and albedo can change eligibility and recovery
together; useful tests of hot-edge atmosphere models.
Transmission
reconnaissance
TRAPPIST-1 e/f; LHS 1140
b
First resolve atmosphere and stellar-contamination
alternatives; evaluate discriminatory spectral
information rather than a single line.
Longer-horizon direct
imaging
HD 20794 f (647.6-day
planet); secondary GJ 514 b
HWO architecture plus true mass, radius, eccentric
climate and wavelength-dependent contrast.
Near-term radio coverage Nearest confirmed-planet
systems, including Proxima,
Barnard’s star, ϵ Eridani,
GJ 887 and Gl 725 A/B
Search-frequency coverage, power distribution,
beaming, duty correlation, recovery calibration and
shared pointing cost.
alternative with one latent occurrence per group. Both use nineteen pointings and three visits, totaling
4.75 hours on source before overheads.
For a specified transmitter-family occurrence fraction η, hypothetical all-null data have likelihood
L(η | 0) = Y
s
(1 − ηcs). (19)
The product is conditional on independence of the modeled occurrence units and recovery events. A
uniform prior on η ∈ [0, 1] is used solely for the illustration. This treatment is related to existing
Bayesian SETI inference, not a new general theory (Grimaldi & Marcy, 2018; Margot et al., 2023).
With beam fraction and duty both one, the hypothetical log-flat population yields a 95% upper
bound of 0.203 under independent hosts, or 0.212 under group occurrence. With β = 1, the bounds
are about 0.949 in either model, almost the prior’s own 0.95 quantile. At duty 0.1 even the log-flat
independent-host bound weakens to 0.711. These are synthetic nondetections. They demonstrate that a
limit on a specified emitter family can range from informative to nearly uninformative without changing
the observed null outcome. They are not limits on civilization prevalence.

8 A practical, differentiated target program

The strongest recommendation is a program with different scientific jobs, rather than one universal
descending list. Table 8 summarizes the decisions supported by this analysis. None requires pretending
that a life prior has been measured.
The unusual cases here are not presented as discoveries of previously unknown habitable planets. GJ
887 d is newly relevant to a confirmed-only comparison and changes the composition tradeoff. Gl 725
B c is unusually sensitive to a catalog distance error and to hemisphere. GJ 273 b becomes easier to

## Page 21

Confirmed exoplanets: a decision audit 17 October 2026
resolve while losing conservative-zone support under better stellar data. Those are reproducible changes
in inference, which are more informative than an unsupported declaration that a planet was missed by
the field.
Atmospheric follow-up should first reduce uncertainties that can reverse a decision. For example, a
reliable radius or inclination for GJ 887 d addresses a different risk from another small improvement in
its orbital period. Better stellar and atmospheric models for TRAPPIST-1 can improve interpretation
across several planets, but shared nuisance does not make their atmospheric outcomes identical. A quiet
present-day optical light curve is not a measurement of integrated XUV exposure or initial volatile
inventory; neither a late-M veto nor an age-based civilization bonus is justified as a universal empirical
rule.
Cross-channel observing can be economical without conflating evidence. Radio observations of a
planetary system can continue while its atmosphere remains uncertain, and an atmospheric null does
not exclude an orbital technological source. Conversely, a nearby giant-planet system can be a good
radio pointing without becoming a terrestrial biosignature candidate. The common target name is a
coordination opportunity, not a common probability model.

9 Verification, limitations, and reproducibility

9.1 Checks that were actually performed

The orbital engine reproduces the exact time-averaged eccentric flux in Eq. (5) and the isotropic circular-orbit access probability p
1 − (IWA/(a/d))2 when the IWA is smaller than a/d. The covariance identity
holds numerically, and shuffling shared states removes the constructed covariance. The inclination
proposal reproduces known normalization and mean-cosine moments. A higher-resolution independent-seed run uses 16,384 physical draws and 256 phases for eighteen selected targets. Appendix A reports
the resulting changes, alongside the eccentricity and raw-catalog ablations.
The spectral engine preserves constant and linear functions under rebinning, reconstructs the sufficient
likelihood subspace to numerical precision, and agrees with an independent two-simple-Gaussian-hypothesis result. For the selected physical template pair at 20+5 ppm, analytic power is 91.937%
and simulated power is 92.074%; simulated false-positive rate is 1.023% against 1%. This validates the
likelihood implementation, not the truth of the atmospheric models. The strongest practical review
correction was inclusion of the previously missing airless alternatives, whose failure is explicitly retained
in Figure 5.

9.2 What would be needed for a stronger claim

There are five principal limitations. First, the environmental preferences are not biological priors.
Composition, surface water, atmospheric retention and abiogenesis are incompletely measured, and
the scenario set is not exhaustive. Subsurface biospheres, exomoons, free-floating planets, non-water
solvents, deliberately engineered habitats and many volatile-rich climates are outside the atmospheric
screen. A low score is not evidence of sterility.
Second, the physical uncertainty distributions combine published marginals and explicit defaults.
They do not include all stellar–planetary covariances, all original radial-velocity activity models, or a
planet-existence posterior. Source corrections are reproducible but not a replacement for re-fitting raw
data. Nominal screening cuts can exclude plausible tails, and the radius completions do not establish
composition.
Third, the ground-based and transit calculations are surrogates. Correlated albedo, clouds, surface
temperature and feature depths are not solved together; a higher reflected continuum can coexist

## Page 22

Confirmed exoplanets: a decision audit 17 October 2026
with weaker molecular features. The raw-leakage extrapolation, residual floors, constant equivalent
feature and idealized phase coaddition need facility-specific validation. The current calculations do not
include telluric line confusion, local sky background, exozodiacal light, detector systematics, stellar line
variability, calendar access or competition for time. Some omitted noise sources are decisive precisely
where the toy model is most optimistic.
Fourth, the atmospheric injection test spans a finite source grid with known noise covariance. It
measures discrimination among admitted models, not posterior life probability. Its airless failure
demonstrates why a large relative likelihood does not establish model adequacy. The exact-spectrum
adversary is a theorem illustrated numerically, not a physically established abiotic explanation for the
source’s strongest biosphere. Full climate/photochemistry retrievals, broader abiotic models, stellar
spectral libraries and independent validation observations would be needed for a claim of biological
attribution.
Fifth, the radio completeness is conditional on a signal class, power distribution, duty model, persistent
beam intersection and effective searched frequency. These are not inferred from human technological
history as though humanity were a random sample of civilizations. Shared pointing cost is separated
from host occurrence independence, but a real survey also needs coupled interference and recovery
models. The finite list of confirmed systems is not necessarily the optimal all-star radio survey universe.

9.3 Data and code availability

The accompanying reproducibility archive contains the unmodified dated catalog; the query and checksum
manifest; all fifteen parameter overrides and their source table; the public spectral archive and its verified
hashes; executable simulation and table-generation code; numerical results, diagnostics and vector figures;
and the LaTeX source. The principal programs are target_audit.py, spectral_injections.py, and
radio_audit.py. Seeds, sample counts, software versions and exact run commands are documented
in README.txt. Intermediate copies of literature PDFs are not required and are not redistributed. All
observing results in this paper are simulated; no new telescope data were collected.

10 Conclusions

The strongest defensible result is a conditional, auditable observing program. Proxima Cen b remains a
robust nearby reflected-light anchor within the tested assumptions. GJ 887 d is a useful alternative when
larger temperate worlds are admitted. Gl 725 B c is promoted by a corrected distance but excluded from
the southern telescope by sky position. GJ 1061 d tests a compact-world case close to the angular limit;
warm-edge targets remain useful controls rather than secure habitat winners. TRAPPIST-1 e/f and
LHS 1140 b are priorities for resolving atmospheric and stellar alternatives, while HD 20794’s 647.6-day
planet becomes compelling in a longer-horizon geometry comparison.
Three methodological findings are more durable than the precise ordering. Shared physical states can
make a product of separately averaged eligibility and observability seriously overoptimistic. Detecting
an inhabited atmosphere’s features can be much easier than attributing them to life, and a missing
airless null can create an almost universal false positive. Radio nondetections constrain a specified
emitter population only when the survey is sensitive to that population. These findings identify concrete
work that can improve the next target decision without manufacturing confidence about where life or
civilization actually exists.

## Page 23

Confirmed exoplanets: a decision audit 17 October 2026
Preparation and attribution
This research manuscript and its original computational experiments were prepared with AI assistance
in response to a research brief. Published atmospheric models and public catalog data remain attributed
to their original authors and providers. The work has not been submitted to arXiv or peer reviewed.
No human authorship, institutional affiliation or observational campaign is asserted.
A Further robustness results
A.1 Numerical convergence
The independent run uses seed 20261117, 16,384 physical draws and 256 phase nodes for eighteen
selected targets, compared with seed 20261017, 8,192 draws and 128 nodes in the main run. Among
11,664 matched scenario rows, the largest absolute change in J is 0.0134. The largest difference divided
by the quadrature sum of numerical Monte Carlo errors is 3.07; no matched row exceeds five such errors.
These comparisons are correlated across scenarios and are not 11,664 independent statistical tests. They
check physical-state Monte Carlo error and a simultaneous increase in phase-grid resolution; they do not
validate physical assumptions.
Replacing the eighteen main-run rows by their higher-resolution counterparts changes the largest
top-five scenario frequency by 1.85 percentage points. Proxima's first-place frequency changes from
92.44% to 92.13%. The minimax portfolio becomes GJ 887 d, Proxima Cen b, Wolf 1061 c with maximum
regret 45.17%. Candidates not in the validation subset retain main-run draws in this comparison. Low
absolute-score ordering remains more fragile than the leading target conclusion.
A.2 Dependence on the environmental decision set
Restricting the optimization to the 324 conservative-zone scenarios gives GJ 251 c, GJ 887 d, Proxima
Cen b with maximum regret 23.72% and mean regret 3.91%. The all-grid optimum instead contains
a warm-edge target because empirical-zone scenarios remain in its adversarial set. Thus portfolio
membership can express a decision maker's environmental scope rather than numerical evidence for life.
Both optimizations have zero reported mixed-integer optimality gap.
A.3 Unknown eccentricities
Fifteen selected targets were recomputed with the otherwise-unmeasured eccentricity Rayleigh scale
set to zero or 0.15, retaining reported eccentricity measurements. All other simulation rules, the base
seed and sampling counts remain unchanged. Targets with measured eccentricity need not change. The
resulting reference-scenario values are in Table 9; the full scenario outputs are retained. A larger unknown
eccentricity can improve angular access near an inner working angle and also alter the flux-residence
gate. It is not an unqualified habitability benefit.
At scale zero, Proxima is first in 92.13% of the southern scenarios; the largest top-five frequency
change is 0.93 percentage points. The corresponding portfolio is GJ 887 d, Proxima Cen b, Wolf 1061 c.
At scale 0.15, Proxima is first in 92.13% of the southern scenarios; the largest top-five frequency change
is 2.31 percentage points. The corresponding portfolio is GJ 251 c, GJ 887 d, Proxima Cen b.
A.4 An eccentric longer-horizon target
For HD 20794 f at its nominal eccentricity 0.45, instantaneous flux ranges from 0.178 to 1.238 Earth
units, while the orbital mean is 0.419. Only 32.2% of orbital time lies in the adopted conservative

## Page 24

Confirmed exoplanets: a decision audit 17 October 2026
Table 9: Sensitivity of the baseline conditional score to the default Rayleigh eccentricity scale, for selected targets.
Reported eccentricity measurements override this default.
Planet Scale 0 Scale 0.05 Scale 0.15
Proxima Cen b 0.408 0.408 0.4
Gl 725 B c 1.32 × 10−3 1.41 × 10−3 2.21 × 10−3
GJ 887 d 1.70 × 10−4 1.83 × 10−4 3.48 × 10−4
GJ 1061 d 2.69 × 10−5 2.69 × 10−5 2.69 × 10−5
GJ 1002 c 1.30 × 10−6 1.21 × 10−6 9.67 × 10−7
Teegarden’s Star c 1.66 × 10−7 1.66 × 10−7 1.66 × 10−7
GJ 251 c 4.39 × 10−6 4.51 × 10−6 5.89 × 10−6
flux interval at the nominal stellar temperature. This numerical residence diagnostic should not be
interpreted as the fraction of an orbit during which life exists: heat capacity, greenhouse response and
atmospheric circulation are absent. It explains why orbit-mean and persistence criteria can disagree
even for an attractive angularly resolved target.
B Parameter rules and supplementary diagnostics
The polynomial used for a habitable-zone boundary is Seff = S0 + aT′ + bT′2 + cT′3 + dT′4, where
T
′ = T∗ − 5780 K after clamping to 2,600–7,200 K. Table 10 reproduces the one-Earth-mass coefficients
used in code (Kopparapu et al., 2014). A repeated boundary calculation at a different assumed planet
mass would be a different scenario, not a correction to these explicitly specified ones.
Table 10: Habitable-zone coefficients used for all planets as environmental templates.
Boundary S0 a b c d
Recent Venus 1.776 2.136×10−4 2.533×10−8 −1.332×10−11 −3.097×10−15
Runaway 1.107 1.332×10−4 1.580×10−8 −8.308×10−12 −1.931×10−15
Maximum GH 0.356 6.171×10−5 1.698×10−9 −3.198×10−12 −5.575×10−16
Early Mars 0.320 5.547×10−5 1.526×10−9 −2.874×10−12 −5.011×10−16
For a self-normalized importance estimate, Ab =
P ωiwi/P ωi
, Bb =
P ωiDi/P ωi
, and bJ = P ωiwiDi/
P ωi
. The paired covariance estimate is ∆b = bJ − AbBb. We use the physical-draw influence term (wi −Ab)(Di −Bb)− ∆b , weighted by ωi
, for its Monte Carlo standard error. The joint estimator
uses wiDi − bJ. These quantify numerical integration error under the declared model, not uncertainty
over the model itself. The finite weights in Eq. (7) avoid the unbounded variance that a naive 1/ sin i
reweighting of purely isotropic draws would produce for the γ = 0 case.
For inclination density proportional to sinγi over [0, π/2], normalization integrals are (π/2, 1, π/4)
and E[cosi] = (2/π, 1/2, 4/(3π)) for γ = (0, 1, 2). The independent test uses 400,000 mixture draws.
The eccentric-flux check uses 100,000 deterministic mean-anomaly nodes. The spectral test projects
out a constant and log-wavelength slope, whitens the remaining covariance, and works in the span of
template differences. Discarded orthogonal noise cancels exactly in likelihood ratios; the low-dimensional
implementation is therefore a sufficient-statistic speedup rather than an approximation to the specified
Gaussian test.

## Page 25

Confirmed exoplanets: a decision audit 17 October 2026
0 50 100 150 200 250
Transit depth variation (ppm)
TRAPPIST-1 d
TRAPPIST-1 e
TRAPPIST-1 f
K2-9 b
TRAPPIST-1 g
LHS 1140 b
LP 890-9 c
TOI-4336 A b
TOI-700 e
TOI-1452 b
TOI-700 d
K2-3 d
Atmospheric-feature ceiling; this is not life identification
5 x modeled noise (20 transits, 10 ppm floor)
Five-scale-height envelope
Figure 8: Selected transmission envelopes under the standard-size, empirical-zone scenario, with no feature
attenuation and a 10 ppm residual floor. Markers show median five-scale-height amplitudes and 16th–84th
percentile spread; vertical strokes mark five times the modeled 20-transit noise. Sorting is by the conditional
feature score, not measured habitability. Unknown masses and high-mean-molecular-weight assumptions limit the
interpretation.
0.0 0.2 0.4 0.6 0.8 1.0
Group-level conditional transmitter prevalence η
0
2
4
6
8
10
12
Posterior density
Hypothetical all-null experiment: conclusions depend on assumptions
β = 0, u = 0.01, b = 0.01; 95% bound 0.950
β = 0, u = 0.1, b = 1; 95% bound 0.729
β = 0, u = 1, b = 1; 95% bound 0.212
β = 1, u = 1, b = 1; 95% bound 0.949
Uniform prior
Synthetic nulls: one abstract occurrence per each of 19 groups; three 300 s visits.
The separate 20-independent-host alternative is tabulated at the same pointing cost.
Beam sharing does not imply occurrence dependence. No new observations or civilization bound.
Figure 9: Posterior examples after explicitly hypothetical all-null radio observations. The displayed group-occurrence model has nineteen abstract latent groups; the numerical supplement also provides twenty independent-host trials at the same nineteen-pointing cost. A shared beam is not evidence for occurrence dependence.
Distributions close to uniform illustrate a nearly uninformative null for the specified weak-emitter or low-duty
population.

## Page 26

Confirmed exoplanets: a decision audit 17 October 2026

References

NASA Exoplanet Archive. 2026. Planetary Systems Composite Parameters Table. IPAC, California
Institute of Technology; snapshot retrieved 2026 October 17. doi:10.26133/NEA13.
Bohl, A., Lawrence, L., Lowry, G., & Kaltenegger, L. 2026. Probing the limits of habitability: a catalogue
of rocky exoplanets in the habitable zone. MNRAS, 547, stag028. doi:10.1093/mnras/stag028.
Brown, R. A. 2005. Single-Visit Photometric and Obscurational Completeness. ApJ, 624, 1010–1024.
doi:10.1086/429124.
Greco, J. P., & Burrows, A. 2015. The Direct Detectability of Giant Exoplanets in the Optical. ApJ,
808, 172. doi:10.1088/0004-637X/808/2/172.
Carrión-González, O., et al. 2023. Large Interferometer For Exoplanets (LIFE). X. Detectability of
currently known exoplanets and synergies with future IR/O/UV reflected-starlight imaging missions.
A&A, 678, A96. doi:10.1051/0004-6361/202347027.
Tuchow, N. W., & Wright, J. T. 2020. A Framework for Relative Biosignature Yields from Future Direct
Imaging Missions. ApJ, 905, 108. doi:10.3847/1538-4357/abc556.
Bixel, A., & Apai, D. 2021. Bioverse: A Simulation Framework to Assess the Statistical Power of Future
Biosignature Surveys. AJ, 161, 228. doi:10.3847/1538-3881/abe042.
Fields, B., Gupta, S., & Sandora, M. 2023. Information gain as a tool for assessing biosignature missions.
International Journal of Astrobiology, 22, 583–607. doi:10.1017/S1473550423000150.
Catling, D. C., et al. 2018. Exoplanet Biosignatures: A Framework for Their Assessment. Astrobiology,
18, 709–738. doi:10.1089/ast.2017.1737.
Walker, S. I., et al. 2018. Exoplanet Biosignatures: Future Directions. Astrobiology, 18, 779–824.
doi:10.1089/ast.2017.1738.
Spiegel, D. S., & Turner, E. L. 2012. Bayesian analysis of the astrobiological implications of life’s early
emergence on Earth. PNAS, 109, 395–400. doi:10.1073/pnas.1111694108.
Kipping, D. 2020. An objective Bayesian analysis of life’s early start and our late arrival. PNAS, 117,
11995–12003. doi:10.1073/pnas.1921655117.
Kopparapu, R. K., et al. 2013. Habitable Zones around Main-sequence Stars: New Estimates. ApJ, 765,
131. doi:10.1088/0004-637X/765/2/131.
Kopparapu, R. K., et al. 2014. Habitable Zones around Main-sequence Stars: Dependence on Planetary
Mass. ApJL, 787, L29. doi:10.1088/2041-8205/787/2/L29.
Zeng, L., Sasselov, D. D., & Jacobsen, S. B. 2016. Mass–Radius Relation for Rocky Planets Based on
PREM. ApJ, 819, 127. doi:10.3847/0004-637X/819/2/127.
Chen, J., & Kipping, D. 2017. Probabilistic Forecasting of the Masses and Radii of Other Worlds. ApJ,
834, 17. doi:10.3847/1538-4357/834/1/17.
Hartogh, C., et al. 2026. RedDots: Multiplanet system around M dwarf GJ 887 in the solar neighborhood.
A&A, 707, A93. doi:10.1051/0004-6361/202554984.

## Page 27

Confirmed exoplanets: a decision audit 17 October 2026
Ould-Elhkim, M., et al. 2026. The SPIRou Legacy Survey: Detection of a nearby world orbiting in the
habitable zone of Gl725B achieved by correcting strong telluric contamination in near-infrared radial
velocities with WAPITI. A&A, 705, A234. doi:10.1051/0004-6361/202555469.
Beard, C., et al. 2025. Discovery of a Nearby Habitable Zone Super-Earth Candidate Amenable to
Direct Imaging. AJ. doi:10.3847/1538-3881/ae0e20.
Robertson, P., et al. 2026. A Revised Mass and Period for the Habitable Zone super-Earth GJ 3378 b:
A Planet Straddling the Cosmic Shoreline. ApJ, 1005, 32. doi:10.3847/1538-4357/ae732b.
Nari, N., et al. 2025. Revisiting the multi-planetary system of the nearby star HD 20794: Confirmation
of a low-mass planet in the habitable zone of a nearby G-dwarf. A&A, 693, A297. doi:10.1051/0004-
6361/202451769.
Dreizler, S., et al. 2025. RedDots: Planetary masses in the GJ1061 system from planet-planet interaction.
A&A, 698, A114. doi:10.1051/0004-6361/202452490.
Liebing, F., et al. 2024. RedDots: Limits on habitable and undetected planets orbiting nearby stars GJ
832, GJ 674, and Ross 128. A&A, 690, A234. doi:10.1051/0004-6361/202347902.
Rabus, M., et al. 2019. A discontinuity in the Teff–radius relation of M-dwarfs. MNRAS, 484, 2674.
doi:10.1093/mnras/sty3430.
Kane, S. R., von Braun, K., Henry, G. W., Waters, M. A., Boyajian, T. S., & Mann, A. W. 2017.
Characterization of the Wolf 1061 Planetary System. ApJ, 835, 200. doi:10.3847/1538-4357/835/2/200.
Mann, A. W., Feiden, G. A., Gaidos, E., Boyajian, T., & von Braun, K. 2015. How to Constrain Your
M Dwarf: Measuring Effective Temperature, Bolometric Luminosity, Mass, and Radius. ApJ, 804, 64.
doi:10.1088/0004-637X/804/1/64.
Cristofari, P., et al. 2022. Estimating fundamental parameters of nearby M dwarfs from SPIRou spectra.
MNRAS, 511, 1893. doi:10.1093/mnras/stab3679.
Gaia Collaboration. 2020. Gaia EDR3. CDS VizieR catalogue I/350; source astrometry served by
CDS/SIMBAD, accessed 2026 October 17. doi:10.26093/cds/vizier.1350.
Tuomi, M., et al. 2019. Frequency of planets orbiting M dwarfs in the Solar neighbourhood. Submitted
manuscript; Appendix A.43, version 2. arXiv:1906.04644v2.
Dedrick, C. M., et al. 2021. Two Planets Straddling the Habitable Zone of the Nearby K Dwarf Gl 414A.
AJ. doi:10.3847/1538-3881/abd0ef.
Pallé, E., et al. 2025. Ground-breaking exoplanet science with the ANDES spectrograph at the ELT.
Experimental Astronomy, 59, 29. doi:10.1007/s10686-025-10000-4.
ANDES Consortium. 2026. SCAO Subsystem. Official consortium technical webpage, accessed 2026
October 17. https://andes.inaf.it/scao-subsystem/.
European Southern Observatory. 2025. Telescope first light for ESO’s Extremely Large Telescope now
planned for March 2029. Official project announcement ann25001, 2025 March 14; accessed 2026
October 17. https://www.eso.org/public/announcements/ann25001/.
NASA. 2026. HWO Technology & Engineering. Official mission architecture webpage, accessed 2026 October 17. https://science.nasa.gov/astrophysics/programs/habitable-worlds-observatory/
engineering/.

## Page 28

Confirmed exoplanets: a decision audit 17 October 2026
Konrad et al. 2022. Large Interferometer For Exoplanets (LIFE). III. Spectral resolution, wavelength
range, and sensitivity requirements based on atmospheric retrieval analyses of an exo-Earth. A&A,
664, A23. doi:10.1051/0004-6361/202141964.
Currie, M. H., & Meadows, V. S. 2025. There’s more to life in reflected light: Simulating the detectability
of a range of molecules for high-contrast, high-resolution observations of non-transiting terrestrial
exoplanets. Accepted in The Planetary Science Journal. arXiv:2503.08592.
Eager-Nash, J. K., Daines, S. J., McDermott, J. W., et al. 2024a. Simulating biosignatures from pre-oxygen photosynthesizing life on TRAPPIST-1e. MNRAS, 531, 468–494. doi:10.1093/mnras/stae1142.
Eager-Nash, J., Daines, S., McDermott, J., et al. 2024b. Simulating biosignatures from pre-oxygen photosynthesising life on TRAPPIST-1e [Dataset]. Zenodo, version 1, 2024 April 20.
doi:10.5281/zenodo.11002784.
Reinhard, C. T., Olson, S. L., Schwieterman, E. W., & Lyons, T. W. 2017. False negatives
for remote life detection on ocean-bearing planets: Lessons from the early Earth. Astrobiology.
doi:10.1089/ast.2016.1598.
Espinoza, N., et al. 2025. JWST-TST DREAMS: NIRSpec/PRISM Transmission Spectroscopy of the
Habitable Zone Planet TRAPPIST-1 e. ApJL. doi:10.3847/2041-8213/adf42e.
Glidden, A., et al. 2025. JWST-TST DREAMS: Secondary Atmosphere Constraints for the Habitable
Zone Planet TRAPPIST-1 e. ApJL. doi:10.3847/2041-8213/adf62e.
Lim, O., et al. 2026. Atmospheric Reconnaissance of TRAPPIST-1 f with JWST NIRISS SOSS: No
Evidence for the Transit Light Source Effect. AJ; arXiv version 2, 2026 August 31. doi:10.3847/1538-
3881/ae990a.
Cadieux, C., et al. 2024a. New Mass and Radius Constraints on the LHS 1140 Planets: LHS 1140 b Is
either a Temperate Mini-Neptune or a Water World. ApJL, 960, L3. doi:10.3847/2041-8213/ad1691.
Cadieux, C., et al. 2024b. Transmission Spectroscopy of the Habitable Zone Exoplanet LHS 1140 b with
JWST/NIRISS. ApJL, 970, L2. doi:10.3847/2041-8213/ad5afa.
Cherubim, C., et al. 2026. Helium escaping from the atmosphere of a nearby rocky exoplanet orbiting in
a habitable zone. Science. doi:10.1126/science.aea9708.
Bennett, K. A., et al. 2026. No Helium Detected in LHS 1140 b from Four JWST NIRISS/SOSS Transits.
Submitted manuscript, 2026 August 13. arXiv:2608.13473v1.
Radica, M. 2026. Strict Limits on Helium Absorption from LHS 1140 b from Four JWST NIRISS
Transits. Preprint, version 2, 2026 September 18. arXiv:2608.13470v2.
Price, D. C., et al. 2020. The Breakthrough Listen Search for Intelligent Life: Observations of 1327
Nearby Stars over 1.10–3.45 GHz. AJ, 159, 86. doi:10.3847/1538-3881/ab65f1.
Margot, J.-L., et al. 2023. A Search for Technosignatures Around 11,680 Stars with the Green Bank
Telescope at 1.15–1.73 GHz. AJ, 166, 206. doi:10.3847/1538-3881/acfda4.
Tusay, N., et al. 2024. A Radio Technosignature Search of TRAPPIST-1 with the Allen Telescope Array.
AJ, 168, 283. doi:10.3847/1538-3881/ad823c.
Grimaldi, C., & Marcy, G. W. 2018. Bayesian approach to SETI. PNAS, 115, E9755–E9764.
doi:10.1073/pnas.1808578115.

## Page 29

Confirmed exoplanets: a decision audit 17 October 2026
Sheikh, S. Z., et al. 2025. Earth Detecting Earth: At what distance could Earth’s constellation
of technosignatures be detected with present-day technology? AJ, 169, 118. doi:10.3847/1538-
3881/ada3c7.
Ribas, I., et al. 2016. The habitability of Proxima Centauri b. I. Irradiation, rotation and volatile
inventory from formation to the present. A&A, 596, A111. doi:10.1051/0004-6361/201629576.
Meadows, V. S., Arney, G. N., Schwieterman, E. W., et al. 2018. The Habitability of Proxima
Centauri b: Environmental States and Observational Discriminants. Astrobiology, 18, 133–189.
doi:10.1089/ast.2016.1589.
Houelle, M., et al. 2026. A broad exploration of climate and observability of close-in rocky exoplanets:
applications to Ross 128 b. Preprint. arXiv:2608.03857v1.
Berta-Thompson, Z. K., Wachiraphan, P., & Murray, C. 2026. The 3D Cosmic Shoreline for Nurturing Planetary Atmospheres. Submitted manuscript, version 2, 2026 March 19; first posted 2025.
arXiv:2507.02136v2.
2MASS. 2008. All-Sky Data Release Explanatory Supplement, VI.4a: Absolute Calibration.
IPAC/Caltech; Table 1 reproduces the calibration of Cohen et al. (2003). Updated 2008 December 28;
accessed 2026 October 17. Official calibration documentation.
