## Page 1

Earth from the Outside
An observer-centered feasibility atlas for planet discovery, habitability, biosignatures,
and technosignatures
Computational research preprint - Version 1.0

18 October 2026 | Rounded evaluation epoch: 2026.8

Abstract

We reverse the usual exoplanet observing problem: given Earth and the Sun, which external
locations could discover the planet, assess its habitability, measure evidence of a biosphere, or
detect technology, and on what timescales? We combine a frozen 2,034-source Gaia-based Earth
Transit Zone catalog, a published Virtual Planetary Laboratory quadrature spectrum,
photon-counting calculations, 300,000 random viewing configurations, and explicit light-cone
constraints. Within the supplied catalog union, a fixed-plane, zero-radial-velocity calculation yields
1,404 transit-zone members at catalog-coordinate epoch 2026.8; a separate first-order
apparent-to-kinematic timing sensitivity yields 1,400. Earth produces an 83.9 ppm central transit
lasting 13.1 h, whereas a 10 km atmospheric annulus contributes only 0.263 ppm. Under specified
6 m and 15 m space-coronagraph scenarios, a local oxygen A-band index in the reference
spectrum attains expected signal-to-noise ratio five in 94.3 h and 6.2 h, respectively, at 10 pc.
Complete-index angular access ends at 12.27 and 30.67 pc for the adopted 3λ/D inner working
angle. These are conditional feature-statistic sensitivities, not atmospheric retrievals or life
probabilities. A historical 20 TW narrowband radar scenario has a sensitivity-only range of 660
light-years for the chosen receiver, but our rounded 1997.0-2020.0 emission-era model occupies a
6.8-29.8 light-year shell at epoch 2026.8, with sparse beam illumination. Nearby observers sample
broadly modern oxygenated Earth but different technological epochs. The evidential stages need
not occur in order: an intercepted artificial transmission can precede optical planet
characterization. The calculations support a reproducible, assumption-dependent atlas of
observing opportunities; they do not identify extraterrestrial civilizations.
Keywords: Earth as an exoplanet; transit geometry; direct imaging; biosignatures; technosignatures; light-time;
reproducible simulation

1. Introduction

An external astronomer would encounter Earth through a chain of measurements: a periodic
change in the Sun, a faint companion in an image, a spectrum modified by an atmosphere and
surface, or radiation produced by engineering. Each measurement samples a particular Earth epoch
and requires a particular geometry, instrument, and observing program. Asking who could see
Earth is therefore an inverse observing-design problem. The unknown observer population is not
measurable from a stellar catalog; the accessible locations and conditional measurement
requirements are.
Earth Transit Zone studies identify a narrow region from which Earth can cross the solar disk [1],
[2]. Earth-as-exoplanet studies provide spectra against which to test observing methods [3]. The
recent Earth Detecting Earth comparison extends this reversal to human technological emissions
[4]. Here we connect these strands through a shared distance, geometry, and time convention. The
contribution is a transparent computational synthesis and a set of new scenario calculations, rather
than a new stellar survey, a complete atmospheric retrieval, or a claim of previously unknown
observers.
We use four operational outcomes. A planet detection establishes a companion consistent with
Earth. A habitability assessment combines irradiation, size or mass, and atmospheric or surface
evidence. A biosignature measurement detects a feature with a plausible biological
interpretation, followed by tests of alternatives. A technosignature measurement detects an
engineered emission or other evidence of technology. The last two require interpretation beyond

## Page 2

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
2
the significance of a single spectral feature. These outcomes can overlap, and their chronological
order is not fixed.
The central question is conditional: if an observer occupied a specified location, possessed a stated
instrument, and observed at the relevant time, would the available Earth signal be accessible and
measurable? We do not assign a probability that the location hosts a civilization. A nearby stellar
system serves as a spatial address for an observing platform; its own planets need not resemble
Earth, and the observed host star remains the Sun. In particular, an observer near an M dwarf does
not obtain the deeper Earth-Sun transit that would occur if Earth instead orbited that dwarf.

1.1. A selection function rather than one detection radius

(1)
For measurement class k, G denotes line-of-sight and orbital access; A denotes the presence of
photons from the relevant emission epoch; W denotes observing-window and beam overlap; and M
denotes adequate measurement sensitivity under the adopted model. These factors are logical
conditions or explicitly defined selection functions. Their product is not a probability of observers or
a posterior probability of life. For a radio beam, W may be zero despite excellent sensitivity. For
spectroscopy, G may be zero at a required continuum wavelength despite sufficient planet photons
at the band center.
Our spatial census is deliberately limited to the published 2,034-source transit-zone union within
the original 100 pc search. Direct imaging and radio are not restricted to that union. Sensitivity
curves therefore describe arbitrary external distances, while catalog counts refer only to the
supplied table. The distinction prevents a transit-selected sample from becoming an apparent
census of every potentially observing star.

2. Data, conventions, and observing scenarios

2.1. Frozen inputs and reproducibility

The stellar input is the machine-readable catalog accompanying Kaltenegger and Faherty [2],
obtained from the authors' public repository. It retains Gaia EDR3 identifiers, coordinates,
parallaxes, proper motions, fit-quality information, and published transit-zone interval labels. The
independent calculation uses inverse-parallax distances and the catalog's 2016.0 astrometric
reference epoch. We preserve the original tables and their hashes. This is a reanalysis of that frozen
sample, not an exhaustive update from every current Gaia or exoplanet catalog.
The spectral input is the characteristic Earth-at-quadrature file distributed with the coronagraph
software [5]. Its header attributes the radiance model to Robinson et al. [3]. That model family was
validated against Earth observations, including EPOXI; the particular distributed file is a model
realization, not raw spacecraft data or a measured October 2026 spectrum. Its exact date, cloud
map, and geographic realization are not specified. We retain its solar spectrum and use only 0.4-1.0
μm, avoiding the long-wavelength region in which thermal radiation contributes to the distributed
apparent reflectance.
Constants are explicit: Earth radius 6,371 km, solar radius 695,700 km, Earth mass 5.9722 × 1024
kg, solar mass 1.98847 × 1030 kg, orbital scale 1 au, and solar effective temperature 5,772 K. These
conventional values are consistent with standard planetary and nominal solar parameter
compilations [6], [7]. The small eccentricity of the real orbit, solar limb darkening, the Moon, and
the other planets are omitted from the analytic amplitude checks. The catalog uses a fixed J2000
orbital reference plane.
All reception and emission years are common inertial-coordinate labels at the accuracy used here,
rather than local calendars or claims about an observer's clock. The evaluation epoch 2026.8 is a
rounded decimal year. One parsec corresponds to 3.26156 light-years using the Julian year; a
source at 100 pc therefore sees Earth about 326 years earlier. Stellar kinematics, catalog time
labels, and actual photon reception are distinguished in Section 3 and Appendix A.

## Page 3

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
3
Parameter Adopted value Role or limitation
Space collecting diameter D 6 m; 15 m Conceptual external observatories; not asserted flown
capabilities
Throughput η 0.20 Common effective scalar; no extra encircled-energy
factor
Spectral resolving power R 140 Rectangular, photon-weighted bins for reflected Earth
Inner working angle 3λ/D Hard access gate; ideal full throughput outside the gate
Effective stellar leakage ε 10-10 Aperture-integrated stellar flux fraction; photon
background
Extraction solid angle Ω 1.5(λ/D)2 Converted to square arcseconds for diffuse sky
Local / one-exozodi sky 23 / 22 AB mag arcsec-2 Flat Fν; scenario surface brightnesses
Exozodiacal level z 3 Additional sensitivity sweeps use 1-10
Background reference Equal information to
science
Variance c
p
+ 2cb; see Section 6
Radio SEFD / dwell /
channels

10 Jy / 300 s / two

polarizations
Frequency-compatible, drift-corrected receiver scenario
Radio significance /
bandwidth
10 / matched signal width 1 Hz narrow-carrier benchmark; wider signals treated
explicitly
Table 1. Declared instrument and background scenarios. They are inputs to this study, not adopted requirements
or performance certifications for any mission. The 6 m class is motivated by current HWO concept work [8]; the 15
m class explores aperture dependence.

2.2. What is calculated and what is taken from literature

New calculations comprise catalog membership propagation, distances and information epochs,
Earth signal amplitudes, a transit precision experiment, orbital-orientation sampling, a
photon-counting oxygen-band statistic, background and calibration sensitivity tests, radio horizons,
and finite emission-era shells. Published atmospheric retrievals and technosignature studies supply
complementary context where this reduced model is insufficient. Their numerical benchmarks are
labeled as literature results. We do not generate new photochemical atmospheres, infer molecular
abundances, or treat simple blackbody curves as realistic thermal spectra.

