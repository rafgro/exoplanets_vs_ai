## Page 1

A thermal inversion that never switches off:
the CO2-band sign flip of 55 Cancri e and the origin of its dayside
variability
[Author name]1
1
[Affiliation, address]; [email]
Draft of 15 October 2026 — prepared for arXiv astro-ph.EP

Abstract

The ultra-short-period super-Earth 55 Cancri e changes its dayside brightness by more than a factor of ten on timescales of
days, and five JWST/NIRCam eclipses in 2022–2023 showed its 4.5µm occultation depth rising from 7±9 to 119 ppm within
six days while a cross-correlation analysis of the same frames found strong CO line emission only in the faintest epoch. We
re-analyse the published per-visit eclipse spectra (Patel et al. 2024, CDS J/A+A/690/A159) with a diagnostic that has not been
applied to them: the contrast between the 4.3µm CO2 ν3 band and the adjacent 3.9–4.2µm window inside each epoch, which
cancels the achromatic systematics that make the absolute depths pipeline-dependent and whose sign is the sign of the vertical
temperature gradient. The band is in emission in the two faint epochs (+23±6 ppm, 3.8σ) and absent or in absorption in the
three bright ones (+1±5 ppm; −12±8 ppm in the brightest), a 38±12 ppm flip within six days that is reproduced by two
independent pipelines and survives every band definition and error model we tried. A joint fit of all five epochs with one gas
layer of common temperature Tu and CO2-band optical depth τ over a continuum photosphere whose temperature alone varies
gives Tu = 2580 K (2300–3600 K), τ ≃ 0.3 (0.1–0.5), χ
2 = 6.3 for 3 degrees of freedom, and is preferred over epoch-by-epoch
blackbodies by ∆χ
2 = 26. The same layer predicts the epoch-to-epoch pattern of the CO line strengths (r = 0.85) and, when the
underlying deck is dark at 2.1µm, the otherwise impossible inverted colour of Visit 2 (2.1µm undetected while 4.5µm read
1400–1950 K). Tu equals, to within the errors, the radiative-equilibrium temperature of a thin grey layer on the dayside, 2300
K hemisphere-averaged and 2700 K substellar, which is the same whether the surface beneath is a bright 1500 K cloud top or
dark 2300 K magma. We conclude that the thermal inversion of 55 Cnc e is not created by the variability: it is the planet’s
ordinary radiative skin, always present at 2300–2700 K, and the variability is the continuum photosphere dropping beneath
it. Only a condensate deck can lower the 4.5µm photosphere by 1000 K within three orbits; gas cannot, because a ≥ 10 bar
CO2 atmosphere neither escapes nor outgasses on that timescale. A delayed magma-ocean/cloud feedback with parameters
inside published bounds reproduces the 4.5µm amplitude and the six-day recovery, and with a global-transport lag of ∼17 d the
47.3-day CHEOPS period. We give five falsifiable predictions for the scheduled JWST NIRCam, MIRI and NIRISS epochs.
Keywords: planets and satellites: atmospheres — planets and satellites: individual: 55 Cnc e — techniques: spectroscopic —
radiative transfer

1 Introduction

55 Cancri e (P = 0.7365 d, Rp = 1.88R⊕, Mp = 8.0M⊕;
Bourrier et al. 2018) is the brightest and best-observed ultra-short-period rocky planet, and the only one whose dayside
has been seen to change on the timescale of its own orbit.
Spitzer measured 4.5µm occultation depths between 47 and
176 ppm in 2012–2013 (Demory et al. 2016; Tamburo et
al. 2018); CHEOPS detected a mean optical occultation
of 12 ± 3 ppm with individual depths from zero to ∼50
ppm and a 47.3-day sinusoidal modulation (Demory et al.
2023), together with a 51.9-day modulation of the phase-curve amplitude (Meier Valdes et al. 2023); the transit depth ´
has never varied. JWST then made the problem acute. Five
NIRCam eclipses, four within one week, showed the 4.5µm
depth rising from 7±9 ppm to 119+34
−19 ppm in six days while
the simultaneous 2.1µm depth went 47 → −5 → 37 → 37
ppm and, five months later, 96±8 ppm, uncorrelated with
4.5µm (Patel et al. 2024). A single epoch had meanwhile
yielded a CO/CO2-bearing secondary atmosphere (Hu et al.
2024).
Three facts in this record have no published explanation.
First, the strongest molecular signal ever extracted from
the planet, an ∼ 8σ CO emission-line detection by cross-correlation at the native R ≈ 1600 of the grism, occurs in the
faintest epoch, with only ∼ 3σ hints in two others and nothing in the brightest (Snellen et al. 2026); the authors found
the line strength difficult to reconcile with a hydrostatic atmosphere unless a 1000 → 3500 K inversion sits at 1–10
mbar with CO2/CO < 10−3. Second, Visit 2 has an inverted
colour: a 2.1µm brightness temperature below ∼1250 K at
1σ and a 4.5µm brightness temperature of 1400–1950 K,
which no blackbody, cloud top or bare surface can produce.
Third, three days later the same planet showed CO2 in absorption (the V-shaped Hu et al. spectrum is Visit 4 of the
Patel et al. set).
The proposed mechanisms address the photometric amplitude rather than these spectral facts. A transient outgassed
atmosphere removed by escape (Heng 2023) changes the
4.5µm opacity but not the 2.1µm depth, and a 3D non-grey GCM fit to the Hu et al. spectrum now favours a ≥ 10
bar, CO2-rich atmosphere that neither escapes nor is replenished within days and whose weather produces variability
an order of magnitude too weak (Zhan & Koll 2026). A

