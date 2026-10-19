## Page 1

No confirmed extragalactic planets:
a reassessment of every published candidate
[Author name(s) and affiliation(s)]*
October 17, 2026

Abstract

Eleven claims of planets, or planet-mass populations, beyond the Milky Way have appeared since 1996, together
with three claims of planets around Milky Way stars of extragalactic origin. None has been confirmed, and none
can be repeated: each rests on a single unrepeatable event or on a statistical inference whose null hypothesis
was never computed. We reassess all of them with a common method: reconstruct the published measurement,
replace the authors' favourable assumption with the full prior, condition the inference on the fact that the
event was found, and compute the null model. For M51-ULS-1b the X-ray dip does not measure the occulter's
radius (a grazing star fits within ∆ lnL = 0.7 of a central Saturn), the achromaticity test carries a Bayes factor
of only ∼ 2–8, and once detection is conditioned on, the most probable occulter is an M-dwarf tertiary; the
event rate also exceeds that expected from bound companions by 102–103. For PA-99-N2 the “6 MJ planet”
requires a 0.5 M⊙ lens in the M31 disc, which implies a source size ρ ≃ 0.10–0.20 Einstein radii, whereas the
sharpness of the fitted anomaly requires ρ < 0.021; forcing ρ = 0.10 in a finite-source binary-lens refit degrades
χ
2 by 65–154 (2% errors), and a rate-weighted lens-population analysis gives a 2–5% probability of a planet in
M31. The Fe Kα line-shift statistics behind the “≳ 2000 planets per star” claims in three lensed quasars are
reproduced by a static spectrum containing the broad relativistic line that RX J1131−1231 is known to possess,
fitted with narrow Gaussians in low-count spectra. The FRB 20180916B planet fails a beaming-independent
energy budget by 103.7–107; the published BD+20 2457 two-companion system disintegrates in 4–2500 yr; the
NGC 4845 tidal-disruption “super-Jupiter” is one corner of a victim-mass degeneracy spanning 2 MJ to 3 M⊙;
the Twin-Quasar and Einstein-Cross “planets” follow from misreadings of event timescales. We identify four
recurring failure modes and state the measurements a future confirmation would need.

1 Introduction

Planets are common in the Milky Way, and nothing
distinguishes the stars of other galaxies in a way that
should prevent them from hosting planets. Finding
one, however, is a different matter. At megaparsec
distances individual stars cannot be resolved, radial
velocities and transits are out of reach, and every proposed detection method relies on a single, unrepeatable event: a microlensing anomaly, an X-ray eclipse,
a brightness fluctuation in a lensed quasar, a flare from
a disrupted body.
The literature now contains eleven such claims beyond the Milky Way, catalogued in the usual reference lists (e.g. Wikipedia, 2026): M51-ULS-1b,
an X-ray transit candidate in the Whirlpool galaxy
(Di Stefano et al., 2021); PA-99-N2, a binary-lens
microlensing event towards M31 interpreted as a
star–planet pair (An et al., 2004; Ingrosso et al.,
2009, 2011); free-floating planet populations in the
lens galaxies of RX J1131−1231, Q J0158−4325 and
SDSS J1004+4112 inferred from Fe Kα line shifts (Dai
& Guerras, 2018; Bhatiani et al., 2019); a “3 Earth-mass” body in the Twin Quasar lens (Schild, 1996;
Colley & Schild, 2003); a 1.6 Jupiter-mass reading
of the 1989 Einstein-Cross event (Irwin et al., 1989)
and a 2024 “nanolens” population in the same system
(Tuntsov, 2024); a 2.9 M⊕ planet orbiting the magnetar responsible for FRB 20180916B (Kurban et al.,
2022); and a 14–40 MJ object destroyed in the tidal disruption event in NGC 4845 (Nikołajuk & Walter, 2013;
Lei et al., 2016). Three further claims concern planets around Milky Way stars thought to have formed in
accreted dwarf galaxies: HIP 13044 b (Setiawan et al.,
2010), BD+20 2457 b and c (Niedzielski et al., 2009;
Perottoni et al., 2021) and a planet-engulfment inference for HD 134440 (Reggiani & Meléndez, 2018).
None of these is listed as confirmed in the NASA
Exoplanet Archive, and the discovery papers themselves use the word “candidate”. Yet they are routinely described in secondary literature as “the first
planets in other galaxies”. In this paper we ask a narrower question of each: given the data that exist, does
the planetary interpretation survive a complete analysis? We find that it does not, in any case. Several
claims are internally inconsistent with the data that
produced them; others rest on a null hypothesis that
was never computed; others follow from a favourable
choice among unconstrained nuisance parameters; and
two had already been withdrawn.
Section 2 describes the common method. Sections 3–
9 treat the candidates in turn, in decreasing order of
the effort each required. Section 10 draws out the common failure modes and specifies what a confirmation
would need. Section 11 tabulates the outcome.

## Page 2

2 Method

2.1 Single-event inference

Every candidate is a single event. For such data the
posterior on the physical parameter of interest, θ (a
radius, a mass, a location), is
p(θ | d, found) ∝ L(d | θ) Pdet(θ) π(θ), (1)
where L is the likelihood of the light curve or spectrum,
π is the astrophysical prior over the populations that
could have produced the event, and Pdet is the probability that an event with parameters θ would have
been found by the search that found it. The discovery papers examined here evaluate L, sometimes with
care, but replace Pdet π(θ) by a choice: a uniform prior
over a convenient range, or a single assumed value for
the parameter that sets the scale (the lens mass, the
black-hole mass, the number of debris clumps). When
L is nearly flat in θ, which is the generic situation for
a single event, that choice is the result. Our first step
in each case is therefore to map L over the full range
of θ and to restore Pdet and π.