3. Where could an observer see Earth transit?

3.1. The transit band and independent propagation

(2)
This is the circular-orbit condition for a fully interior transit. Including grazing configurations
changes the numerator to R⊙ + R⊕ and the half-width to 0.2689°. A random isotropic direction
therefore has a 0.4608% chance of a full-transit orientation, or 0.4693% if any grazing transit is
allowed. Earth's eccentric orbit makes the exact zone slightly nonuniform [1]. We use the catalog's
fixed ±0.264° band and ±0.132° restricted band for consistency with its selection.
(3)
The proper motions are converted from milliarcseconds per year to radians per year before
Cartesian propagation. Gaia's μα* already includes cos δ; multiplying by that factor a second time
would be incorrect. We rotate the propagated vector into the fixed J2000 ecliptic frame and
evaluate its latitude. Radial velocity is set to zero. This procedure reproduces all 1,402 catalog
memberships at the 2016.0 reference epoch, with no disagreements in that binary classification.

## Page 4

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
4
Selection within the frozen union Number
All catalog sources ever selected over the nominal ±5,000 yr interval 2,034
Inside the full band at 2016.0, independently reproduced 1,402
Inside the full band at catalog-coordinate epoch 2026.8 1,404
Inside the restricted band at 2026.8 713
Inside the full band and within 30 pc at 2026.8 47
Inside the full band after also requiring RUWE ≤ 1.4 1,164
Inside the full band with the separate first-order light-time sensitivity 1,400
Table 2. New membership calculations within a frozen, transit-selected catalog. RUWE is an astrometric fit-quality
statistic, not a habitability criterion. The last row uses a different time convention and is not a precision corrected
catalog.
Figure 1. The supplied transit-zone union. Left: propagated latitude at catalog-coordinate epoch 2026.8 against
ecliptic longitude at 2016.0; the shaded band is ±0.264°. One source lies outside the plotted latitude range. This
mixed-epoch visualization is a catalog diagnostic. Right: distance distributions for the whole union and current
fixed-band members. These counts characterize locations, without asserting observers or habitable planets.

3.2. A catalog epoch is not automatically a reception appointment

The published entry and exit offsets are explicitly measured from 2016.0. Thus Teegarden's +29
entry has source label 2045, and TRAPPIST-1's +1,642 entry has source label 3658. These labels
are preserved rather than shifted by the 2021 publication date. Values at the limits of the authors'
time grid are censored: a boundary at the last sampled year does not establish that the star actually
enters or exits then.
(4)
A physical observation connects Earth emission t
e
to the receiver's position at reception t
o
. The
orbital plane belongs to the emission event. Moreover, Gaia's astrometric model describes apparent
directions and explicitly distinguishes them from true kinematic positions [9], [10]. Simply adding a
light-travel time to a catalog crossing while leaving the observer at the old position is inconsistent.
We report the ordinary fixed-band catalog-coordinate result as the reproducible descriptive
baseline. Separately, advancing the apparent stellar track by approximately one light-time
estimates its simultaneous physical position in a zero-RV, stationary-Sun approximation. That
sensitivity produces 1,400 members, with 13 additions and 17 removals relative to the baseline. The
net difference of four hides 30 classification changes. Appendix A derives the convention

## Page 5

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
5
translation. Neither version includes a full stellar six-dimensional covariance model or an evolving
solar-system ephemeris, so the integer counts are exact outputs of their models, not exact counts of
actual receivers in the universe.
Location d (pc) L (yr) Published catalog-coordinate
window
Earth epoch seen at t
o
= 2026.8
Wolf 359 2.409 7.86 1970 to 2448 2018.9
Ross 128 3.375 11.01 -1041 to 1116 2015.8
Teegarden's Star 3.832 12.50 2045 to 2454 2014.3
GJ 9066 4.470 14.58 2862 to 3793 2012.2
TRAPPIST-1 12.467 40.66 3658 to 6028 1986.1
K2-65 63.104 205.82 -167 to beyond 7015 1821.0
K2-155 72.933 237.87 Before -2983 to 5134 1788.9
K2-240 73.043 238.23 Before -2983 to beyond 7015 1788.6
Table 3. Spatial examples and separate clocks. The seven planet-host labels are those identified in the 2021
catalog; Wolf 359 is an additional nearby location. Distances are recomputed from the published parallaxes.
Windows are source labels, not precision causal predictions. Negative years use astronomical numbering. The last
column is the stationary-distance information age, independent of whether a transit is available.
A fixed orbital plane is especially consequential for millennial entry dates. Planetary perturbations
change the Earth's orbital normal; this is distinct from precession of its spin axis. Solar-system
transit-zone work already recognizes this issue [11], and JPL supplies ephemerides and
bounded-validity approximate elements [12]. We therefore use the historical catalog windows to
illustrate changing access, without promoting their annual sampling or formal tabulated errors into
dynamical precision. Our independent propagation matches present memberships but does not
reproduce every historical endpoint exactly; slow crossings can differ by about 30 years. A
high-accuracy chronology would require full kinematics, covariances, and the Earth orbital normal
at emission.

4. Detecting the planet

4.1. Transit photometry and the observing calendar

(5)
The transit depth is independent of distance; the number of detected photons is not. We integrate a
5,772 K solar blackbody over 0.45-0.85 μm for a 1 m telescope with throughput 0.2. An explicitly
assumed independent residual precision of 20, 30, or 50 ppm per 6.5 h block is added in quadrature
to stellar photon noise. These residuals average down across independent blocks and transits. They
are not irreducible systematic floors. A long out-of-transit baseline is assumed known for this
discovery experiment.
(6)
At 10 pc, three central transits yield expected S/N = 10.26, 6.85, and 4.11 in the three
residual-precision scenarios. Requiring both S/N ≥ 7.1 and at least three events gives 3, 4, and 9
transits, respectively. The 7.1 threshold is motivated by the Kepler search statistic [13]; this
analytic exercise does not reproduce that pipeline's completeness or validation tests. With complete
observing coverage and a random initial orbital phase, these event counts require approximately
2-3, 3-4, or 8-9 elapsed years from the start of monitoring. Additional missed events increase the
calendar time.

## Page 6

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
6
At 100 pc, the 20 ppm scenario still gives S/N = 9.57 for three central transits, because the adopted
residual precision remains larger than photon noise. That result illustrates why geometry and
stability can dominate nearby-Sun photometry; it is not an asserted real survey yield. Noncentral
transits are shorter. In the fixed-band model, Wolf 359 has T14 ≈ 8.7 h, while G 157-77 has only
≈2.9 h. Neither receives the central-transit significance by default. Limb darkening, solar activity,
instrumental gaps, and false-positive rejection would need an actual light-curve
injection-and-recovery analysis.

4.2. Radial velocity and astrometry

(7)
(8)
Earth induces an approximately 9 cm s-1 edge-on solar radial velocity, and a 0.300 μas astrometric
semimajor axis at 10 pc. These are signal amplitudes, not achievable precision statements. The
radial-velocity amplitude has no distance factor, but obtaining the same spectral precision from a
fainter Sun does; stellar variability also competes with the signal. Astrometric information depends
on scan geometry, mission baseline, and separating parallax and the other planets. The one-year
Earth signal can be especially entangled with an observer's own parallax and scheduling cycles. A
weak or absent transit does not remove either channel.

4.3. Direct imaging across the sky

(9)
(10)
For the illustrative Lambert sphere with geometric albedo 0.2, quadrature contrast is 1.155 × 10-10.
Geometric albedo is different from Bond albedo, which appears in energy balance. At 10 pc Earth
reaches 0.1 arcsec projected separation. All orbital inclinations admit quadrature, including a
face-on orbit that remains at quadrature. Thus an observer outside the transit zone can image Earth
given adequate angular access and sensitivity. A hard 3λ/D gate at 0.76 μm permits quadrature to
12.76 pc for 6 m and 31.90 pc for 15 m; the gate is not a universal detection horizon.
We draw 300,000 isotropic viewing directions and independent orbital phases with a fixed random
seed. A trial passes if the separation exceeds the 0.76 μm IWA and contrast exceeds an illustrative 5
× 10-11. At 10 pc, the passing fractions are 0.5212 for 6 m and 0.6848 for 15 m, with Monte Carlo
standard errors about 0.0009. The analytic value for the 6 m case is 0.5191, consistent with
sampling variation. These are single-epoch geometric and brightness fractions, not detection
probabilities that include exposure, repeated visits, telescope availability, or the existence of
observers. Reusing the same draws correlates the numerical errors across distances.