## Page 2

magma-temperature/silicate-cloud limit cycle (Loftus et al.
2025) reproduces the 4.5µm brightness-temperature range
and predicts out-of-phase variability between bands, but says
nothing about emission lines. Tidally driven magma-ocean
waves (Farhat & Chiang 2026) redistribute heat on a hot
surface. External explanations — stellar activity, magnetic
star–planet interaction, a 3:2 spin–orbit resonance, a patchy
circumstellar dust torus — have been tested against the photometry (Section 5.3) but not against the one quantity a grey
screen or a change of viewing geometry can never alter: the
sign of a molecular band.
This paper makes that test. Section 2 describes the public
per-visit spectra; Section 3 defines a band-contrast index
that is immune to the achromatic common-mode systematics
of the data, a joint two-layer model, and a parameter-free
radiative estimate; Section 4 gives the results, including the
closure between the low-resolution band contrast and the
high-resolution line strengths; Section 5 interprets them and
confronts the alternatives; Section 6 lists predictions that the
scheduled JWST programmes can falsify.

2 Data

All spectra are the occultation-depth spectra published with
Patel et al. (2024) at CDS (J/A+A/690/A159, table e2), obtained through the VizieR mirror at Harvard. They cover
3.86–4.98µm from NIRCam F444W/GRISMR for the five
visits listed in Table 1 (GO 2084, PI Brandeker; Visit 4
is GO 1952, PI Hu). We use the three pipelines that provide binned spectra: Eureka (30 bins of 0.033µm, relative
depths), SPARTA (22 bins of 0.05µm, absolute depths), and
HANSOLO (30 bins, absolute, Gaussian-process detrended;
Visit 1 only, as a third check). The native-resolution stark
spectra (∼1150 channels, ±200 ppm each) are not needed
for band-averaged quantities. The Eureka spectra are placed
on an absolute scale by adding the stark white-light depth
of each visit from Patel et al. Table 1; only intra-visit differences are used in the primary analysis, so this offset does not
enter the main result.
All visits carry an achromatic common-mode systematic of 100–200 ppm of unknown origin (Patel et al. 2024;
Snellen et al. 2026); it shifts the absolute level of a visit
by tens of ppm between pipelines — the SPARTA window
depth of Visit 1 is 40 ppm where stark’s white light is 7 ppm
— but, being achromatic, it cancels in differences between
wavelength regions of the same visit. That is the property
the analysis below is built on.
Three spectral regions are defined by molecular physics
rather than by the data: the window W = 3.90–4.19µm,
where neither CO nor CO2 absorbs; the CO2 band C =
4.20–4.46µm, the ν3 fundamental and its hot bands; and the
CO band O = 4.47–4.98µm, the 1–0 fundamental, whose
integrated intensity is about ten times smaller than that of the
CO2 ν3 band. Region means are inverse-variance weighted
with the quoted per-bin uncertainties (symmetrised); the
empirical scatter of the bins inside each region is carried as
an alternative error estimate.

3 Methods

3.1 The band-contrast index

For each visit and pipeline we form the difference between
the mean depth in the CO2 band and in the window, corrected
for the slope that a featureless blackbody at the window
brightness temperature TW would itself produce between the
two region centres (4.33 and 4.05µm):
∆C = ⟨d⟩C − ⟨d⟩W −
[
D(4.33µm,TW )−D(4.05µm,TW )
]
,
(1)
D(λ,T) = (Rp
R⋆
)2 Bλ
(T)
Bλ(T⋆)
, (2)
with (Rp/R⋆)
2 = 332 ppm, T⋆ = 5172 K, and an analogous
∆O for the CO band at 4.72µm. The blackbody correction
is 0–3.4 ppm in the CO2 band and up to 7.5 ppm in the
CO band for the bright visits, and negligible for the faint
ones. Positive ∆C means the band emits more than the continuum beneath it, i.e. the band-forming gas is hotter than
the 4.05µm photosphere; negative means the reverse. Because the common-mode systematic is achromatic it enters
⟨d⟩C and ⟨d⟩W identically and cancels. The two pipelines
reduce the same photons, so their inverse-variance mean
is a pipeline-robust estimate of one measurement, not two;
we inflate its uncertainty by √2 and quote the larger of the
quoted-error and empirical-scatter estimates.

3.2 One gas layer over a variable photosphere

The minimal model that can change the sign of a band is
a continuum photosphere at Tc,i (free per epoch i) under a
single gas layer with temperature Tu and CO2-band optical
depth τ common to all epochs:
dW,i = D(4.05,Tc,i), (3)
dC,i = D(4.33,Tc,i) e
−τ +D(4.33,Tu) (1−e−τ
). (4)
It has seven parameters for the ten absolute SPARTA region
depths (window and CO2 band, five visits). We minimise
χ
2 with Nelder–Mead from a grid of starting points, profile
the likelihood over (Tu, τ) by re-optimising the five Tc,i at
each grid point, and compare with the null model of an
independent blackbody per epoch (five parameters), which
is nested in it at τ = 0.