2.2 Null models

Several claims are statistical: an excess frequency of
some feature is attributed to planets because a model
without planets predicts fewer. The decisive question
is then what the model without the claimed effect predicts once all known ingredients are included, calibrated with the look-elsewhere effect appropriate to
the search. We compute these nulls by simulation.

2.3 Reconstruction from published parameters

The raw data of several candidates (Chandra event
files, POINT-AGAPE photometry) could not be retrieved from the environment in which this analysis
was carried out. Where that is so we reconstruct the
measurement from the published model definition and
fitted parameters, using “Asimov” data sets (expected
values, no noise) and verifying that our likelihood reproduces the published posterior before any new analysis is layered on top. Conclusions drawn this way
concern the information content of the published fit,
which is what the published claims rest on.

2.4 Independent verification

The load-bearing computations—the M51-ULS-1b radius degeneracy, the PA-99-N2 finite-source refit, the
Fe Kα line-shift simulation, the FRB energy budget
and the BD+20 2457 integrations—were re-derived
from scratch by an independent implementation that
had access to the specification of each calculation but
not to our code. Where the first pass of our own analysis contained an error (an unequal treatment of blending in the PA-99-N2 refit, §4.2), the verification caught
it and the corrected numbers are the ones reported.

3 M51-ULS-1b

3.1 The claim

Di Stefano et al. (2021) searched 2624 Chandra light
curves of 238 bright X-ray sources in M51, M101 and
M104 for intervals in which the count rate fell to zero
and recovered, and found one: a ≃ 3 h symmetric dip
in the ultraluminous supersoft source M51-ULS-1 during ObsID 13814 (2012 September 20), with 20–30 min
at zero flux. Fitting an opaque disc crossing a uniform
X-ray photosphere of radius RX = 2.5
+4.1
−1.1 × 109
cm
(Urquhart & Soria, 2016), they obtained an occulter
radius with mode 0.74 RJ (90% interval 0.18–2.7 RJ), a
transverse speed of 17 km s−1(5–56 km s−1) and hence
a circumbinary orbit of tens of AU, and argued from
the constancy of the X-ray hardness ratio across the
dip that it is an eclipse rather than absorption or a
state change. Stellar companions were excluded on
the grounds that the system is younger than 20 Myr
and a star of that age is larger than the fitted radius.

3.2 The light curve does not measure

the radius
We reimplemented the published model (five parameters: baseline counts cX, mid-time, impact parameter
b, radius ratio f = R/RX, speed v; 471.156 s bins;
Poisson likelihood; background 0.38 counts per bin)
and fitted an Asimov light curve constructed from the
published values (cX = 7.6, 10.5 ks first-to-last contact,
1.56 ks at zero). Restricted to f < 3 the posterior reproduces Table 1 of Di Stefano et al. (2021): radius
mode 0.73 RJ, speed mode 18 km s−1.
Profiling the likelihood over f with the other parameters free reveals why that restriction matters (Fig. 1).
An opaque body of any radius R ≥ RX whose limb
passes through the source, b ≃ R − RX, fits the dip to
within ∆ lnL = −0.13 (f = 2), −0.48 (f = 5), −0.61
(f = 10) and −0.70 (f = 30, i.e. R ≃ 1.3 R⊙). The
grazing geometry trades a faster limb crossing for a
larger body and reproduces the ingress, the flat bottom and the egress. A likelihood ratio of 2 is no discrimination at all. The published “Saturn-sized” mode
arises because the prior on b is uniform out to 51RX
while the ridge of acceptable large-f solutions is only
∼ 0.1RX wide in b; with a prior proportional to the
transiting range of b, which is the physically correct
one, the ridge is not penalised and the 90% interval
on R becomes 0.14–14 RJ. A generic trapezoid or a
flat-bottomed Gaussian fits as well as the occultation
geometry (∆ lnL = 0.04), so the dip shape carries no
evidence for a transit as opposed to any other symmetric interruption.

3.3 The achromaticity test is weak

The argument that a constant hardness ratio excludes
absorption and photospheric changes was qualitative.
We folded a blackbody of kT = 70–130 eV through

## Page 3

Figure 1: Expected counts for the published M51-ULS-1b
solution (a body of 1.35RX crossing the source centrally)
and for grazing occulters of 5RX ≃ 1.5 RJ and 30RX ≃

1.3 R⊙, with the other parameters re-optimised. The three

curves differ by ∆ lnL ≤ 0.7 for the observed data quality.
Figure 2: Soft and hard light curves expected for the same
broadband dip under the three hypotheses, kT = 100 eV.
The curves differ by a few counts.
an approximate 2012 ACIS-S response (with Morrison–
McCammon absorption) and constructed, for the same
broadband dip, the soft (0.3–0.7 keV) and hard (0.7–
7 keV) light curves expected from (A) an opaque occulter, (B) an absorbing cloud whose column reproduces
the broadband depth at each instant, and (C) an expanding, cooling photosphere at constant bolometric
luminosity, the mechanism of the X-ray off-states this
class of source is known to display (Greiner & Di Stefano, 2002). With ∼ 70 source photons in the partial
phases and a hard fraction of 0.27 at kT = 100 eV, the
expected log Bayes factor for A over B is 1.3 and for
A over C is 2.1 (Fig. 2); across the temperature range
it spans 0.3–4.2. The constancy of the hardness ratio
favours an opaque body by odds of roughly 2:1 to 8:1.