## Page 7

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
7
Figure 2. Single-visit access in the illustrative Lambert-sphere model. Left: exact analytic curves with Monte Carlo
markers; each curve terminates at its hard angular cutoff. A contrast cut of 5 × 10-11 is imposed, without a
photon-exposure requirement. Right: the adopted phase law. Favorable separation and favorable brightness are
coupled through orbital phase. This phase experiment is separate from the fixed quadrature spectrum used below.

5. Recognizing a plausibly habitable world

An external observer can establish that a planet receives approximately terrestrial irradiation from
a Sun-like star before demonstrating liquid surface water. From an orbital period and stellar mass,
Kepler's law constrains the orbital scale; stellar luminosity then gives incident flux. Habitable-zone
models provide a physically motivated selection criterion [14], but the phrase likely habitable
should refer to a stated inference from multiple observations, rather than a probability assigned
solely by position in that zone.
(11)
The equilibrium temperature is an effective energy-balance quantity. It is not the surface
temperature, which depends on atmospheric composition, pressure, clouds, circulation, and surface
properties. Similarly, reflected brightness mixes radius and albedo. A transit radius, a dynamical
mass constraint, or a joint thermal-reflected analysis helps break those degeneracies. The signal
injection here is Earth, but an external analyst would not know that identity before interpreting the
data.
Measurement What it supports What remains ambiguous
Orbit + solar luminosity Earth-like incident irradiation Atmospheric and surface climate
Transit radius and/or
dynamical mass
Terrestrial scale; density when
combined
Interior and volatile inventory
H2O + CO2 spectroscopy Water-bearing atmosphere and
climate context
A hot steam atmosphere can also contain
water
Phase, glint, polarization Possible surface liquids and
scattering geometry
Clouds, aerosols, and viewing-angle
degeneracies
Thermal spectrum + time
dependence
Temperature, gases, heat
redistribution
Cloud tops, vertical structure, surface
pressure
Consistent visible + infrared
retrieval
Stronger habitability assessment Model inadequacy and remaining false
positives
Table 4. An operational evidence ladder for habitability. No row alone establishes a surface ocean. The present
calculations quantify access and selected photon statistics, rather than assigning a universal habitability
probability.

## Page 8

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
8
Earth observations demonstrate that ocean glint and ozone absorption can exist in disk-integrated
light [15]. Those features are not available at identical strength from every direction. At ecliptic
latitude β, a circular orbit spans phase angles from |β| to π - |β|; a pole-on observer cannot obtain
extreme crescent phases. Clouds and repeated rotation or season sampling matter. We therefore do
not attach the oxygen-index exposure time to a claim that oceans, pressure, temperature, and
radius have all been established in the same exposure.
Thermal measurements offer complementary information. An Earth-radius 255 K blackbody at 10 pc
has approximately 0.189 μJy at 10 μm and a planet/Sun contrast of 8.45 × 10-8. A 288 K blackbody
gives 0.362 μJy and 1.62 × 10-7; the difference illustrates why surface temperature cannot simply
replace wavelength-dependent brightness temperature. For a two-aperture Bracewell response, the
first off-axis transmission maximum at Earth's 10 pc separation requires B = λ/(2θ) ≈ 10.3 m at 10
μm. This baseline is an angular scale, not a complete interferometer design: collecting area, stellar
leakage, zodiacal light, thermal backgrounds, and modulation are still required.
As a separate literature benchmark, Mettler et al. combine empirical AIRS-based Earth spectra with
simulated LIFE noise and retrievals at 10 pc [16]. Their R = 50 or 100 experiments support
atmospheric and temperate-climate inference under the stated noise model. Multi-gas
interpretation is stronger at R = 50 with continuum S/N = 20, or R = 100 with S/N = 10 (continuum
S/N defined at 11.2 μm), than for the minimum R = 50, S/N = 10 methane case. This is a published
retrieval result; our blackbody check is not a reproduction of that analysis.

6. Measuring biosignature-bearing spectra

6.1. Why transmission is difficult for the real Earth-Sun system

(12)
A feature-minus-continuum effective height of 10 km produces only 0.263 ppm additional transit
depth. A 50 km illustrative height gives 1.32 ppm. These are annulus amplitudes for chosen
effective-height differences, not assigned strengths of every molecular band. The optical solar disk
greatly dilutes Earth's atmosphere. Refraction further prevents a distant observer from probing the
lowest roughly 12.75 km in a representative Earth-Sun transmission model [17]; it can suppress
access to lower-atmosphere water. Empirical Earth transmission spectra assembled from solar
occultations provide useful, distinct validation material [18].
(13)
For a favorable central geometry at 10 pc, D = 6 m, η = 0.2, R = 140 at 0.76 μm, and only solar
photon noise, this expression requires about 447 transit-equivalent integrations for the 10 km
feature, or 17.8 for 50 km. A 15 m aperture reduces them to 71.5 and 2.84. The factor two assumes
equal in-transit and out-of-transit photon totals; the neighboring spectral continuum is treated as
perfectly known. These values are lower bounds on an observing campaign, not robust
molecular-identification times. There is only about one Earth transit per year from a qualifying
direction, and a star may leave the zone before the accumulated requirement is met. Noncentral
durations, an independently noisy spectral reference, solar variability, and instrumental systematics
make the program harder.
The 3.3749 pc entries in the reproducibility table describe a hypothetical favorable transit geometry
at that distance. They do not imply a current transit from Ross 128, which lies outside the adopted
present band. This distinction illustrates a general rule: a distance-only sensitivity cannot replace a
location-specific access test. Direct imaging avoids the requirement for annual atmospheric
transits, while introducing demanding suppression and angular-access conditions.

## Page 9

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
9

6.2. Photon normalization of the physical reflected spectrum

(14)
The reference file supplies disk-averaged radiance Iλ and solar irradiance F⊙,λ at 1 au. Its
reflectance is already defined for quadrature. Applying an additional Lambert 1/π factor would
count the phase twice. We form logarithmically spaced, rectangular bins at R = 140, anchored to
0.760 μm, and integrate photons on the native grid. The input contains 97,822 rows; the visible
product contains 127 bins. The code performs the wavelength-unit conversion explicitly and verifies
that the planet/star count ratio equals Cj.
(15)
(16)
The background includes effective stellar leakage and diffuse local plus exozodiacal light, using the
explicit Table 1 scenarios. A 10-10 leakage fraction means the residual stellar flux integrated inside
our extraction aperture divided by total stellar flux. It is not a local point-spread-function peak ratio
and not an irreducible calibration floor. The common throughput is applied once; a more detailed
design would distinguish point-source encircled energy and diffuse-background throughput.
Published coronagraph noise models include additional terms omitted here [19].
The factor two for background arises from subtracting an independent estimate with the same
statistical information as the science exposure. It can be supplied by an equally informative
simultaneous region or by an additional reference exposure. We quote on-source science time; if a
separate reference requires an equal sequential exposure, it doubles that part of elapsed telescope
time. Orbit scheduling, rolls, slews, detector losses, and calibration overheads are additional. An
exactly known background would replace 2cb by cb but would still contribute shot noise in the
science photons.
For flat sky Fν, the sky photon count in a bin is proportional to AηΩFν ln(λhi/λlo)/h. With Ω ∝ (λ/D)2,
uniform surface-brightness sky counts at fixed R are approximately independent of D and source
distance, whereas the planet count scales as D2d
-2. A fixed background-to-planet ratio would
therefore give the wrong distance scaling in a sky-dominated regime. We omit detector noise,
wavelength-dependent throughput, dust structure, speckle covariance, and variability from the
baseline, then test one explicit residual-floor scenario below.

6.3. A measurable local oxygen statistic

(17)
We define S before generating noisy data. Four neighboring bins fit an affine continuum in
reflectance, and the mean predicted continuum is compared with three oxygen A-band core bins.
The complete linear weight vector q propagates uncertainty in the fitted continuum, including the
covariance of its predictions across the core. It annihilates any affine spectrum. Appendix B
specifies every wavelength and weight, making the estimator reproducible without a hidden
continuum choice.
The reference model yields S = 0.0199056, a fitted continuum mean of 0.0695601, and a mean
deficit of 28.62%. With the baseline backgrounds, expected S/N = 5 requires 94.3 h at 10 pc for 6 m
and 6.19 h for 15 m. With planet photons alone, the 6 m value would be 9.71 h; treating the
backgrounds as exactly known gives 52.0 h. The spread demonstrates why an exposure without its
noise convention is incomplete.