3.3 Radiative-equilibrium temperature of a

thin layer
A thin layer with shortwave optical depth τSW and infrared
optical depth τIR above a photosphere of temperature Tc and
albedo A absorbs the direct and reflected stellar flux and
the upwelling thermal flux, and emits in two directions. Its
equilibrium temperature is
T
4
u =
1
2
[
γ (1+A) f T4
ss +T
4
c
]
, γ =
τSW
τIR
, (5)
where Tss = T⋆(R⋆/a)
1/2 = 2756 K is the zero-albedo substellar equilibrium temperature and f = 1 at the substellar

## Page 3

Table 1: The five JWST/NIRCam eclipses. White-light depths and brightness temperatures are the stark values of Patel et al. (2024);
cross-correlation significances are from Snellen et al. (2026).
Visit Start (UTC) Parity d2.1 (ppm) d4.5 white light (ppm) Tb(4.5) (K) CO x-corr S/N
V1 2022-11-18 14:40 even 47.4
+21
−16 7.0±8.8 873 ∼8 (emission)
V2 2022-11-20 19:43 odd −5.1
+5.5
−6.0
65.2
+22
−42 1716 ∼3
V3 2022-11-23 00:44 even 37.3±4.7 101.4
+17
−32 2078 none
V4 2022-11-24 11:38 even 36.8
+28
−33 119.2
+34
−19 2256 ∼3
V5 2023-04-24 11:57 odd 95.9±8 95.4
+14
−17 2016 none
point or 1/2 for the dayside-hemisphere average of the incident flux. This has no free parameter for a grey layer
(γ = 1) and is the number against which the fitted Tu is compared. The layer is in emission against the photosphere when
Tu > Tc.

3.4 Predicted line contrast

At the native resolution the CO lines of such a layer appear
in emission with a contrast proportional to D(4.7µm,Tu)−
D(4.7µm,Tc,i), the line-core minus continuum depth, for
fixed layer properties. Normalising to Visit 1 gives a predicted epoch-to-epoch pattern of cross-correlation signal-to-noise that can be compared with Snellen et al. (2026) without
further fitting. We evaluate it both with the SPARTA continuum temperatures from the joint fit and with the stark white-light brightness temperatures, which bracket the pipeline-dependent absolute level.

3.5 Supporting simulation

To check that the required photospheric swing is dynamically possible we re-implemented the delayed magma-temperature/cloud feedback of Loftus et al. (2025) as a delay-differential system in physical time, extended it to predict
the 2.1µm, 4.5µm and CHEOPS-band depths including reflected light, and scanned 640 parameter sets within their
Table 1 bounds (Appendix A). It is used only to show that
a condensate deck can move the 4.5µm photosphere by the
observed amount on the observed timescale; the results of
Section 4 do not depend on it.

4 Results

4.1 The CO2 band flips from emission to absorption within six days

The band-contrast index is positive in both faint epochs and
consistent with zero or negative in all three bright ones (Table 2, Fig. 1b). Combining the two pipelines, ∆C = +26±9
ppm in Visit 1 and +20±9 ppm in Visit 2, i.e. +23±6 ppm
(3.8σ) for the faint state, against +1±5 ppm for Visits 3–5
and −12±8 ppm in Visit 4 alone. The Visit 1 − Visit 4 difference is 38±12 ppm (3.2σ). Eureka and SPARTA, which
treat the correlated noise differently, agree epoch by epoch
(V1: +32±9 and +21±8; V4: −13±8 and −12±9), and
HANSOLO, whose Gaussian-process detrending absorbs
part of any slow signal, still gives +12±9 for Visit 1. Across
twelve combinations of band boundaries (window 3.90–4.15
to 3.95–4.19µm; band 4.18–4.50 to 4.22–4.46µm) and the
two error models the faint-state emission stays at 3.0–3.8σ
and the flip at 3.0–3.3σ (Appendix B). The CO band shows
no significant contrast in any epoch (|∆O| ≤ 1.9σ, mostly
within the blackbody slope), as expected for a band ten times
weaker than CO2 ν3.
This is the first direct, band-integrated evidence that the
thermal structure of the 4.5µm-emitting layer changes sign
between epochs. It is consistent with, and independent of, the
three single-epoch inferences already in the literature: Patel
et al.’s retrieval of Visit 1, which preferred an atmosphere at
∼2000 K above a surface at ∼1000 K; Snellen et al.’s CO
emission lines in the same epoch; and the CO2 absorption of
the Hu et al. spectrum, which is Visit 4.

4.2 One hot, optically thin layer fits all five