3.4 Detection-conditioned inference

A transit found in a search must be weighted by the
probability of being found: the alignment probability
∝ (RX + R)/(δ a), where δ ≃ 0.15 rad is the inclination spread allowed by the donor eclipses the system
shows, and the timing probability Tobs/Porb ∝ a
−3/2
.
We re-weighted the light-curve posterior by these fac-Figure 3: Occulter radius and orbital separation for M51-
ULS-1b under the published prior (grey; black outline
when the grazing ridge is sampled) and under the detection-conditioned class mixture (stacked).
tors and by physical priors over four classes of occulter
at the system's age of 5–20 Myr: sub-Saturns (0.35–

1.2 RJ), giant planets (1.1–1.8 RJ), brown dwarfs (1.5–

5.4 RJ) and M dwarfs (3.5–15 RJ), with orbits between

the circumbinary stability limit 2.4 abin (Holman &
Wiegert, 1999) and 300–1000 AU, Mtot between 10
and 40 M⊙ and eccentricities up to 0.5. The detection-conditioned posterior moves every class inward and
the mixture towards larger bodies: a giant planet at
6
+6
−2 AU (P ≃ 4 yr), a brown dwarf at 2.6 AU, an M
dwarf at 1.7 AU (Fig. 3). With occurrence priors of 0.2,
0.1, 0.05 and 0.15 per massive binary, the class probabilities given an occultation are 1%, 7%, 13% and 79%;
tripling the planet priors raises the planetary share to
21%.

3.5 Occultation or intrinsic variability:

the base rate
Summed over the four classes, bound-body occultations of a bright X-ray binary are expected at 2.4 ×
10−5 per source-megasecond. The search found one
in 20–200 source-Ms (the exposure actually sensitive
to a 1 ks drop to zero), a factor 102–103 above expectation. Di Stefano et al. (2021) resolve this by inferring “64/g” wide-orbit companions per X-ray binary
with g ≃ 1, i.e. every companion's orbit aligned with
the line of sight to ∼ 10−5rad; the donor eclipses
constrain the inclination only to ∼ 0.1 rad, and circumbinary mutual inclinations are ≳ 0.01 rad. The
alternative is that the dip is not an occultation. This
source shows off-states, energy-dependent double dips
and stellar eclipses in the same archive; if intrinsic or
absorption events that mimic a 3 h achromatic dip occur at even 10−3 per source-Ms, the probability that
this dip is an occultation is ≃ 10% at the central Bayes
factor (Fig. 4). We also checked all on-state windows
of the 2000–2018 archive for a repeat at T0 +nP: only
2% of the short-period posterior is excluded, so the
archive is uninformative.

3.6 Verdict

M51-ULS-1b is a 3 h achromatic dip in a variable supersoft source, consistent with an opaque body of any

## Page 4

Figure 4: Probability that the M51-ULS-1 dip is an occultation by a body, as a function of the rate of look-alike intrinsic or absorption events, for three values of the
shape/hardness Bayes factor. The vertical line is the predicted bound-body occultation rate; the shaded band is
the empirical rate of such dips in the search.
radius ≳ 0.3 RJ. Given an occultation, a planet is the
least probable class; whether it is an occultation at
all depends on a base rate the data do not constrain.
More Chandra time on this source cannot settle it:
with P ≃ 0.5–10 yr the chance of a repeat per Ms
is 0.003–0.1, and a repeat at this count rate leaves the
size degeneracy intact. Separating a central 1.35RX
body from a grazing star at ∆ lnL ≃ 5 requires about
seven times the photons in the partial phases.

4 PA-99-N2

4.1 The claim

PA-99-N2 is a bright 1999 pixel-lensing event 22′from
the centre of M31 (Paulin-Henriksson et al., 2003). An
et al. (2004) showed that its light curve departs from
a point-lens model near peak and is fitted by a binary
lens with tE = 125–132 d, mass ratio q = 10−1.85 (close
solution C1), 10−1.91 (wide, W1) or 10−2.12 (finite-source solution FS), and found marginal finite-source
effects, ρ = (1.31 ± 0.30) × 10−2 with ∆χ
2 = 4.9 relative to a point source and ρ < 2.06 × 10−2
. The
source is an M giant in the M31 disc with angular
radius θ∗ = 0.51 ± 0.06 µas. An et al. (2004) concluded that the lens is most probably in the M31 halo
and “most probably a stellar remnant”. Ingrosso et al.
(2009, 2011) instead adopted a 0.5 M⊙ lens in the M31
disc, the most probable mass for disc self-lensing, and
announced a 6.34 MJ companion.

4.2 The finite-source constraint excludes the assumed lens