## Page 10

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
10
The statistic identifies a local depression at the expected oxygen-band location in a known injected
spectrum. It is not an oxygen-removed forward model, a measurement of oxygen abundance, or a
comparison against every alternative absorber. Curvature, cloud state, adjacent absorption, and
spectral-bin placement can bias the continuum bridge. Molecular identification requires templates
or a retrieval that marginalizes over these alternatives. The fixed reference realization also omits
the covariance introduced by observing a rotating, changing Earth over many hours.
Figure 3. A physical reference spectrum and a synthetic observation. Top: the published quadrature model,
rebinned to R = 140, and independent Poisson science-minus-background counts for a 6 m telescope at 10 pc. The
exposure is 94.3 on-source hours, chosen for expected oxygen-index S/N = 5. Gray at the red edge marks
wavelengths excluded by the adopted IWA. Bottom: the same realization near the oxygen A band; blue and orange
shading mark core and sideband bins. This realization yields 4.34σ and has not been selected to exceed the
threshold. Labels identify features in the injected model, not retrieval detections. Source model attribution: [3], [5].

## Page 11

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
11
Distance (pc) 6 m: expected 5σ (h) 15 m: expected 5σ (h) Geometry
2.41 1.9 0.3 Quadrature
3.37 4.1 0.5 Quadrature
5 11.2 1.2 Quadrature
10 94.3 6.2 Quadrature
12 177.7 10.0 Quadrature

12.47 Blocked by IWA 11.1 6 m loses a required red-side bin

20 Blocked by IWA 45.1 Quadrature

30 Blocked by IWA 177.7 Quadrature

Table 5. New oxygen-index exposure budgets for the reference Earth spectrum, with Table 1 assumptions. These
are science exposures for a fixed phase and spectrum. A blocked configuration cannot be repaired by integrating
longer within the same hard-IWA design. Values are conditional sensitivity calculations, not full atmospheric
retrieval forecasts.
All seven participating bins must be accessible. The longest bin edge is 0.790451 μm, so the
complete-index angular limits are 12.267 pc for 6 m and 30.667 pc for 15 m. These are slightly
inside the 0.760 μm core-only limits. TRAPPIST-1 at 12.467 pc therefore passes the 6 m
single-wavelength gate but fails the complete index as defined here. A different continuum
estimator or coronagraph design could change that specific boundary; the paper does not
extrapolate beyond the implemented definition.

6.4. Expected significance, repeated experiments, and calibration floors

An expected 5σ signal does not imply that every noisy experiment crosses a 5σ threshold. Twenty
thousand independent Poisson realizations at the nominal 6 m/10 pc exposure give an index
standard deviation of 0.004011, versus the predicted 0.003981, and 49.4% cross the threshold. For
a single Gaussian statistic with a known variance and a one-sided threshold of five, 95%
threshold-crossing probability requires expected S/N ≈ 6.645. In the photon-limited regime this is
1.766 times the exposure, or 166.5 h in the nominal example. Multiple testing and model
uncertainty require additional treatment; this calculation is a completeness illustration, not a global
false-alarm calibration.
(18)
For an illustrative independent, time-persistent per-bin contrast uncertainty of 10-11, the
oxygen-index asymptotic S/N is only 4.70, so no exposure reaches expected five. At 10-12, the
exposure grows from 94.3 to 95.4 h; at 3 × 10-12, it grows to 105.0 h. These values assume a
diagonal systematic covariance in contrast space. Actual correlated speckles can project differently
onto the index. Longer exposure cannot remove a component that does not average down.
Recent research illustrates why resolving power alone is not a guarantee. Gilbert-Janizek et al. find
useful R ≈ 140 visible measurements in their adopted Earth-history simulations [20]. Ruffio et al.
explicitly include spectral speckle correlations and find regimes favoring R > 1,000, with
low-resolution molecular information potentially suppressed [21]. The present independent-Poisson
calculation is a conditional benchmark within that design debate, not a final HWO instrument
recommendation.

6.5. A separate generic sensitivity experiment

(19)

## Page 12

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
12
To make the role of feature depth transparent, we also model two simultaneous, equal-width
channels: a continuum with count rate c
p
and an absorption channel with (1 - f)c
p
. Each has equal
statistical background subtraction. This is a separate blackbody/Lambert experiment, not the
seven-bin physical oxygen index. For f = 0.2 at 0.76 μm, the nominal 6 m/10 pc exposure is 765 h.
The larger number follows from using fewer spectral samples and a different feature definition; it
must not replace the oxygen result or be described as a contradictory calculation.
In the source-dominated limit, exposure scales approximately as d2/D2. With a distance-independent
sky background, it approaches d4/D4. We sample 30,000 independent parameter combinations:
geometric albedo uniform on 0.1-0.3, feature depth uniform on 0.1-0.4, exozodiacal level
log-uniform on 1-10, and throughput uniform on 0.1-0.3. At 6 m/10 pc the 5th, 50th, and 95th
scenario percentiles are 125, 658, and 4,698 h. These are sensitivity ranges under chosen input
distributions, not empirical confidence intervals or priors on civilizations.
Figure 4. A separate generic 20% two-channel feature experiment. Left: exposure versus distance for two
diameters and three diffuse exozodiacal levels, truncated at the 0.76 μm angular cutoffs. Right: a parameter sweep
at 6 m/10 pc, with distributions specified in the text. The sweep quantifies assumption dependence; it is not the
uncertainty distribution of the actual Earth spectrum.

6.6. From oxygen-bearing light to a biosphere inference

The most useful interpretation combines oxygen or ozone with water, carbon-bearing species,
atmospheric pressure and temperature constraints, and the Sun's spectral environment. Abiotic
oxygen can accumulate in some modeled dry, highly water-rich, or unusual initial volatile-inventory
worlds even around Sun-like stars [22]. A single oxygen feature therefore does not prove biological
replenishment. Methane can add information, but modern oxygenated Earth has a comparatively
weak methane signal, and the wavelengths needed to discriminate alternatives may be inaccessible
in the same visible coronagraph configuration.
For anoxic terrestrial atmospheres, methane together with CO2 and low CO can provide a different,
context-dependent biosignature [23]. That criterion is not automatically transferable to modern
Earth. A joint inference should explicitly compare living and nonliving forward models and account
for geochemical and photochemical sources and sinks. We do not specify the prior odds needed to
turn spectral data into a numerical probability of life. The physical oxygen index is one observable
that such an inference could use.

## Page 13

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
13

7. Detecting technology

7.1. Radio sensitivity with matched power and bandwidth

(20)
Here PEIRP is peak equivalent isotropic radiated power, g is the gain relative to the beam maximum
in the receiver direction, q is the power fraction in the matched spectral signal, B is its effective
bandwidth in hertz, and SEFD is in janskys. The expression follows the radiometer framework used
in radio technosignature searches [24]. It assumes frequency coverage, polarization-consistent
calibration, usable illuminated dwell time, and successful compensation for frequency drift. EIRP is
not the actual transmitter's electrical or radiated power; antenna gain concentrates the radiation.
(21)
The adopted receiver has SEFD = 10 Jy, two polarizations, 300 s illuminated integration, and
threshold ρ = 10. For the main narrowband examples, g = q = 1 and B = 1 Hz. A modulated radar
waveform need not put all its power into 1 Hz; these rows describe a narrow-carrier or
continuous-wave scenario. With fixed total power, distance scales as P1/2, SEFD-1/2, bandwidth-1/4,
and dwell time1/4. The weak time exponent makes extending range through integration expensive.
Source scenario Adopted EIRP Matched width Sensitivity-only range
Historical upgraded S-band radar 20 TW 1 Hz 660 ly (202 pc)
Historical earlier S-band radar 7 TW 1 Hz 390 ly
Documented DSN 70 m S-band setting 39.8 GW 1 Hz 29.4 ly
Spacecraft-downlink example 1.32 MW 1 Hz 0.170 ly
Broadband power comparison 4 GW 20 MHz 0.140 ly
Table 6. New radiometer calculations, conditional on on-axis signal interception and the stated receiver. Historical
radar power and upgrade eras are documented by NASA PDS [25]; the DSN value is approximately 106 dBW at 20
kW transmitted power in the 2022 services catalog [26]. Other characteristic power comparisons follow [4]. The 4
GW row is an illustrative total-power/bandwidth comparison, not a measured isotropic Earth leakage model.
For the DSN example, the documented 106 dBW is an EIRP capability at a specified power setting,
not a continuous emission history or a claim that all modulated power occupies 1 Hz. The 29.4 ly
range uses the explicit q = 1 carrier idealization; at q = 0.1 it becomes 9.31 ly. Real residual-carrier
fractions, pointing, and operations require a separate reconstruction [26].
A broadband terrestrial network cannot generally be collapsed into one narrow hertz of coherent
power. Real antennas point toward service areas and spacecraft, and the visible aggregate depends
on Earth rotation and geography. A dedicated mobile-tower study models those effects and finds
substantially weaker detectability than optimistic radar benchmarks [27]. Thus ordinary
communications and peak planetary radar must remain separate signal classes. Earth need not
transit the Sun for either to be detectable.