epochs
The joint two-layer model (Section 3.2) fits the ten absolute SPARTA region depths with χ
2 = 6.3 for 3 degrees of
freedom at Tu = 2580 K and τ = 0.31, with the continuum
photosphere at 1612, 1488, 2578, 2253 and 2327 K in Visits
1–5. The per-epoch blackbody null model gives χ
2 = 32.3;
the improvement of ∆χ
2 = 26.0 for two added parameters
is formally 5.1σ. The profile likelihood (Fig. 1d) allows
Tu from 2300 to 3600 K at ∆χ
2 < 4, with τ = 0.1–0.5: a
hotter layer needs a smaller optical depth to give the same
∼25 ppm of band emission, and the upper range includes
the 3500 K that Snellen et al. required for the CO line cores.
What is not allowed is a layer cooler than ∼2200 K, or an
optically thick one (τ ≥ 0.7, ∆χ
2 > 8), which would make
the band depth epoch-independent while the data still show
it rising with the continuum in the bright epochs (Fig. 1c).
The residual pattern is instructive. The model slightly
overpredicts the band in Visit 4 (+10 vs −8±9 ppm) and
underpredicts it in Visit 3 (+3 vs +13±9 ppm); these two
epochs are 1.5 days apart with the same continuum within
errors, so the difference is noise at the ∼ 2σ level rather than
a demand for a time-variable Tu. A layer whose temperature
lies between the two bright-state continua (2250–2580 K) is
neutral to weakly absorbing against hot magma and strongly
emitting against a 1500 K photosphere, which is the whole
observed behaviour.

## Page 4

Figure 1: (a) SPARTA absolute eclipse spectra of the five visits with the window, CO2 ν3 and CO 1–0 regions shaded. (b) Band-contrast
index ∆C per visit for Eureka (squares), SPARTA (circles) and their combination (diamonds); grey triangles: the CO band. Labels give the
stark white-light depth and the CO cross-correlation significance of Snellen et al. (2026). (c) CO2-band brightness temperature against
window brightness temperature; dotted line: single blackbody; solid: the joint two-layer fit (Tu = 2580 K, τ = 0.31); dashed and dash-dotted:
τ = 0.15 and 1.0 at the same Tu. (d) ∆χ
2 of the joint fit over (Tu, τ); contours at 1, 4 and 9; star: best fit.

4.3 The low-resolution fit predicts the high-resolution line strengths

With Tu and the per-epoch continua fixed by Section 4.2, the predicted narrow-line contrast D(4.7µm,Tu)−
D(4.7µm,Tc,i), scaled to Visit 1 = 8, is [8, 8.9, 0, 2.8, 2.2]
using the SPARTA continua and [8, 3.7, 1.0, 0, 1.5] using the
stark white-light temperatures (858, 1906, 2396, 2625, 2317
K on a blackbody-star scale); the observed cross-correlation
significances are [8, 3, 0, 3, 0]. The correlation coefficients
are 0.75 and 0.85. Two analyses of the same photons, at
R ≈ 30 and R ≈ 1600, are therefore described by one configuration: a layer at 2300–3600 K whose lines and bands
appear in emission exactly when, and in proportion to how
far, the continuum photosphere lies below it. The remaining discrepancy — Visit 2 predicted as strong as Visit 1 but
observed at 3σ against 8σ — is the one Snellen et al. themselves computed: a CO2/CO ratio of only 10−3
in the layer
cuts the CO cross-correlation signal-to-noise from ∼7 to ∼3
by blanketing the lines, while it broadens the band emission
that our index measures. The band contrast of Visit 2 being
at least as large as that of Visit 1 in SPARTA (+25 vs +21
ppm) is consistent with that reading, though not decisive in
Eureka (+15 vs +32).

4.4 The inverted colour of Visit 2

Visit 2 had no detectable 2.1µm occultation (−5.1
+5.5
−6.0
ppm,
Tb <∼ 1250 K at 1σ) while its 4.5µm white-light depth was
65+22
−42 ppm. No single-temperature surface or cloud top can
emit at 1400–1950 K in one band and below 1250 K in the
other, and the 2.1µm channel has no gas opacity to hide a
hot photosphere. The fitted layer resolves it without new
ingredients. A deck with a cold top (1000–1300 K) that is
dark at 2.1µm gives d2.1 = 1–5 ppm; the CO2 and CO bands
of the 2580 K layer, occupying roughly 30% of the 3.86–
4.98µm bandpass at τ ≈ 0.3, raise the white-light 4.5µm
depth to 22–35 ppm, within 1σ of the observed value. The
same deck made bright at 2.1µm (geometric albedo ∼1)
gives 2.5+26.7 ≈ 29 ppm, within 1.1σ of the 47+21
−16 ppm
of Visit 1. Visits 1 and 2, three orbits apart, thus differ in
the near-infrared reflectivity of the deck and in nothing else
that the data constrain; the 4.5µm band emission is present
in both. The 96 ± 8 ppm 2.1µm depth of Visit 5 exceeds
the 88 ppm that a Lambertian unit-albedo cloud over a 2756
K surface can produce and needs either a strongly back-

## Page 5