Microlensing fixes θ
2
E = κMπrel with κ =
8.144 mas M−1
⊙ . For a lens inside M31 the relative parallax is tiny, so a 0.5 M⊙ star 1–4 kpc in
front of the source has θE = 2.6–5.2 µas and the
source subtends ρ = θ∗/θE = 0.10–0.20 Einstein radii,
five to ten times the published upper limit (Fig. 5,
left). Equivalently, the limit θE ≳ 25 µas requires
M ≳ 114 M⊙ (1 kpc/DLS) for an M31 lens and, with
tE = 127 d, a lens–source relative speed ≳ 260 km s−1
(Fig. 5, right); disc stars move at ∼ 60 km s−1relative
to one another.
Because the finite-source fit of An et al. (2004) was
a restricted search around C1 and was flagged as possibly affected by systematics, we tested the constraint
directly. We computed finite-source binary-lens magni-
fication maps for the C1 geometry by inverse ray shooting (81 million rays, 0.0015θE pixels; companion on the
side that reproduces the published anomaly, ∼ 14%
peak-to-peak 3.6 d before t0), generated the ρ = 0.013
light curve with POINT-AGAPE-like sampling (167
epochs, a gap at JD′ 72–91) and 2% errors, and refit-ted it with models forced to larger ρ, letting t0, u0, tE,
α and the fluxes float in a global search, with the baseline pinned to within −10%/+50% of the source flux
as the flat 2000–2001 seasons pin it. Across four epoch
realisations the best attainable χ
2
is 52–93 at ρ = 0.05,
65–154 at ρ = 0.10 and 109–201 at ρ = 0.20, against 0
for the published solution and 134–161 for a single lens
(Fig. 6). A disc-star source size does not smooth the
fitted anomaly; it produces a different, 25-day-wide
feature. Scaled to the real photometric precision these
penalties are several hundred in χ
2
. An independent
implementation confirmed the light curves and the re-
fits; it also exposed an error in our first pass, which had
compared a flux-constrained binary against a flux-free
single lens, and showed that with unconstrained negative blending both models find unphysical shortcuts.
The numbers above are the corrected ones.

4.3 Rate-weighted lens-population inference