7.2. Causal shells and beam interception

(22)
NASA PDS specifies approximately 7 TW peak Arecibo S-band EIRP during 1974-1997 and
approximately 20 TW after the upgrade [25]. The telescope's destructive failure occurred in 2020
[28]. Using the rounded eras 1974-1997 and 1997-2020, the strongest-era radiation at epoch 2026.8
can occupy radii 6.8-29.8 ly, while the earlier-era radiation occupies 29.8-52.8 ly. These are
supports of the rounded emission-era model; subyear uncertainty in the historical boundaries shifts

## Page 14

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
14
the edges by up to about one light-year. They do not assert continuous operation or illumination of
every direction. Within the inner radius, those finite-era packets have already passed, although an
observer might have recorded them earlier.
The 660 ly sensitivity range is therefore not a present-day radius populated by our upgraded
historical radar signals. Earth's 1997 photons would reach a stationary observer 660 ly away
around year 2657, conditional on the emitted beam intersecting the receiver. General arrival
spheres with arbitrary onset dates are useful only if their meaning is equally explicit. Within the
frozen transit-selected union, a hypothetical continuously emitted signal beginning in 1900 has
reached 189 source distances by 2026.8, including 86 current catalog-coordinate transit-zone
members. Those numbers include no flux, beam, receiver, or observer-existence test.
Figure 5. Radio sensitivity and historical radiation support answer different questions. Left: the adopted
radiometer model; the shaded distance interval is the 2026.8 support in the rounded 1997.0-2020.0 radar-era
model. Right: finite emission eras create expanding shells after transmission stops. The shaded regions represent
possible radial support only. Actual beams illuminate sparse, intermittent parts of each region, and the figure is not
a map of terrestrial transmissions.
A top-hat beam with a one-arcminute half-angle occupies an instantaneous fraction (1 - cos α)/2 =
2.12 × 10-8 of an isotropic sky. This is an illustrative angular scale, not a measured chance that a
particular star receives Earth radar. Planetary targets are clustered and pointings repeat;
independent isotropic boresights would be an inappropriate model of actual operations. Sidelobes,
duty cycle, horizon limits, and dwell-time overlap require pointing records and antenna patterns.
For a moving receiver, the relevant ray points to its future interception position. The transverse
point-ahead scale v⊥/c is 20.6 arcsec for 30 km s-1, material compared with a one-arcminute
half-beam. Appendix A gives the constant-velocity null equation. We do not reconstruct historical
boresights, so no named system is asserted to have received a particular radar transmission. Band
membership and radar illumination are separate filters.

## Page 15

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
15

7.3. Atmospheric pollution, lights, lasers, and heat

Channel Defensible benchmark or calculation Implication for actual Earth
NO2 pollution Published cloud-free Sun-Earth simulation:
≈400 h at 10 pc with a 15 m LUVOIR-A
concept [29]
Conditional spectral sensitivity; natural
production and atmospheric degeneracies
remain
CFCs Published M-dwarf transit cases depend
strongly on an optimistic ≈10 ppm noise floor
[30]
That host-star advantage does not apply to
Earth transiting the Sun
Nightside city
lights
Published Earth-level lighting scenarios
require much stronger urbanization for
nearby-star detections with studied concepts
[31]
A reference sodium-lamp model is not a
census of all modern lighting
Optical
communications
Directed optical links have narrow beams and
a recent demonstrated emission history [33]
A useful sensitivity limit still requires causal
arrival and interception
Additional
thermalized power
This work: 20 TW / 1.223 × 1017 W = 1.64 ×
10-4
Effective-temperature increment ≈0.0104 K
in a global 255 K model
Table 7. Complementary technological observables. The literature rows are not simulated afresh here, and their
instruments, atmospheres, and significance definitions differ. They should not be combined into one precise
universal detection radius.
NO2 is a possible pollution tracer, but lightning, biology, and atmospheric chemistry also produce it.
A technological interpretation requires abundance and context, not merely an absorption feature.
We use the original photochemical study as the conditional benchmark [29], rather than adopting a
uniform global mixing ratio from local monitoring statistics. CFC studies identify more specifically
industrial molecules, yet their favorable M-dwarf transit geometry cannot be transferred to the real
Sun-sized host [30]. Multiple bands and alternative-absorber tests would still be necessary.
Artificial lighting and lasers illustrate different directional requirements. Nightside light is faint
relative to reflected daylight and depends on phase, cloud cover, urban area, and lamp spectrum
[31]. Laser communications can concentrate power into a much smaller solid angle, so a receiver
can obtain a strong signal only within the beam. NASA's DSOC demonstration first exchanged data
in November 2023 and completed its final pass in September 2025 [32], [33]. At October 2026,
those demonstrated emissions have not traveled even three light-years, irrespective of a sensitivity
forecast. They therefore cannot yet have reached the nearest stellar systems.
For an illustrative additional 20 TW fully thermalized on a 255 K Earth, the emitted thermal power
is 4πR⊕
2σT4
= 1.223 × 1017 W and the temperature increment is about 0.0104 K. This is a new
scaling calculation, not a measurement of present global anthropogenic heat. It assumes the power
is additional to the existing energy budget. Climate variability, albedo and emissivity uncertainty,
and redistribution would complicate any inference. Greenhouse radiative forcing is physically
distinct from direct waste heat. Large waste-heat or megastructure scenarios should not be
substituted for actual Earth merely because they are easier to detect.
A credible technological claim would benefit from repeat observations, independent receivers,
localization to the solar system or planet, consistent Doppler behavior, and rejection of natural or
instrumental alternatives. Narrowband engineering may be recognizable before an optical image
identifies Earth itself. The four outcome classes are consequently an evidence framework, not a
necessary sequence of discovery.

## Page 16

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
16

8. When: four distinct clocks

8.1. Earth evolution, photon age, observing cadence, and integration

The Earth-evolution clock says when a physical feature existed on the planet. The light-travel clock
says when those photons can reach another location. The observing-calendar clock says when
geometry and a working instrument allow useful data. The integration clock says how much data
the chosen statistic needs. Conflating them can move a predicted observation by decades,
centuries, or billions of years, depending on the context.
(23)
For nearby stationary-distance examples, L = d/c. The response relation adds acquisition, analysis,
and transmission delay; it is a causal lower bound without an assumed responding civilization. A
receiver at 10 pc at epoch 2026.8 sees Earth around 1994.2. If it first reacts to an Earth event
emitted in 2026.8, the event arrives around 2059.4 and an immediate return signal reaches Earth
no earlier than about 2092.0. If it instead responds to the older Earth photons arriving there now,
an immediate reply arrives here around 2059.4. These are different questions with different
answers.
Likewise, acquiring three annual transits requires waiting for the first available event and then at
least two further orbital periods. A 94 h spectroscopy exposure could be accumulated over several
observing windows; 94 h is not automatically four calendar days. Long integrations may average
over rotation, seasons, and cloud states. For a beamed technological signal the illuminated dwell
time, not the wall-clock duration of a receiver campaign, enters the sensitivity formula.

8.2. Earth through geological time