Table 2: Band-contrast indices (Section 3.1). Combined values carry the √
2 inflation for shared photons.
Visit ∆C Eureka (ppm) ∆C SPARTA (ppm) ∆C combined (ppm) ∆O SPARTA (ppm) State
V1 +32.0±8.6 +20.5±8.4 +26.1±8.5 (3.1σ) +2.3±8.0 faint, inverted
V2 +14.8±8.5 +24.5±8.4 +19.8±8.5 (2.3σ) +2.6±7.9 faint, inverted
V3 +5.4±8.6 +10.0±8.5 +7.7±8.5 (0.9σ) +9.2±7.9 bright, flat
V4 −12.6±7.8 −11.6±8.7 −12.2±8.2 (−1.5σ) −10.4±8.6 bright, absorbing
V5 +11.1±8.5 +7.8±8.5 +9.5±8.5 (1.1σ) −9.9±8.0 bright, flat
scattering fresh condensate (opposition surges give Ag > 1
on icy solar-system bodies) or residual systematics; we do
not use it.

5 Discussion

5.1 The inversion is the radiative skin, and it

never switches off
The fitted layer temperature is not a free quantity. Equation (5) gives, for a thin grey layer (γ = 1) averaged over the
dayside (f = 1/2), Tu = 2310 K above a bright 1500 K cloud
top (A = 0.8) and Tu = 2310 K above dark 2300 K magma
(A = 0): the reflected starlight the layer loses when the deck
clears is compensated by the hotter thermal flux rising from
the exposed magma. At the substellar point (f = 1) the same
layer sits at 2700 K. The joint fit’s 2300–3600 K is this number. No special absorber is needed to put a 2300–2700 K
layer above the photosphere of 55 Cnc e; a thin grey layer in
radiative equilibrium is there by default, and a layer enriched
in optical absorbers (γ > 1; TiO, PS, atomic metals, or the
condensate haze itself) is hotter still, which is where the

3500 K of the CO line cores belongs.

The variability is therefore not the appearance and disappearance of an inversion. It is the continuum photosphere
moving from 2250–2580 K, where it is hotter than the skin
and the bands are flat or weakly absorbing, to 1500 K and
below, where the skin stands out in emission by 25 ppm in
the CO2 band and by 8σ in the CO lines. Equation (5) also
explains why the emission is strongest when the planet is
faintest and the 2.1µm channel bright: the (1 + A) factor
makes the skin ∼17% hotter over a reflective deck than over
bare magma, so a bright deck both lowers the continuum and
raises the layer.

5.2 Only a condensate deck can move the photosphere that far, that fast

The 4.5µm continuum photosphere dropped by ≥ 1000 K between Visit 4-like and Visit 1-like states and recovered within
six days; between Visits 1 and 2 (three orbits) the deck’s near-infrared reflectivity changed while its temperature did not.
Gas cannot do this. Energy-limited escape at this old, quiet
star gives M˙ ≈ 2.5 × 106 kg s−1for LXUV ≈ 1028 erg s−1
and ε = 0.1, consistent with the ∼ 2.9×106 kg s−1ceiling
derived from CHEOPS (Meier Valdes et al. 2023); a 1 mbar ´
atmosphere (8×1010 kg) is removed in 104 days and a 10 bar
one in 106 years. A ≥ 10 bar CO2 troposphere, which the Hu
et al. spectrum requires once heat redistribution is computed
self-consistently (Zhan & Koll 2026), is permanent on the
timescales in question, and its large-scale dynamics produce
brightness-temperature variability an order of magnitude below what is observed (ibid.). A condensate deck, by contrast,
forms and sediments on hours-to-days timescales, has a cold
top set by radiative balance with the surface below (Loftus
et al. 2025, their Eq. 11; 1030–1220 K for surfaces at 1400–
1700 K and a cloud thickness parameter ∆T = 250–350 K),
and changes its near-infrared reflectivity with grain growth
on the same timescale.
Our delay-differential implementation of the magma-temperature/cloud feedback (Appendix A) shows the swing
is dynamically available: with a vapour-transport lag of 4.5
d, a cloud residence time of 0.6 d and a 30 m magma mixed
layer — all inside the published bounds — the 4.5µm depth
cycles between 18 and 105 ppm with a 12-day period, reproduces the Visit 1–4 sequence with pulls of 1.9, −1.1, −0.7
and −0.9σ at fixed amplitude, gives a CHEOPS-band mean
of 18 ppm (observed 12 ± 3), and with a lag of 17 d, the
global cloud-transport time, has a period of 47 d (CHEOPS:
47.3 d). The same model fails the 2.1µm channel in exactly
the way Section 4.4 anticipates: a single grey cloud couples
the two bands too tightly (model r = 0.96 against the observed 0.13), and the data require the deck’s reflectivity at
2.1µm to vary independently of its temperature.

5.3 External explanations are excluded by the

band sign
A stellar origin would need the star to brighten 17-fold to
turn a 119 ppm depth into 7 ppm (the occultation depth is
Fp/F⋆); the star varies by 0.6% (Fischer et al. 2008). Magnetic star–planet interaction can deliver at most ∼ 4×1015
W of Poynting flux to the planet for a few-gauss stellar dipole
at 0.015 au, against the ∼ 1021 W of dayside luminosity that
must be modulated. A 3:2 spin–orbit resonance predicts a
parity dependence that the JWST programme was designed
to test and did not find (Patel et al. 2024). A patchy circumstellar dust screen needs only ∼ 1012 kg to reach τ ≈ 3 over
the planet’s disc, so its mass budget is not the problem; but
a screen, like any change of viewing geometry, multiplies
the spectrum by a wavelength-dependent factor that varies
slowly across 0.3µm and cannot turn a molecular band from
absorption into emission. The band sign is the one observable that separates “less planet” from “a different planet”,
and it says the latter. Tidal magma-ocean waves (Farhat &
Chiang 2026) move heat across a hot surface and can produce aperiodic hotspot wandering; they do not lower the
photosphere to 1500 K or create band emission, though they
may well modulate the cycle.