We built a Bayesian model with five lens populations—
M31 disc, spheroid and halo, Milky Way halo and
Milky Way disc—normalised by the optical depths of
An et al. (2004) (halo MACHO fractions 1–20%) and
a local-density model for the Galactic disc; a present-day mass function including white dwarfs, neutron
stars and black holes (Kroupa IMF, initial–final mass
relations); line-of-sight density profiles; realistic kinematics (disc dispersion plus shear, spheroid and halo
dispersions, the source's transverse rotation, solar motion); a luminosity veto on foreground main-sequence
lenses brighter than V = 22; and the measured tE and
θ∗. Each population was sampled τ -weighted and converted to event-rate weights, Γ = (2/π)τ ⟨1/tE⟩. The
finite-source information was applied three ways: ignored, as an upper limit only, and as published (Table 1, Fig. 7).
Ignoring the finite-source information reproduces
the published picture: a 0.6 M⊙ M31 disc star with
a ∼ 9 MJ companion. That picture predicts ρ ≃ 0.1,
which the light curve excludes. With the published
constraint, the lens is in M31 with probability 0.8–0.95
but is a 5–50 M⊙ remnant in the halo or spheroid moving at ∼ 400 km s−1
, with a ∼ 0.1 M⊙ companion; the

## Page 5

Figure 5: Left: Einstein radius against lens–source distance for lenses inside M31; the band is the θE implied by
the sharpness of the anomaly. Right: Einstein time against relative transverse speed; disc kinematics cannot produce
tE = 127 d with θE ≥ 25 µas.
Figure 6: Finite-source light curves for the PA-99-N2 solution C1 at the published ρ and at the values implied by
a 0.5 M⊙ disc lens, and residuals from each curve's best
single-lens fit.
Table 1: PA-99-N2: probabilities under three treatments
of the finite-source constraint. Ranges span halo MACHO
fractions 0.01–0.2 with an agnostic (log-uniform) MACHO
mass prior.
ρ treatment P(lens in M31) P(Mc < 13 MJ) P(planet in M31)
ignored 0.96 0.66–0.77 0.62–0.73
upper limit only 0.31–0.70 0.31–0.74 0.002–0.012
as published 0.79–0.95 0.12–0.31 0.02–0.05
probability of a planet in M31 is 2–5%. With only the
upper limit, the most probable planetary solution is a
foreground Galactic M dwarf at ∼ 2 kpc with a ∼ 4 MJ
companion—a planet, but a Milky Way one. The single scenario that restores a planet in M31 assumes a
population of 0.5 M⊙ MACHOs; the data then favour
a 4–7 MJ companion to a dark object 100–200 kpc from
either galaxy, with comparable odds for the two haloes,
at a MACHO fraction excluded in the Milky Way by
EROS and OGLE (Tisserand et al., 2007; Mróz et al.,
2024).

4.4 Verdict

The binary-lens anomaly is probably real (it improves
on a single lens by ∆χ
2 = 512 and is seen in independent MEGA photometry), though χ
2/dof = 0.66, a
4%-per-arcsecond seeing systematic and parallax alternatives within ∆χ
2 ≃ 25–30 counsel caution. Its mass
ratio is well determined. Its planetary reading requires
a lens that the same light curve excludes. The lens is
most probably a stellar-mass black hole in the M31
halo or spheroid with a low-mass stellar companion.

5 Quasar-microlensing “planet

populations”

5.1 The claim

Dai & Guerras (2018) examined 38 Chandra observations of the quadruply lensed quasar RX J1131−1231
(zs = 0.658, zl = 0.295), in which Chartas et al.
(2017) had fitted narrow Gaussian lines to each image's spectrum and found Fe Kα energies shifted from
6.4 keV, with g = E/6.4 spanning 0.5–1.3. Shifts sig-nificant at 3σ occur in 26%, 34%, 21% and 11% of
epochs for images A–D. Assuming that each shifted
line marks a caustic crossing the Fe Kα region (≲

## Page 6

Figure 7: Companion-mass posterior for PA-99-N2, stacked by lens population, for the three treatments of the finite-source constraint (MACHO mass log-uniform, halo fraction 5%).
10 rg ≃ 1.9 × 1014 cm), they computed the probability that a caustic crosses a source of that size at
a random time from magnification maps with stars
only (κ∗/κ ≃ 0.1) and with an added population of
free-floating bodies, and found that stars alone are excluded at 4.5–6.4σ while a planet surface-mass fraction αpl ≳ 10−4 of the total is required, which they
expressed as ≳ 2000 objects from Moon to Jupiter
mass per main-sequence star. Bhatiani et al. (2019)
applied the same method to Q J0158−4325 (10 lines
in 12 spectra) and SDSS J1004+4112 (8 in 40).

5.2 The null model

The logic treats every shifted narrow line as an event.
But RX J1131−1231 possesses a strong broad relativistic Fe Kα line in its stacked spectrum; it is the object in which Reis et al. (2014) measured a black-hole
spin from that line, and its g range for a disc seen at
i ≃ 70–76◦is precisely 0.5–1.3. The individual spectra
have 150–7400 counts (B–D) and up to a few thousand
for most epochs of A. A narrow Gaussian of free energy fitted to such a spectrum will lock on to noise
peaks within the broad hump, and its energy uncertainty from a ∆C = 1 interval will be a few tens of
eV.
We simulated static spectra (power law Γ = 1.7;
a narrow 6.4 keV core of rest-frame equivalent width
150 eV, the value Chartas et al. (2017) find in the
stacked image-C spectrum; a broad line from a Keplerian disc at i = 70◦ with emissivity r
−3 or r−6 and
rest EW of 300–600 eV), folded through an ACIS-like
response, and fitted each as in Chartas et al. (2017):
C-statistic, power-law null, power law plus unresolved
Gaussian of free energy over rest 3.5–9 keV. The 90%
and 99% detection thresholds were calibrated on line-free simulations, which includes the look-elsewhere effect. A detected line was called “shifted” if |g − 1|
exceeded 3 (or 1) times its ∆C = 1 uncertainty.
The results (Fig. 8) at 1000–3000 counts per spectrum are: lines detected at > 90% in 28–64% of spectra
(observed 51%), at > 99% in 6–27% (observed 14%),
3σ-shifted narrow lines in 15% (core plus broad) to 19–
31% (broad only), against the observed 21–34%, with
shifted energies spanning g = 0.55–1.3 (observed 0.5–
1.3) and the large fitted equivalent widths that Chartas et al. (2017) report. An independent implementation with a Gaussian broad line found 13–17% (core
plus broad) and 17–30% (broad only) at 1000 and 3000
counts, and its line-free control gave 3σ-“shifted” lines
in 8–9% of spectra, as it must: a 90% threshold admits
10% false lines, and essentially all of them are shifted.
No single static model reproduces all three observed
fractions simultaneously; the actual spread of counts
across 152 spectra, and the stellar microlensing that
is undisputedly present (κ∗/κ ≃ 0.1; this quasar's X-ray flux ratios vary by factors of several), bracket the
observations without difficulty.

5.3 Verdict

The statistic from which the planet population was inferred has a null expectation of 15–30%, not the few
per cent implied by counting stellar caustic crossings
alone. Nothing remains for planets to explain. Two
further points stand independently of the simulation.
First, the quoted mass range is not what the data
probe: a Moon-mass lens has a source-plane Einstein
radius of 9×1012 cm against a ≳ 2×1014 cm emitting
region and perturbs its magnification by ∼ 10−3; only
bodies above a few Earth masses can shift the line,
and the “2000 per star” number is dominated by the
extrapolated low-mass end of an assumed N ∝ M−2
distribution. Second, the implied free-floating mass
per star (≳ 1 MJ) exceeds the Galactic microlensing
measurements by a factor of several (Mróz et al., 2017;
Sumi et al., 2023). The 2019 systems inherit all of this
with far fewer spectra.

## Page 7

Figure 8: Left: fraction of simulated static spectra in which a narrow-Gaussian fit detects a line at > 90% (solid) and
> 99% (dashed) confidence, against counts per spectrum, for four line models. Right: fraction with a > 3σ-shifted line.
The observed fractions for RX J1131−1231 are marked.

6 Single-event quasar microlensing

6.1 Q0957+561

Schild (1996) interpreted rapid (∼day) fluctuations of
∼ 1% in the time-delay-corrected difference of the
two Twin Quasar images as microlensing by planetary-mass bodies in the lens galaxy, popularly reported as
a 3 Earth-mass planet; Colley & Schild (2003) later reported a 0.93%, 12-hour event. A point lens whose Einstein radius is much smaller than the source changes
the source's magnification by at most ≃ 2(RE/Rs)
2
.
For Q0957+561 (zl = 0.355, zs = 1.41) the source-plane Einstein radius of 3 M⊕ is 1.8 × 1014 cm; the
R-band disc is 5 × 1015–1016 cm (Refsdal et al., 2000;
Hainline et al., 2012). The maximum perturbation
is 0.07–0.26% and the event lasts 2Rs/v ≃ 3–6 yr at
v = 1000 km s−1(Fig. 9). A 1% event in half a day
requires ∼ 10−7 M⊙ lenses crossing ∼ 1013 cm brightness structures in the disc, which is the ad hoc “double-ring” quasar of Colley & Schild (2003). The 2003 event
itself rests on 12 overlapping points from two epochs
14 months apart, and the authors' leave-one-night-out
significances are 41–74%.

6.2 Q2237+0305

The 1989 brightening of image A of the Einstein Cross
(Irwin et al., 1989) was the first detection of quasar
microlensing and is universally interpreted as a stellar
caustic crossing in the lens bulge (κ∗ ≃ 0.4–0.8). The
“1.6 Jupiter-mass” reading that has entered reference
lists appears in no paper: it is RE = v t with t = 420 d
and v ≃ 2000 km s−1. The effective source-plane velocity for this system is (Ds/Dl) ≃ 11 times the lens-plane
velocity, i.e. 3000–6500 km s−1(Kochanek, 2004; Mosquera & Kochanek, 2011), which in the same reading
gives 10–30 MJ; and the reading is wrong in kind, be-Figure 9: Maximum fractional brightening of the
Q0957+561 optical disc by a single point lens, against lens
mass, for three source radii.
cause the duration of a caustic crossing measures the
source size (Rs ≃ vt ≃ 1–5 × 1015 cm, which is the
measured disc size), not the lens mass. Tuntsov (2024)
tests a population of 10−4 M⊙ “nanolenses” making up
6–11% of the lens convergence against time-derivative
statistics of filtered OGLE light curves, describes the
outcome as “not much more than suggestive”, gives no
significance, and notes that a 1016 cm source removes
the signal. Such a population, if compact, is excluded
by Galactic constraints on free-floating bodies by two
orders of magnitude.

7 FRB 20180916B

Kurban et al. (2022) proposed that the 16.35-day periodicity of FRB 20180916B arises from a 10−5 M⊙
(3.3 M⊕) rocky planet on an e = 0.88–0.92 orbit about
a neutron star, partially disrupted at each periastron
(rp = 2rtd ≃ 1.6–2.4 × 1011 cm); km-sized debris
clumps then interact with the pulsar wind through
Alfvén wings (Mottez & Zarka, 2014), and their orbital-

## Page 8

Figure 10: Spin-down luminosity required by the
FRB 20180916B planet model, against the number of
emitting clumps, compared with spin-down lifetimes, the
persistent-source limit and known pulsars.
period spread sets a ∼ 5-day active window. The
model's flux formula multiplies a 4π/Ω beaming factor
(Ω = 0.1 sr) by an additional (γ/105)
2 with γ = 3×106
.
Beaming cannot help a time-averaged budget. The
observed burst rate times the observed isotropic energy equals the true power emitted by all clumps, because each clump's beaming factor cancels between the
two. CHIME measures a peak rate of 0.86+0.5
−0.35 h
−1
above 5.2 Jy ms with a fluence index of −2.3 (Sand
et al., 2023); with a 400 MHz band at 150 Mpc the
mean burst energy is 2.4 × 1038 erg and ⟨Liso⟩ =
5.8 × 1034 erg s−1 at phase peak. With the model's
radio efficiency ϵr ≤ 10−2the clumps must tap ≥
5.8 × 1036 erg s−1. The Alfvén-wing power of a clump
of radius Rc at distance r is 1.5(Rc/r)
2 = 2.6 × 10−11
of the spin-down luminosity for 10 km clumps at periastron, so
Lsd ≥
2.2 × 1047
Nc
erg s−1, (2)
where Nc is the number of simultaneously emitting
clumps; the model produces “a few major fragments”.
A neutron star at break-up spin holds ≲ 1053 erg, so
this engine lasts 5 days (Nc = 1) to 14 yr (Nc = 103),
against a period that has remained 16.34±0.07 d with
a constant Poisson rate since 2018 (Sand et al., 2023);
and any such wind would feed a nebula 5×103–5×106
times brighter than the 18 µJy persistent-source limit
of Marcote et al. (2020) (Fig. 10). Tidal heating at
rp = 2rtd also deposits the planet's binding energy in
∼ 200 yr. The chromatic activity window—earlier at
high frequency, later at 150 MHz by ∼ 3 d (Pastor-Marazuela et al., 2021; Pleunis et al., 2021)—has no
counterpart in a debris-clump model. The independent re-derivation reproduced every number in this
section.
Figure 11: Victim masses consistent with the NGC 4845
flare, against black-hole mass, for substellar and stellar victims; shaded bands show the black-hole-mass ranges from
the different estimators.

8 The NGC 4845 tidal disruption event

IGR J12580+0134 was a hard X-ray flare in the nucleus of NGC 4845 (January 2011) with a t
−5/3 decline, peak 17–80 keV luminosity 1.5×1042 erg s−1 and
tpeak = 60–100 d. Nikołajuk & Walter (2013) derived
a black-hole mass of 2.3
+1.1
−1.0 ×105 M⊙ from excess variance (systematic range 104–106
) and, with the fallback
fits of Guillochon & Ramirez-Ruiz (2013), a 10% radiative efficiency, a bolometric correction of 10 and
a partial disruption releasing ∼ 10% of the victim, a
“14–30 MJ super-Jupiter”; Lei et al. (2016) quote 8–

40 MJ over 3×105–1.2×107 M⊙, while the other mass

estimators they list (QPO relation, bulge luminosity,
fundamental plane) give 106–2 × 107 M⊙.
The two observables fix only the product M˙
peaktpeak,
i.e. the accreted mass, ≃ 0.5 MJ (0.1/η)(fbol/10). We
inverted tpeak and M˙
peak with the Guillochon &
Ramirez-Ruiz (2013) scalings over η ∈ [0.06, 0.4],
fbol ∈ [1, 10], MBH log-uniform in [104, 2 × 107] M⊙,
impact parameters β across the simulated range, an
Eddington ceiling of 3LEdd, and mass–radius relations
for substellar objects and stars. Acceptable victims
are substellar objects of 2–46 MJ (62% of solutions
at equal class prior) or stars of 0.1–3 M⊙ stripped of
< 1% of their mass at β ≃ 0.5–0.7 (38%); the stripped
mass is 0.4–0.8 MJ in every case (Fig. 11). Forcing the
excess-variance black-hole mass narrows the substellar branch to 4.5–19 MJ but leaves the stellar one at
∼ 25%, and a galactic nucleus offers far more stars
than super-Jupiters on loss-cone orbits. The 2023
NICER detection of weak flares from the same nucleus (arXiv:2504.18558, 2025) shows it to be a low-luminosity AGN, so even the 2011 event's classifica-tion rests on the decline law alone. The super-Jupiter
is one assumption-dependent corner of a degeneracy
that spans three orders of magnitude.

## Page 9

9 Milky Way stars of extragalactic origin

BD+20 2457. Niedzielski et al. (2009) reported two
companions with m sin i = 21.4 and 12.5 MJ at 1.45
and 2.01 AU (e = 0.15, 0.18) around a 2.8 M⊙ giant;
Perottoni et al. (2021) suggested the star formed in
Gaia–Enceladus. The pair is separated by 2.1 mutual
Hill radii, below the 2
√
3 required for Hill stability.
REBOUND integrations (Rein & Liu, 2012) of the
published system end in ejection or e > 0.98 within
35–2500 yr over 16 orbital-phase combinations, 275 yr
for circular orbits, 828 yr with halved masses and 20 yr
for a 1.5 M⊙ star, confirming Horner et al. (2014); the
independent run found 4–270 yr. Whatever produces
the radial velocities of this gigayear-old giant, it is not
that pair of planets.
HIP 13044 b. The 1.25 MJ planet around this
Helmi-stream star (Setiawan et al., 2010) was withdrawn after Jones & Jenkins (2014) showed the signal arose from an erroneous barycentric correction; the
corrected data show no planet.
HD 134440. Reggiani & Meléndez (2018) inferred
past planet engulfment from an abundance difference
between HD 134440 and HD 134439. This is a chemical inference, not a planet detection, and falls outside
the scope of refutation.

10 Discussion

Four failure modes recur.
The favourable reading of an unconstrained scale. A
single event determines a dimensionless combination—
an occulter-to-source size ratio, a lens mass ratio, an
accreted mass, a timescale—and the physical quantity of interest follows only after a scale is supplied: the lens mass (PA-99-N2), the black-hole mass
(NGC 4845), the effective velocity (Q2237+0305), the
number and size of debris clumps (FRB 20180916B).
In each case the published planet is the value obtained
for one choice of scale, and other choices within the
published uncertainties give a star, a black hole or
nothing.
The absent null. The quasar-microlensing populations were inferred from an excess over a null that
counted only one mechanism (stellar caustics) and
omitted the dominant ones (a static broad line sampled by narrow fits in low-count spectra, and the false-detection floor of the threshold itself). The M51-ULS-1b hardness test and shape test were asserted rather
than computed; computed, they carry odds of a few
to one.
Detection without conditioning. An event found in
a search of known sensitivity must be weighted by
the probability of being found. For M51-ULS-1b this
moves the posterior from a Saturn at 45 AU to an M
dwarf at 2 AU and exposes a rate excess of 102–103
;
for PA-99-N2 it is what makes halo remnants, not disc
stars, the most probable lenses.
Internal inconsistency. PA-99-N2's assumed lens
predicts a source size the same light curve excludes; the
FRB planet's assumed engine would have spun down
before the second observing season.
A confirmed extragalactic planet will require a measurement that breaks the scale degeneracy within the
event itself: a microlensing event towards M31 with
both finite-source and parallax signatures, giving θE
and πE and hence the lens mass directly; or an X-ray transit with enough photons in ingress and egress
to distinguish a central crossing from a grazing one
(∆ lnL ≳ 5, roughly seven times the M51-ULS-1b
count rate), together with a measured base rate of look-alike dips in the same source class. Rubin/LSST pixel
lensing of M31 and the Roman microlensing survey of
the Bulge, with their dense sampling, are the plausible
routes; archival Chandra data cannot provide the first
and have not provided the second.

11 Summary

Table 2 collects the outcomes. No entry on the list
of extragalactic planets has been observed: each is a
single unrepeatable event read through a favourable
assumption, a statistic whose null model was not computed, or a claim already withdrawn. None of this
bears on whether planets exist in other galaxies; it
bears on whether any has yet been detected.
Acknowledgements
The analyses in this paper were carried out with the
assistance of an AI system (Claude, Anthropic), which
implemented the calculations described here under the
authors' direction; independent re-implementations of
the load-bearing computations were produced by separate instances with access to the specifications but not
to the primary code. Responsibility for the content
rests with the authors.
Data availability
All code (light-curve reconstruction and fits for M51-
ULS-1b; binary-lens ray shooting, finite-source refits
and lens-population model for PA-99-N2; the Fe Kα
spectral simulation; the FRB energy budget; the tidal-disruption inversion; the N-body integrations), the numerical results in machine-readable form, and the independent verification runs are provided as supplementary material and will be deposited in a public repository on acceptance. Published parameters were taken
from the cited papers; no proprietary data were used.

## Page 10

Table 2: Status of all published extragalactic-planet candidates after this work.
Candidate Claim Status Decisive point
M51-ULS-1b 0.7 RJ transiting planet unconfirmable; planet
disfavoured
dip does not measure size; rate excess 102–103
PA-99-N2 6.3 MJ companion refuted as published needs ρ ≃ 0.1; light curve requires ρ < 0.02
RX J1131−1231 ≳ 2000 planets per star unsupported shift statistic reproduced by a static spectrum
Q J0158,
SDSS J1004
same unsupported same method, 12 and 40 spectra
Q0957+561 3 M⊕ body refuted ≤ 0.3% over years, not 1% in a day
Q2237+0305 1.6 MJ; nanolens
population
dismissed misread caustic crossing; “suggestive”
FRB 20180916B 2.9 M⊕ planet refuted energy budget short by 103.7–107
NGC 4845 TDE 14–40 MJ victim unsupported victim mass degenerate, 2 MJ–3 M⊙
BD+20 2457 b, c two super-Jupiters refuted as published system disintegrates in 4–2500 yr
HIP 13044 b 1.25 MJ refuted (Jones & Jenkins,
2014)
barycentric-correction error
HD 134440 engulfment not a detection —

References

An, J. H., Evans, N. W., Hewett, P., et al. 2004, ApJ,
601, 845 (arXiv:astro-ph/0310457)
Bhatiani, S., Dai, X., & Guerras, E. 2019, ApJ, 885,
77 (arXiv:1909.11610)
Chartas, G., Krawczynski, H., Zalesky, L., et al. 2017,
ApJ, 837, 26 (arXiv:1609.09490)
Colley, W. N., & Schild, R. E. 2003, ApJ, 594, 97
(arXiv:astro-ph/0303170)
Dai, X., & Guerras, E. 2018, ApJ, 853, L27
(arXiv:1802.00049)
Di Stefano, R., Berndtsson, J., Urquhart, R.,
et al. 2021, Nature Astronomy, 5, 1297
(arXiv:2009.08987)
Greiner, J., & Di Stefano, R. 2002, A&A, 387, 944
Guillochon, J., & Ramirez-Ruiz, E. 2013, ApJ, 767, 25
(arXiv:1206.2350)
Hainline, L. J., Morgan, C. W., Beach, J. N., et al.
2012, ApJ, 744, 104
Holman, M. J., & Wiegert, P. A. 1999, AJ, 117, 621
Horner, J., Wittenmyer, R. A., Hinse, T. C., et al.
2014, MNRAS, 439, 1176
Ingrosso, G., Calchi Novati, S., De Paolis, F., et al.
2009, MNRAS, 399, 219 (arXiv:0906.1050)
Ingrosso, G., Calchi Novati, S., De Paolis, F., et al.
2011, General Relativity and Gravitation, 43, 1047
(arXiv:1001.4342)
Irwin, M. J., Webster, R. L., Hewett, P. C., Corrigan,
R. T., & Jedrzejewski, R. I. 1989, AJ, 98, 1989
Jones, M. I., & Jenkins, J. S. 2014, A&A, 562, A129
(arXiv:1401.0517)
Kochanek, C. S. 2004, ApJ, 605, 58
Kurban, A., Huang, Y.-F., Geng, J.-J., et al. 2022,
ApJ, 928, 94 (arXiv:2102.04264)
Lei, W.-H., Yuan, Q., Zhang, B., & Wang, D. 2016,
ApJ, 816, 20 (arXiv:1511.01206)
Marcote, B., Nimmo, K., Hessels, J. W. T., et al. 2020,
Nature, 577, 190
Mosquera, A. M., & Kochanek, C. S. 2011, ApJ, 738,
96
Mottez, F., & Zarka, P. 2014, A&A, 569, A86
Mróz, P., Udalski, A., Skowron, J., et al. 2017, Nature,
548, 183
Mróz, P., Udalski, A., Szymański, M. K., et al. 2024,
Nature, 632, 749
Niedzielski, A., Nowak, G., Adamów, M., & Wolszczan, A. 2009, ApJ, 707, 768
Nikołajuk, M., & Walter, R. 2013, A&A, 552, A75
(arXiv:1304.0397)
Pastor-Marazuela, I., Connor, L., van Leeuwen, J., et
al. 2021, Nature, 596, 505
Paulin-Henriksson, S., Baillon, P., Bouquet, A., et al.
2003, A&A, 405, 15
Perottoni, H. D., Amarante, J. A. S., Limberg, G., et
al. 2021, ApJ, 913, L3
Pleunis, Z., Michilli, D., Bassa, C. G., et al. 2021, ApJ,
911, L3
Refsdal, S., Stabell, R., Pelt, J., & Schild, R. 2000,
A&A, 360, L10
Reggiani, H., & Meléndez, J. 2018, MNRAS, 475, 3502
Rein, H., & Liu, S.-F. 2012, A&A, 537, A128
Reis, R. C., Reynolds, M. T., Miller, J. M., & Walton,
D. J. 2014, Nature, 507, 207
Sand, K. R., Breitman, D., Michilli, D., et al. 2023,
ApJ, 956, 23 (arXiv:2307.05839)
Schild, R. E. 1996, ApJ, 464, 125
Setiawan, J., Klement, R. J., Henning, T., et al. 2010,
Science, 330, 1642
Sumi, T., Koshimoto, N., Bennett, D. P., et al. 2023,
AJ, 166, 108
Tisserand, P., Le Guillou, L., Afonso, C., et al. 2007,
A&A, 469, 387
Tuntsov, A. V. 2024, MNRAS, 528, 1979
(arXiv:2401.05590)
Urquhart, R., & Soria, R. 2016, MNRAS, 456, 1859
(arXiv:1511.05275)
IGR J12580+0134: the nearest tidal disruption event
and its faint resurrection, 2025, arXiv:2504.18558
Wikipedia contributors, “Extragalactic planet”, accessed 2026 October 17