Terrestrial interval or model
epoch
Plausible remote evidence Meaning of the timing
Early Earth; published ≈3.9
Ga scenarios
CO2, water-related climate context;
little oxygen
Potential habitability can precede a remotely
evident biosphere
Archean biosphere, before the
major oxygen rise
Methane-related disequilibrium or
haze in favorable scenarios
Biology can exist while an oxygen search
returns a false negative
Proterozoic; published ≈2.0
and 0.8 Ga scenarios
Ozone may remain more
informative than visible O2 for some
atmospheres
Oxygenation does not immediately imply
modern oxygen-band strength
Broadly the last ≈0.5 Gyr A more favorable oxygen/ozone
biosphere proxy; evolving surface
pigments
A broad, model-dependent interval rather
than a universal detection onset
Industrial and
communications eras
Changing pollutants; radio, radar,
and optical links
Individual species and transmitter histories
have distinct beginnings and endings
Table 8. Historical interpretation, not a new continuous atmospheric reconstruction. Published Earth-evolution
spectra [34], [35] and geochemical false-negative analyses [36] motivate these broad regimes. Specific observer
dates require adding light travel and observing constraints to a physically justified Earth-state model.
A living planet need not advertise its biosphere in the gases we find easiest to measure.
Ocean-atmosphere recycling and limited atmospheric accumulation can conceal biological
production. Earth-history assessments suggest that oxygen and ozone were poor universal proxies
for much of the time before the last roughly 500 million years [36]. Consequently, the Great
Oxidation Event is not a defensible single date on which every capable external observer could
suddenly detect modern-strength oxygen.
All locations in the present 100 pc sample receive Earth light delayed by at most about 326 years.
They therefore sample essentially the same broad oxygenated geological era, while seeing markedly
different industrial and communications histories. A 326-year delay is crucial for technology and
negligible compared with a 500-million-year biological regime. This scale separation is why a local

## Page 17

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
17
atlas can reasonably use a modern reference biosphere spectrum while requiring separate
historical transmitter models; it still cannot reproduce the exact cloud state or pollution profile at
each retarded epoch.
The present stellar catalog must not be propagated backwards for gigayears with a straight line.
Galactic orbital evolution, stellar evolution, and the Earth-Sun system's changing environment
would all matter. Nor can very distant present-day observers be assigned a simple Euclidean
distance from a billion-year lookback time without cosmology. Geological visibility is therefore
treated as a separate physical history, not as a list of today's nearby stars claimed to have watched
ancient Earth.

9. Combining where, how, and when

Observer location Full ETZ
now?
Earth epoch
arriving now
O2 index hours: 6 m / 15 m Historical radar radial
support
Wolf 359 Yes 2018.9 1.9 / 0.3 1997-2020 era
Ross 128 No 2015.8 4.1 / 0.5 1997-2020 era
Teegarden's Star No 2014.3 5.6 / 0.7 1997-2020 era
GJ 9066 No 2012.2 8.3 / 1.0 1997-2020 era
TRAPPIST-1 No 1986.1 Blocked / 11.1 1974-1997 era
K2-65 Yes 1821.0 Blocked / Blocked Before the radar eras
K2-155 Yes 1788.9 Blocked / Blocked Before the radar eras
K2-240 Yes 1788.6 Blocked / Blocked Before the radar eras
Table 9. Worked combinations of the independent selection factors at rounded epoch 2026.8. ETZ is the
catalog-coordinate convention. Spectroscopy assumes the reference spectrum at quadrature and all Table 1
conditions; it is independent of transit access. Radar labels identify which emission era has the correct photon age,
not whether a beam was emitted or intercepted. Blocked means at least one required bin falls inside the angular
exclusion. The distant K2 systems are angularly blocked in both spectrograph designs.
Wolf 359: At 2.409 pc it is a close current transit-zone location in the reference model, receiving
Earth light from about 2018.9. The source is brighter and more widely separated than at the 10 pc
benchmark. The physical oxygen index requires about 1.85 h for the 6 m design at quadrature,
conditional on prior acquisition and calibration. The actual transit duration is shorter than the
central value, so planet discovery must use its own geometry. The recent radar era has the correct
photon age; illumination remains unknown.
Ross 128 and Teegarden's Star: These illustrate that current transit access is unnecessary for
direct imaging. Their Earth-information epochs are approximately 2015.8 and 2014.3, and the 6 m
quadrature index times are 4.06 and 5.55 h. Ross 128's published transit opportunity lies in the
past; Teegarden's source entry label lies in the future. Neither fact prevents an appropriately
equipped external imaging observatory from finding Earth outside a transit. The future catalog
label is not a precise receiving date after light-time and orbital-plane effects are considered.
TRAPPIST-1: At 12.467 pc it receives Earth light from around 1986.1. The published fixed-plane
transit entry label is 3658, so transits are unavailable in the present reference model. A 15 m
instrument gives an 11.1 h oxygen-index budget at quadrature. The 6 m instrument loses the
specified red-side continuum bin even though the 0.76 μm core itself is nominally outside the IWA.
Historical 7 TW-era radar has the relevant photon age, whereas upgraded 20 TW-era photons have
not yet arrived. These results concern observation of Earth and the Sun, without assigning
properties or observers to any TRAPPIST-1 planet.
K2-65, K2-155, and K2-240: These systems lie in the present fixed-band catalog but receive
terrestrial light from roughly 1821, 1789, and 1789. Under sufficiently stable transit photometry,

## Page 18

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
18
Earth could be identified as a small one-year planet; the biosphere is still broadly oxygenated. The
adopted 6 m and 15 m oxygen-index designs cannot resolve the required planet-Sun separation. At
about 63-73 pc, preserving the same 3λ/D gate through 0.790 μm requires approximately 31-36 m
collecting diameters just for angular access, before a sensitivity budget is considered. Human
radio-era photons have not reached these distances at the specified reception epoch.
These cases demonstrate three distinct outcomes: nearby imaging opportunities outside the transit
zone; current transit opportunities too distant for the chosen spectroscopy; and technological
photons whose emission era differs from modern Earth. A single ranking of stars would hide those
differences. A useful observing plan should retain a vector of access, sensitivity, information epoch,
and required evidence rather than one unqualified score.

10. Limitations, verification, and conclusions

10.1. Boundaries of the present calculation

The stellar analysis is restricted to a frozen, transit-selected union. It excludes a new all-sky census,
unrecognized sources outside the original selection, and a complete contemporary planet-host
crossmatch. Stars are treated as potential observing locations rather than inhabited systems. The
seven historical planet-host labels are retained only for orientation; no current count of confirmed
planets or habitability claim for their own planets is inferred.
The kinematic model holds the Sun and Earth's orbital plane fixed, neglects radial velocities in its
primary propagation, and does not propagate Gaia covariance matrices. Apparent-to-kinematic light
time is included only as a separately reported first-order sensitivity. The changing orbital plane,
eccentricity, observer-host orbital displacement, binary motion, and exact solar-system
ephemerides can alter boundary crossings. Annual entry labels and decimal information epochs
should not be read as observations timed to that precision.
The reflected-light calculation uses one model realization, a hard IWA, constant effective
throughput, a simple diffuse background, and independent photon statistics. It omits a wave-optics
coronagraph, realistic detector noise, temporal stellar and planetary variation, mission scheduling,
foreground-source confusion, and a full spectral covariance model. These omissions limit the result
to a conditional feasibility calculation. The local oxygen statistic and the generic two-channel
feature are intentionally separate observables. Neither supplies posterior abundances, surface
pressure, temperature, habitability, or life probabilities.
Radio uses declared matched bandwidths, power fractions, and receiver properties. Finite
emission-era support is not a beam reconstruction. A generic telescope located near another star
may have different local sky backgrounds, atmospheric transmission, and solar-avoidance
constraints from a telescope near Earth. We have not assigned those unknown environmental
quantities from the observer's stellar spectral type. No historical beam interception, technological
development date, or decision to observe the Sun is inferred.

10.2. Numerical verification and reproducibility

The companion bundle contains the raw stellar tables, a pinned physical spectrum with its software
license and attribution, independently written analysis scripts, numerical CSV outputs, figure files,
editable manuscript data, and the PDF renderer. The main simulations run without network access
once those inputs are present. The catalog and spectrum have SHA-256 records. Fixed random
seeds are 20261018 for orientation sampling, 20261019 for the generic parameter sweep, and
20261020 for the synthetic spectrum and Poisson verification.
Checks cover Earth's transit depth and duration, radial velocity and astrometry, inverse-square
photon scaling, radio power and bandwidth scaling, diffuse-sky scaling, all 2016 catalog
memberships, affine-continuum annihilation by the oxygen estimator, and equality of modeled
photon-count and spectral contrast ratios. Independent reviews checked the radiometer and
spectral normalizations. An initial plotting interpolation that extended beyond the IWA was replaced
with the analytic completeness curve. The 20,000-trial Poisson experiment tests the estimator
variance rather than merely mirroring its algebra.

## Page 19

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
19
Reproducibility commands and dependency versions are recorded in the bundle. The Python model,
published input data, and manuscript source make the assumptions inspectable and replaceable. A
full follow-up study could substitute a solar-system ephemeris, full Gaia phase-space posteriors,
time-resolved Earth spectra, a coronagraph covariance model, atmospheric retrievals, and archived
transmitter pointings. Those substitutions would improve specific unresolved uncertainties rather
than merely add more decimal places to the present scenarios.