## Page 6

5.4 A CO-rich skin above a CO2-rich troposphere

Snellen et al. require CO2/CO < 10−3at 1–10 mbar in Visit
1 and favour a hydrogen-rich composition; Zhan & Koll
require > 1% CO2 in a ≥ 10 bar troposphere from Visit

4. These need not conflict. The skin is the layer in which

the unshielded stellar UV photodissociates CO2 in minutes
(Heays et al. 2017, scaled to 0.015 au) while CO survives
by self-shielding; in a hydrogen-poor atmosphere the CO
+ O + M recombination is slow enough that the mbar layer
can be CO-dominated above a CO2-dominated interior, as
Snellen et al. note for the hydrogen-poor case. The epoch-to-epoch change in CO line strength at roughly constant band
emission (Section 4.3) then measures the CO2/CO ratio of
the skin, which is set by the balance of photolysis against
vertical mixing and can change within a day when a clearing
deck releases a convective pulse. This is a prediction rather
than a result: it requires the next high-resolution epochs to
show CO line strength anti-correlated with band breadth at
fixed continuum.

5.5 Caveats

The two pipelines reduce the same photons; the 3.8σ faint-state emission is one measurement whose robustness to reduction has been checked, not two independent detections.
The quoted per-bin uncertainties may be underestimated in
the presence of the hour-long correlated noise Patel et al.
describe; the empirical-scatter error model gives the same
significance, but thirty bins is a small sample. A wavelength-dependent instrumental effect that correlates with eclipse
depth could in principle mimic a band; it would have to peak
at the CO2 ν3 band in two epochs reduced by two pipelines
and vanish in three others, which we consider unlikely but
cannot exclude with five visits. The absolute continuum
temperatures differ between pipelines by up to 500 K even
though the band contrast does not, so the per-epoch Tc,i of
the joint fit carry that systematic. The radiative-equilibrium
argument treats the layer as thin and the deck as grey; a
deck with wavelength-dependent albedo changes the (1+A)
factor by tens of per cent, not the conclusion. Finally, five
epochs cannot establish periodicity; the cycle period and
duty cycle in Appendix A are illustrative, and the 47-day
CHEOPS modulation is matched by choosing the lag, not
predicted.

6 Predictions and tests

Each of the following can be falsified by a single scheduled JWST epoch (NIRCam eclipses; MIRI/MRS GO 7875;
NIRISS/SOSS transmission GO 12237; Zhan & Koll 2026
list the programmes).

1. Zero crossing. The CO2 band − window contrast is

positive whenever the window brightness temperature
is below 2300 K and zero or negative whenever it is
above 2600 K; the crossing lies at 2300–2600 K. An
epoch with a 1500 K continuum and a flat or absorbing
band falsifies the ever-present skin.

2. Bimodal 2.1µm in the faint state. When the 4.5µm

window is faint (TW < 1800 K) the 2.1µm depth is
either ∼0 ppm (dark deck) or 25–45 ppm (bright deck),
never intermediate, and the CO2 band is in emission in
both cases.

3. Line strength follows continuum darkness, not band

strength. The CO cross-correlation significance scales
with D(4.7,Tu)−D(4.7,Tc) and is undetectable when
TW > 2500 K; at fixed continuum, a broader CO2 band
emission goes with a weaker CO line signal.

4. Mid-infrared. In a faint epoch MIRI/MRS will show

the 15µm CO2 band in emission over a continuum at
1000–1500 K and a silicate emissivity feature of the
deck near 10µm; in a bright epoch the 15µm band is
in absorption against the ≥ 10 bar troposphere, as in
the Hu et al. LRS spectrum.

5. Transit. The deck sits at ≳ mbar, below one scale

height (∼50 km, ∼8 ppm), so the transit depth stays
constant to the ∼30 ppm precision of the record, but the
1–2.5µm transmission slope steepens in faint epochs if
the fresh deck is sub-micron.
The decisive programme is simultaneous optical (CHEOPS),
2.1µm, 4.5µm and R ≳ 1500 CO-line monitoring through
one cycle; ELT/METIS, which Snellen et al. show recovers
the CO signal at S/N > 20 per epoch, would make prediction
3 a routine measurement.

7 Conclusions