10.3. Main conclusions

Earth is easiest to recognize as a transiting planet from a narrow band covering about 0.46% of
directions, but direct imaging can work from outside that band. In the frozen catalog and specified
fixed-plane model, 1,404 locations satisfy the band at epoch 2026.8. The physical causal
interpretation requires separate treatment of apparent astrometry and photon travel. Catalog
membership alone says nothing about telescopes or civilizations.
A planet-sized transit is much stronger than its atmospheric annulus. Annual Earth-Sun cadence
makes transmission spectroscopy expensive even in favorable photon-only calculations. In the
explicit reflected-light scenario, the physical oxygen A-band index is measurable at expected S/N =
5 in about 94 h for 6 m at 10 pc, or 6 h for 15 m. Its complete angular-access limits are about 12 and
31 pc. Those values are useful benchmarks only with their instrument, spectrum, covariance,
continuum, and time assumptions attached.
Habitability and biosphere interpretation require a consistent planetary context. Nearby locations
sample the same broad oxygenated Earth era, but a detectable oxygen feature is not automatically
biological proof. Much earlier Earth could host life that an oxygen-centered observing strategy
missed. Technological evidence can arrive through a different channel and precede an optical or
biological characterization.
The strongest historical radio signals are highly detectable if intercepted, yet their finite histories
produce sparsely illuminated shells whose present radii are far smaller than their sensitivity-only
horizons. A defensible answer to where, how, and when must preserve both limits. The resulting
atlas identifies conditional opportunities and testable requirements, without asserting that Earth
has actually been observed from any of these locations.
Authorship and status. This is a commissioned, AI-assisted computational research manuscript. It contains
original calculations and a selective primary-source synthesis, with cited external data and models. It has not
been submitted to arXiv or undergone external peer review. No institutional affiliation or human author identity
is assumed.

## Page 20

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
20
Appendix A. Time and geometry conventions
Let g(T) denote an apparent catalog position and r(t) a physical stellar position relative to an
approximately stationary solar-system barycenter. For constant distance and to first order in speed
divided by c, the observation of a star received here at T describes its earlier physical state: g(T) ≈
r(T - L). This convention is grounded in the distinction between astrometric and kinematic
parameters [9], [10]. The propagation used for Table 2's baseline simply treats g as the declared
catalog-coordinate track.
(24)
The first subtraction associates a catalog crossing label with the physical stellar event whose light
reaches Earth later. The second dates the terrestrial photons reaching that physical observer. As a
sign check, a star physically crossing a reference transit band in year 2000 at a distance of 10 ly is
seen crossing from Earth in 2010. The Earth photons that the star receives during its physical
crossing left in 1990. No single extra +L correction to the original catalog label expresses all three
events.
For the published Teegarden label 2045 and nominal L = 12.497 yr, this leading-order translation
gives physical reception near 2032.5 and Earth emission near 2020.0. For the TRAPPIST-1 label
3658 and L = 40.662 yr, it gives reception near 3617.3 and Earth emission near 3576.7. These are
demonstrations of the time convention, not precision revised entry forecasts. Changing distance,
radial motion, orbital-plane evolution, and the imperfect reproduction of catalog endpoints preclude
that interpretation. In the primary catalog-coordinate toy convention alone, by contrast, a label
used as a model reception event would have Earth emission at that label minus L. The conventions
must not be mixed.
For a physical receiver moving at constant velocity v, let r be its position relative to the transmitter
at Earth emission. The positive light-travel solution satisfies |r + vτ| = cτ:
(25)
The beam test uses (r + vτ)/|r + vτ| against the transmitter boresight at emission. A precision
transit test instead uses the projected Earth-Sun separation along that ray and the Earth orbital
state at emission, including the condition that Earth is in front of the Sun. This paper implements
the simpler band and radial-support approximations; it supplies the null equation to make explicit
what a future trajectory and pointing reconstruction would have to solve.
The source table's restricted-zone columns carry a .162 label, but the authors' code uses ±0.132°.
We follow the code's numerical definition. The source grid includes offsets -4999 to +4999, with
zero duplicated, so its end labels are censoring limits and its sample counts are not always elapsed
durations. Angular-error fields are preserved verbatim and are not used to assign probabilistic
boundary errors. Full covariance propagation would need the original Gaia uncertainty conventions.

## Page 21

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
21
Appendix B. Oxygen estimator and noise audit
Bin center (μm) Role Index weight qj

0.749220 Continuum sideband +0.299956

0.754591 Continuum sideband +0.285944

0.760000 Band core -0.333333

0.765448 Band core -0.333333

0.770935 Band core -0.333333

0.782027 Continuum sideband +0.214363

0.787633 Continuum sideband +0.199737

Table B1. Rounded weights of the predeclared local index. The full-precision vector is in the output CSV and code.
Weights sum to zero and annihilate a linear function of wavelength. The largest required bin upper edge is
0.790451 μm.
(26)
The two counts are independent in the simulation. Equal expected backgrounds cancel in the mean
and add in the variance. The code integrates the physical model in photons, forms fixed
ordinary-least-squares continuum weights, and evaluates the full linear estimator. It does not treat
a fitted continuum as noiseless. For correlated spectral residuals the variance is qTΣq; retaining
only a diagonal photon term is justified here solely by the declared scenario.
Numerical check Expected or analytic Simulation / result
Full-transit direction fraction 0.00460788 0.004720 in 300,000 draws

2016.0 ETZ membership 1,402 source members 1,402 reproduced; zero binary

disagreements
Oxygen index mean 0.01990560 0.01983262 in 20,000 Poisson trials
Oxygen index standard deviation 0.00398112 0.00401078
Threshold crossing at expected 5σ ≈50% for a single Gaussian
statistic
49.385%
Radio range at 20 TW, Table 1 receiver Power/bandwidth radiometer
equation
659.9685 ly
Table B2. Numerical verification. Monte Carlo values fluctuate; repeated use of a fixed sample also correlates
errors across scenario curves. Validation does not establish the completeness of the underlying physical model.
A spectral floor that is independent between bins but persistent in time contributes a fixed contrast
covariance. Our floor experiment maps it into reflectance units before applying q. A floor of 10-11
per bin gives limiting S/N = 4.70; this demonstrates a regime where increasing exposure cannot
reach the selected threshold. Smooth common-mode errors may cancel more strongly in an
affine-continuum index, while structured correlated errors can mimic or obscure molecular bands.
An actual observation requires its measured covariance, not a preferred outcome from the diagonal
proxy.

## Page 22

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
22
Appendix C. Audit trail and scope of source comparisons
The full source catalog and quadrature spectrum are archived in the companion bundle with exact
URLs and SHA-256 hashes. The spectrum is pinned to coronagraph repository commit
b5c58d315ed8d13c37f778364217a8fcda1ce773. Its distributed MIT license and attribution are
retained. Source identifiers are preserved as decimal strings in the stellar products. All generated
figures and tables can be reproduced from the included input bytes without an online catalog query.
Numerical comparisons must preserve the receiver assumptions of the cited work. As one check,
the printed radio equation in [4], evaluated with its printed one-polarization inputs, reproduces its
approximate radar and spacecraft-downlink scales, while two other reported values do not exactly
reproduce. We therefore use independently specified SI calculations throughout Table 6 and retain
a separate audit script. This observation does not determine what choices may have been made in
unpublished calculations.
The literature review is selective and includes relevant 2026 spectroscopy studies; it is not a
guarantee of complete coverage of every subsequent catalog change or instrument result. NASA's
HWO materials describe a concept in development [8]. The telescope cases in this manuscript
should be interpreted as hypothetical external capabilities, not forecasts of a civilization's
development date or claims that humanity already operates those full capabilities.

References

[1] Heller, R., & Pudritz, R. E. (2016). The Search for Extraterrestrial Intelligence in Earth's Solar Transit Zone.
Astrobiology, 16, 259-270. doi:10.1089/ast.2015.1358.
[2] Kaltenegger, L., & Faherty, J. K. (2021). Past, present and future stars that can see Earth as a transiting exoplanet.
Nature, 594, 505-507. doi:10.1038/s41586-021-03596-y.
[3] Robinson, T. D., Meadows, V. S., Crisp, D., et al. (2011). Earth as an Extrasolar Planet: Earth Model Validation
Using EPOXI Earth Observations. Astrobiology, 11, 393-408. doi:10.1089/ast.2011.0642.
[4] Sheikh, S. Z., Huston, M. J., Fan, P., et al. (2025). Earth Detecting Earth: At What Distance Could Earth's
Constellation of Technosignatures Be Detected with Present-day Technology?. The Astronomical Journal, 169,
118. doi:10.3847/1538-3881/ada3c7.
[5] Lustig-Yaeger, J., Robinson, T. D., & Arney, G. (2019). coronagraph: Telescope Noise Modeling for Exoplanets in
Python. Journal of Open Source Software, 4(40), 1387. doi:10.21105/joss.01387.
[6] NASA/NSSDC (accessed 18 October 2026). Earth Fact Sheet. NASA Goddard Space Flight Center. NASA Earth
Fact Sheet.
[7] Prša, A., Harmanec, P., Torres, G., et al. (2016). Nominal values for selected solar and planetary quantities: IAU

2015 Resolution B3. The Astronomical Journal, 152, 41. doi:10.3847/0004-6256/152/2/41.

[8] NASA (accessed 18 October 2026). Habitable Worlds Observatory. NASA Astrophysics. NASA HWO concept
overview.
[9] Lindegren, L. (2021). Astrometric source model. Gaia EDR3 Documentation, release 1.1, Section 4.3.3. ESA Gaia
EDR3 source-model documentation.
[10] Butkevich, A. G., & Lindegren, L. (2014). Rigorous treatment of barycentric stellar motion: Perspective and
light-time effects in astrometric and radial velocity data. Astronomy & Astrophysics, 570, A62.
doi:10.1051/0004-6361/201424483.
[11] Wells, R., Poppenhaeger, K., Watson, C. A., & Heller, R. (2018). Transit Visibility Zones of the Solar System
Planets. Monthly Notices of the Royal Astronomical Society, 473, 345-354. doi:10.1093/mnras/stx2077.
[12] NASA/JPL Solar System Dynamics (accessed 18 October 2026). Approximate Positions of the Planets. Jet
Propulsion Laboratory. JPL orbital elements and validity intervals.
[13] Seader, S., Jenkins, J. M., Tenenbaum, P., et al. (2015). Detection of Potential Transit Signals in 17 Quarters of
Kepler Mission Data. The Astrophysical Journal Supplement Series, 217, 18. doi:10.1088/0067-0049/217/1/18.
[14] Kopparapu, R. K., Ramirez, R., Kasting, J. F., et al. (2013). Habitable Zones Around Main-Sequence Stars: New
Estimates. The Astrophysical Journal, 765, 131. doi:10.1088/0004-637X/765/2/131.
[15] Robinson, T. D., Ennico, K., Meadows, V. S., et al. (2014). Detection of Ocean Glint and Ozone Absorption Using
LCROSS Earth Observations. The Astrophysical Journal, 787, 171. doi:10.1088/0004-637X/787/2/171.

## Page 23

EARTH FROM THE OUTSIDE Computational preprint | 18 October 2026
23
[16] Mettler, J.-N., Konrad, B. S., Quanz, S. P., & Helled, R. (2024). Earth as an Exoplanet. III. Using Empirical
Thermal Emission Spectra as an Input for Atmospheric Retrieval of an Earth-twin Exoplanet. The Astrophysical
Journal, 963, 24. doi:10.3847/1538-4357/ad198b.
[17] Bétrémieux, Y., & Kaltenegger, L. (2013). Transmission Spectrum of Earth as a Transiting Exoplanet: From the
Ultraviolet to the Near-infrared. The Astrophysical Journal Letters, 772, L31. doi:10.1088/2041-8205/772/2/L31.
[18] Macdonald, E. J. R., & Cowan, N. B. (2019). An Empirical Infrared Transit Spectrum of Earth: Opacity Windows
and Biosignatures. Monthly Notices of the Royal Astronomical Society, 489, 196. doi:10.1093/mnras/stz2047.
[19] Robinson, T. D., Stapelfeldt, K. R., & Marley, M. S. (2016). Characterizing Rocky and Gaseous Exoplanets with
2-meter Class Space-based Coronagraphs. Publications of the Astronomical Society of the Pacific, 128, 025003.
doi:10.1088/1538-3873/128/960/025003.
[20] Gilbert-Janizek, S., Lustig-Yaeger, J., & Krissansen-Totton, J. (2026). The effect of spectral resolution on
biosignature detection via reflected light observations of the Earth through time. arXiv:2604.26925; accepted for
The Astrophysical Journal. arXiv:2604.26925.
[21] Ruffio, J.-B., Steiger, S., Spohn, C., et al. (2026). Characterizing Earth analogs may require a moderate or
high-resolution spectrograph. Journal of Astronomical Telescopes, Instruments, and Systems, 12(4), 041020.
doi:10.1117/1.JATIS.12.4.041020.
[22] Krissansen-Totton, J., Fortney, J. J., Nimmo, F., & Wogan, N. (2021). Oxygen False Positives on Habitable Zone
Planets Around Sun-Like Stars. AGU Advances, 2, e2020AV000294. doi:10.1029/2020AV000294.
[23] Thompson, M. A., Krissansen-Totton, J., Wogan, N., Telus, M., & Fortney, J. J. (2022). The Case and Context for
Atmospheric Methane as an Exoplanet Biosignature. Proceedings of the National Academy of Sciences, 119,
e2117933119. doi:10.1073/pnas.2117933119.
[24] Enriquez, J. E., Siemion, A., Foster, G., et al. (2017). The Breakthrough Listen Search for Intelligent Life: 1.1-1.9
GHz Observations of 692 Nearby Stars. The Astrophysical Journal, 849, 104. doi:10.3847/1538-4357/aa8d1b.
[25] NASA Planetary Data System (accessed 18 October 2026). Arecibo Planetary Radar Transmitter. Instrument
context record, arecibo.305m.trans_s. PDS transmitter history.
[26] NASA/JPL (2022). Deep Space Network Services Catalog. Document 820-100, Revision H, 6 June 2022, Table 3-2.
DSN Services Catalog, Rev. H.
[27] Saide, R. C., Garrett, M. A., & Heeralall-Issur, N. (2023). Simulation of the Earth's radio-leakage from mobile
towers as seen from selected nearby stellar systems. Monthly Notices of the Royal Astronomical Society, 522,
2393-2402. doi:10.1093/mnras/stad378.
[28] Roshi, D. A., Aponte, N., Baddi, R., et al. (2021). The Future Of The Arecibo Observatory: The Next Generation
Arecibo Telescope. arXiv:2103.01367. arXiv:2103.01367.
[29] Kopparapu, R., Arney, G., Haqq-Misra, J., Lustig-Yaeger, J., & Villanueva, G. (2021). Nitrogen Dioxide Pollution as
a Signature of Extraterrestrial Technology. The Astrophysical Journal, 908, 164. doi:10.3847/1538-4357/abd7f7.
[30] Haqq-Misra, J., Kopparapu, R., Fauchez, T. J., Frank, A., Wright, J. T., & Lingam, M. (2022). Detectability of
Chlorofluorocarbons in the Atmospheres of Habitable M-dwarf Planets. The Planetary Science Journal, 3, 60.
doi:10.3847/PSJ/ac5404.
[31] Beatty, T. G. (2022). The detectability of nightside city lights on exoplanets. Monthly Notices of the Royal
Astronomical Society, 513, 2652-2662. doi:10.1093/mnras/stac469.
[32] NASA/JPL-Caltech (2023). DSOC First Light at JPL's Psyche Mission Support Area. NASA Photojournal, PIA26143,

16 November 2023. NASA DSOC first-light record.

[33] NASA/JPL (2025; accessed 18 October 2026). Deep Space Optical Communications (DSOC). Jet Propulsion
Laboratory mission overview. JPL DSOC mission record.
[34] Kaltenegger, L., Traub, W. A., & Jucks, K. W. (2007). Spectral Evolution of an Earth-like Planet. The Astrophysical
Journal, 658, 598-616. doi:10.1086/510996.
[35] Rugheimer, S., & Kaltenegger, L. (2018). Spectra of Earth-like Planets Through Geological Evolution Around
FGKM Stars. The Astrophysical Journal, 854, 19. doi:10.3847/1538-4357/aaa47a.
[36] Reinhard, C. T., Olson, S. L., Schwieterman, E. W., & Lyons, T. W. (2017). False Negatives for Remote Life
Detection on Ocean-Bearing Planets: Lessons from the Early Earth. Astrobiology, 17. doi:10.1089/ast.2016.1598.