The public NIRCam eclipse spectra of 55 Cnc e contain a
diagnostic that the published analyses did not use: the sign
of the 4.3µm CO2 band relative to the adjacent continuum,
which is immune to the achromatic systematics of the data
and is the sign of the vertical temperature gradient. It flips
from +23±6 ppm (emission, 3.8σ) in the two faint epochs
to +1±5 ppm in the three bright ones within six days, in
two independent pipelines. All five epochs are fitted by one
gas layer at 2300–3600 K (best 2580 K) with CO2-band optical depth 0.1–0.5 over a continuum photosphere that alone
changes, from 1500 K to 2600 K; that layer predicts the
epoch-to-epoch CO line strengths of Snellen et al. (r = 0.85)
and the inverted colour of Visit 2. Its temperature is the
radiative-equilibrium temperature of a thin grey layer on
the dayside, 2300–2700 K, which is the same over a bright
cloud top as over bare magma. The thermal inversion of 55
Cnc e is therefore always present; what varies is whether the
continuum photosphere lies above or below it. A ≥ 10 bar
troposphere cannot move its photosphere by 1000 K in three
orbits and no external screen can change a band’s sign; a condensate deck forming and clearing on a magma-ocean/cloud
feedback cycle can do both, and reproduces the 4.5µm amplitude, the six-day recovery and, with a global-transport lag,
the 47-day optical period. The scheduled JWST epochs can
falsify this within a year through the five predictions above.

## Page 7

Data and code availability
The eclipse spectra are those of Patel et al. (2024) at
CDS, J/A+A/690/A159, table e2 (Eureka, SPARTA and
HANSOLO reductions), retrieved through the VizieR mirror at Harvard on 15 October 2026. The analysis script
(band flip analysis.py, NumPy/SciPy/Matplotlib, ∼2
minutes), its full numerical output, the delayed-feedback simulation (cnc e variability.py) and the retrieved spectra
accompany this preprint and will be deposited on Zenodo at
submission. White-light depths, brightness temperatures and
visit times are from Patel et al. (2024) Table 1; CO cross-correlation significances from Snellen et al. (2026) and their
Supplementary Figure 1; the magma-cloud model equations
and parameter bounds from Loftus et al. (2025) Methods and
Table 1.
Acknowledgements
This work is based on observations made with the
NASA/ESA/CSA James Webb Space Telescope, obtained
from the Mikulski Archive for Space Telescopes at STScI
(programmes GO 2084, PI A. Brandeker, and GO 1952, PI
R. Hu), and on the reductions made public by J. A. Patel
and collaborators, without which this analysis would not
have been possible. It used the VizieR catalogue access tool,
CDS, Strasbourg. The numerical analysis, figures and first
draft were produced with Claude (Anthropic) acting as an
AI research assistant under the author’s direction; the author
takes full responsibility for the content.

References

[1] Bourrier V., Dumusque X., Dorn C., et al. 2018, A&A, 619,
A1
[2] Demory B.-O., Gillon M., Madhusudhan N., Queloz D. 2016,
MNRAS, 455, 2018
[3] Demory B.-O., Sulis S., Meier Valdes E., et al. 2023, A&A, ´
669, A64
[4] Farhat M., Chiang E. 2026, ApJ, accepted, arXiv:2601.07080
[5] Fischer D. A., Marcy G. W., Butler R. P., et al. 2008, ApJ,
675, 790
[6] Heays A. N., Bosman A. D., van Dishoeck E. F. 2017, A&A,
602, A105
[7] Heng K. 2023, ApJL, 956, L20 (erratum 2024, ApJL, 971,
L52)
[8] Hu R., Bello-Arufe A., Zhang M., et al. 2024, Nature, 630,
609
[9] Loftus K., Luo Y., Fan B., Kite E. S. 2025, PNAS, 122,
e2423473122, arXiv:2409.16270
[10] Meier Valdes E. A., Morris B. M., Wells R. D., Schanche N., ´
Demory B.-O. 2022, A&A, 663, A95
[11] Meier Valdes E. A., Morris B. M., Demory B.-O., et al. 2023, ´
A&A, 677, A112
[12] Mercier S. J., Dang L., Gass A., Cowan N. B., Bell T. J. 2022,
AJ, 164, 204
[13] Patel J. A., Brandeker A., Kitzmann D., et al. 2024, A&A,
690, A159
[14] Snellen I., Miguel Y., Janssen L., Gonzalez Picos D., de Regt
S., Grasser N., Klijn L. 2026, Nature Astronomy, submitted,
arXiv:2606.11866
[15] Tamburo P., Mandell A., Deming D., Garhart E. 2018, AJ,
155, 221
[16] Zhan R., Koll D. D. B. 2026, ApJ, accepted,
arXiv:2606.12116
[17] Zilinskas M., van Buchem C. P. A., Zieba S., et al. 2025,
A&A, 697, A34
A Delayed magma-temperature/cloud
feedback in physical time
We integrate the two equations of Loftus et al. (2025) with
an explicit delay d rather than in lag-normalised time, so that
periods and timescales come out in days:
dτSW
dt
=
Π1 pref
d
exp(−
Tref
Ts(t −d)
)
−
Π2
d
τSW , (6)
dTs
dt
=
S0/(1+ατSW ) +εc σT
4
cd −σT
4
s
Π3 d
, (7)
with pref = 8.1 × 1013 Pa and Tref = 7.1 × 104 K for SiO
vapour over a bulk-silicate-Earth magma, α = 0.5, εc =
1−exp(−β τSW ), the cloud top and base temperatures from
T
4
s = T
4
cu+T
4
cd with Tcd −Tcu = ∆T, S0 = 3.27×106 W m−2
,
a solidus floor at 1400 K with a latent-heat budget equivalent
to 300 K, and Π1, Π2, Π3, β, ∆T inside the bounds of their
Table 1. The observables are computed from the state: the
4.5µm depth as the hemisphere-averaged emission of the
surface through the deck plus that of the cloud top (ε at
4.5µm = 0.6τSW ), the 2.1µm depth as the same thermal
term plus reflected light κgA(τ)(Rp/a)
2 with Lambertian
κg = 1 and (Rp/a)
2 = 26.7 ppm, a CHEOPS-band depth
from the shortwave albedo, and a CO line-minus-continuum
contrast from a shortwave-heated layer at T0(1+A)
1/4 with
T0 = 2300 K.
Of 640 parameter sets (d = 1.5–6 d, Π1 = 0.1–3 Pa−1,
Π2 = 1–8, Π3 = 300–104 kg s−3 K
−1
, ∆T = 250–350 K),
48 oscillate; the dynamics depend only on the Π’s and the
period scales linearly with d. The best cycle (d = 4.5 d,
Π1 = 3, Π2 = 8, Π3 = 300, ∆T = 350 K; cloud residence
0.6 d; mixed-layer heat capacity 1.2×108J m−2 K
−1
, i.e.
∼30 m of magma) has a 12.3-day period, a 4.5µm depth
of 18–105 ppm (brightness temperature 1130–2440 K), a
surface temperature of 1690–2760 K, a minimum cloud-top
temperature of 1220 K, a 2.1µm depth of 25–60 ppm and a
CHEOPS-band depth of 6–26 ppm (mean 18 ppm). Phase-aligned to the JWST week-1 sequence with no amplitude
scaling, the 4.5µm pulls are 1.9, −1.1, −0.7 and −0.9σ;
the 2.1µm pulls are −1.1, 6.0, 0.8 and 0.8σ, the 6σ being
Visit 2 (Section 4.4). The CO contrast is 110 ppm at the
cloud-on minimum and −11 ppm at the cloud-off maximum.

## Page 8

With d = 17.3 d and the same Π’s the CHEOPS-band period
is 47.2 d. Stochastic outgassing bursts (log-normal, σ = 1.5,
twice daily) jitter the period but do not destroy the cycle; it
is a stable limit cycle, as Loftus et al. found.
B Robustness of the band-contrast index
Table 3 lists the faint-state (V1+V2) CO2-band emission
and the V1 − V4 flip for twelve combinations of window
and band boundaries, with errors taken as the larger of the
quoted-uncertainty and empirical-scatter estimates and the
√
2 inflation for shared photons. The result does not depend
on which bins are called band or window, nor on the error
model.

## Page 9

Figure 2: (a) Surface temperature, cloud-top temperature and shortwave cloud optical depth over two cycles of the best parameter set. (b)
Predicted 4.5µm, 2.1µm and CHEOPS-band depths with the JWST week-1 points phase-aligned. (c) Model CO line contrast against
4.5µm continuum depth, with the observed cross-correlation significances. (d) The 2.1µm–4.5µm plane: the model trajectory couples the
bands (r = 0.96) more tightly than observed (r = 0.13), because of Visits 2 and 5. (e) The same physics with a 17-day lag reproduces the
47-day CHEOPS period. (f) Robustness to stochastic outgassing bursts.
Table 3: Robustness of the band-contrast result to band definitions.
Window CO2 band Faint ∆C V4 ∆C V1−V4
(µm) (µm) (ppm) (ppm) (ppm)
3.90–4.195 4.20–4.46 +23.8±7.4 (3.2σ) −12.2±8.2 +38.3±12.3 (3.1σ)
3.90–4.195 4.20–4.40 +22.7±7.3 (3.1σ) −10.8±8.8 +40.2±13.0 (3.1σ)
3.90–4.195 4.22–4.46 +25.5±7.3 (3.5σ) −12.3±8.4 +39.5±12.4 (3.2σ)
3.90–4.195 4.18–4.50 +22.3±6.7 (3.3σ) −10.7±7.8 +37.3±11.7 (3.2σ)
3.90–4.15 4.20–4.46 +27.4±7.8 (3.5σ) −12.0±8.6 +41.9±13.2 (3.2σ)
3.90–4.15 4.20–4.40 +26.0±7.6 (3.4σ) −10.6±9.2 +43.9±13.7 (3.2σ)
3.90–4.15 4.22–4.46 +29.0±7.7 (3.8σ) −12.0±8.8 +43.1±13.2 (3.3σ)
3.90–4.15 4.18–4.50 +25.7±7.0 (3.6σ) −10.6±8.3 +41.0±12.5 (3.3σ)
3.95–4.19 4.20–4.46 +22.2±7.3 (3.0σ) −12.8±8.4 +36.9±12.4 (3.0σ)
3.95–4.19 4.20–4.40 +21.1±7.2 (2.9σ) −11.4±8.9 +38.7±13.0 (3.0σ)
3.95–4.19 4.22–4.46 +23.8±7.3 (3.3σ) −12.9±8.6 +38.0±12.4 (3.1σ)
3.95–4.19 4.18–4.50 +20.7±6.6 (3.1σ) −11.1±8.0 +35.8±11.7 (3.1σ)
