## Page 1

The Wow! signal faded while it was in the beam:
a recorder-aware reanalysis, a frequency-reference discrepancy,
and constraints on natural and artificial origins
[Author name]*1
1
[Affiliation]
Draft of 17 October 2026

Abstract

The 1977 “Wow!” signal survives as six quantized signal-to-noise values (6EQUJ5) from one 10 kHz channel of the Ohio
State Big Ear telescope. We re-derive what those six numbers
constrain with a forward model of the instrument that includes,
for the first time, the recorder algorithm (N50CH running baseline and σ, floor quantization, 10 s integration in 12 s records)
and an interval-censored likelihood. Three results are new. (i)
The profile is asymmetric: the leading wing is 1.7 units brighter
and the trailing wing 1.5 units fainter than any symmetric beam
allows; a symmetric crossing reproduces data this skewed in
0.37% of Monte-Carlo trials (≈ 2.9σ), while a profile that
fades with an e-folding time of 17+4
−3
s starting ≈ 7 s after beam
centre fits essentially perfectly. The fade explains the blank
second beam 172 s later without additional assumptions and
places the detection in the first beam to sweep the source with
probability 0.89 (Bayes factor 8.4), i.e. at RA 19h27m55srather
than the commonly quoted 19h25m02s. (ii) The second local-oscillator reading at the peak, under the Galactic-standard-of-rest tracking described by the observatory’s staff, implies a
frequency reference of 120.00 MHz rather than the 120.1 MHz
adopted in the 2025 reanalysis, moving the line from 1420.726
to 1420.826 MHz and VLSR from −74 to −95 km s−1(the 2025
paper itself gives both reference values, and its calibrating
clouds post-date the relevant LO change); all candidate velocities are forbidden for circular rotation at l = 11.6
◦
and
fall in the velocity range of the compact-clump HVC complex
GCN. (iii) The 1977 August 15 continuum chart, digitised here,
gives the beam on the night: HPBW 36±1.5 s on both horns
and a beam separation of 181 ± 4 s rather than the assumed
172.4 s; against that beam the Wow! core is unresolved and
the anomaly reduces to a leading excess of ≈ 10% of peak
about 30 s before beam centre, which neither horn’s measured
response reproduces. Recorder absorption of the first record
raises the flux lower limit to ≳ 300 Jy. Simulations exclude
every steady source, including scintillating ones; a stochastic
repeater sits at 1.0% likelihood after 193.5 h of follow-up. A

natural origin requires coherent 21-cm emission from a cold,
dense, tens-of-AU knot pumped by a flare whose geometry
forces a circumstellar host and a flare that reached Earth within
a minute of the pulse; an artificial origin is technologically
undemanding but requires a 10−5–10−2timing coincidence.
We estimate posterior odds of roughly 50–60% anthropogenic
or instrumental, 25–35% natural transient and ≲ 10% artificial
extraterrestrial, and identify four archival tests costing hours to
days that would reorder them.

1 Introduction

The narrowband event recorded by the Ohio State University
Big Ear telescope on 1977 August 15 (local date) remains
the most-cited candidate radio technosignature (Ehman, 2010;
Gray, 2012). Its properties were set in the 1990s (Ehman, 2010;
Gray, 1994) and revised only recently: Méndez et al. (2024)
proposed a natural origin in a flaring cold hydrogen cloud;
Méndez et al. (2025) re-reduced the archival printouts to obtain
a peak flux density ≥ 256 ± 63 Jy, a corrected frequency of
1420.726 ± 0.005 MHz (a spectral-axis inversion and a 2nd-LO reference of 120.1 MHz), a 27 s shift in right ascension
and an upper limit of 1.9
′ on the source size; and Méndez et al.
(2026) published the first account of the Ohio SETI program’s
archive, including >40 000 narrowband events. Follow-up
searches (Gray, 1994; Gray & Marvel, 2001; Gray & Ellingsen,
2002; Harp et al., 2020; Breakthrough Listen, 2022) have found
nothing, and Kipping & Gray (2022) showed that a stochastic
repeater is in 2.4σ tension with the follow-up record.
All of these analyses fit the six printed values with a symmetric Gaussian and treat the printed numbers as linear samples
of the beam pattern. Neither assumption has been tested. Here
we build a forward model of the full signal path, fit it with a
likelihood appropriate to floor-quantized data, and ask what the
data actually constrain (Sect. 2–3). We then simulate the principal origin classes against the same constraints (Sect. 4), work
through the physics of the one surviving natural mechanism
(Sect. 5) and the requirements of an artificial source (Sect. 6),
and argue for a probability assessment (Sect. 7).
1

*Corresponding author. Affiliation and contact to be completed before
submission. The analysis and drafting were carried out with the assistance of
Claude (Anthropic); all code is released with the manuscript.

## Page 2

2 Data and forward model

The data. N50CH printed, every ≈ 12 s per channel, the
integer part of the signal-to-noise ratio of a 10 s mean of 1 s
samples, with 0 blank and 10–35 as A–Z (Ehman, 2010). The
sequence 6EQUJ5 therefore means SNR in [6,7), [14,15),
[26,27), [30,31), [19,20), [5,6) in six consecutive records,
with the records before and after printed blank or “1”. Everything else known about the signal is inferred.
The instrument. Big Ear was a meridian-transit instrument
with HPBW ≈ 8
′
in RA (36–39 s of time at Dec −27◦) and
40′in Dec, two feed horns whose beams were separated by
172.4 s of RA, and a Dicke switch between them at 79 Hz; the
recorded quantity is the difference, and before 1977 October 22
its absolute value was printed, so a steady source produced two
positive events 172 s apart. The negative (west) horn’s beam
swept a source first; the positive (east) horn’s beam second
(Méndez et al., 2025). The running baseline B (weight 1/6) and
σ (weight 1/60) were frozen while a signal exceeded a threshold, which Ehman states was the case for Wow!. We adopt the
per-record freezing he describes and test the alternatives.
Forward model and likelihood. A source of brightness
A b(t) crosses a Gaussian beam of HPBW w centred at t0;
record j averages ten 1 s samples of unit noise starting at 12 j;
the printed value is ⌊S¯
j⌋. The likelihood of a printed k is
P(k ≤ X < k +1) with X ∼ N (mj,0.3162), where mjis the
model record mean and 0.316 = 1/
√
10 is the noise on a 10-
sample mean; records before and after are constrained to X < 2.
Posteriors are computed on grids; model comparison uses
maximum log-likelihood, Bayes factors with explicit priors,
and Monte-Carlo goodness-of-fit (3000 symmetric crossings
through noise, recorder and quantization).

3 What the six numbers constrain

3.1 The profile is asymmetric

The symmetric Gaussian beam reproduces Ehman’s unadjusted
WOWFIT exactly (SSE 7.53 vs his 7.525), which validates
the geometry, but it is a poor fit: maximum lnL = −23.6
against a best achievable ≈ −0.7, because it predicts 4.8 for
the “6” record and 7.0 for the “5” (Fig. 1). Table 1 compares
profile models. Allowing different half-widths on the two sides
gives lnL = −2.7 with HPBW 45.3 s rising and 30.7 s falling;
a physical pulse that is flat and then decays exponentially
from tdec gives −4.7 with tdec = 46.7±1.2 s (≈ 7 s after beam
centre), e-folding time 17+4
−3
s and a beam-side half-width of
44±2 s. The brightness 25 s before beam centre was 2.6
+0.2
−0.6
times that 25 s after.
The significance is assessed by simulation. A true symmetric
crossing with A = 31.2, w = 38.1 s, 1 s Gaussian noise, the
per-record N50CH filter (threshold 6σ) and floor quantization
yields a best symmetric fit as poor as −23.6 in 11 of 3000 trials
Table 1: Profile models fitted to 6EQUJ5 with the interval-censored
likelihood.
Model max lnL Fitted parameters
Symmetric Gaussian beam −23.6 t0=36.7 s, A=31.2,
w=38.1 s
Symmetric sin2x/x
2 beam −33.8 w=39.6 s
Sym. beam, first record absorbed −10.2 A=35.0, w=38.7 s
Sym. beam, switch-off at 65 s −9.8 A=30.7, w=40.3 s
Flat pulse, exponential fade −4.7 tdec=46.7 s, τ=17 s,
w=44 s
Skewed Gaussian, two half-widths −2.7 45.3 s rising, 30.7 s
falling
(p = 0.0037). Ehman’s SSE of 0.32 was reached only after a
post-hoc search over 36adjustments of ±1 to each point.
Instrumental alternatives. Had the baseline updated every
second with weight 1/6, the 6 s time constant would have swallowed most of a 38 s pulse: no amplitude or width reproduces
the data (lnL < −4000 for thresholds of 5–8σ). The data
therefore require per-record freezing, as recollected. The only
surviving recorder effect is absorption of the first record into
the baseline if the freeze threshold exceeded 6σ; it reaches
lnL = −10.2, still 7.5 units short of the skewed profile, and
raises the true peak from 31.2 to 35.0 SNR units (Sect. 3.2).
An asymmetric beam is the remaining instrumental option:
the horns sat 34′and 73′ off the paraboloid axis, so coma
produces a leading or trailing shoulder that should differ between horns. Ehman’s correlation of 6EQUJ5 against 1994
calibrator transits (0.9905 vs 0.9919 for the two horns) has no
power against a 1.5:1 asymmetry. The decisive measurement
is the leading and trailing half-width of each horn’s beam on
the 1977 calibrator transits (OC-230.4, OC-266, OP-282, OF-241, PKS 1628−268) that Méndez et al. (2025) have already
digitized.
Consequence: a fading source and the horn. If the asymmetry is intrinsic, the source lost a factor ∼2.5 in brightness
during the crossing. A pure exponential fade cannot do this—
multiplied by a Gaussian beam it merely shifts a symmetric
profile—so the decline steepened, as for a pulse ending. That
by itself explains why the other beam saw nothing 172 s later,
and it bears on which beam detected the signal. Under the
flat-then-fading pulse model with a log-uniform prior on pulse
duration (1 s to 1 d) and identical priors otherwise, the evidence for detection in the first beam (other beam later) over
the second beam (other beam earlier, which requires the pulse
to have both begun and ended inside a ≈ 250 s window) is a
Bayes factor of 8.4, P(first) = 0.89. The favoured position
is therefore the negative-horn one: RA 19h27m55s ±3
s
, Dec
−26◦57′ ±20′(J2000), l = 11.87◦, b = −19.42◦. Within the
model, fading during the crossing is preferred to no fading
by 2.5 × 107; that preference, however, assumes a beam of
38–44 s and is revisited in Sect. 3.3 with the beam measured
on the night.

## Page 3

Figure 1: The six printed values as quantization intervals (grey bands), with the best symmetric Gaussian beam crossing (grey), the best skewed
profile (blue) and a symmetric beam with the source switching off at 65 s (red). The lower panel shows residuals in units of the per-record noise;
the band is the ±0.5 quantization width. The symmetric model misses the first and last records by −5σ and +5σ.

3.2 Flux, width and angular size

Within the symmetric model the peak is 31.2 ± 0.3 and the
HPBW 37.9±0.5 s; across recorder assumptions the peak is
31–35, so the Méndez et al. (2025) lower limit of 256 Jy becomes 265–300 Jy before any correction for the unknown declination offset (up to ×2). From first principles, Tsys ≈ 100 K
and 0.1 K Jy−1 give an SEFD of ≈ 1000 Jy and a 10 kHz×10 s
Dicke-switched record noise of 4.5–9 Jy, bracketing the 8.5 Jy
adopted there.
The angular-size inference is not robust. With the nominal 8.0
′ beam (35.9 s) the quantization-aware posterior on the
width implies a resolved source of 2.7
′ ±0.8′
(quadrature difference); with the 8.6
′ beam (38.6 s) that Ehman measured
on OY 372 in 1994 the source is unresolved (< 0.5
′
). The
published ≤ 1.9
′
assumes the former beam and a point-like
fit. The 1977 beam width measured in Sect. 3.3, 36 ± 1.5 s,
implies 2.7
′
(+0.8
′/−1.5′
) if the whole profile is one source,
but the core records alone are fitted by a point source once the
leading excess is a separate component.

3.3 The beam on the night of the signal

The 8 MHz continuum chart of 1977 August 15 (Dec strip
−26◦00′set, −27◦ beam; 3 s time constant; Fig. 2) records the
Ohio source OV-221 crossing both horns 50 minutes before
Wow!. Digitising the trace with the grid removed, and calibrating the time axis on the 1910/1920/1930 LST marks (2.11 s
per pixel), gives three numbers nobody had: a half-power
width of 35.7 s for the negative horn and 36.8 s for the positive
horn after deconvolving the time constant, i.e. the nominal
8.0
′ beam at Dec −27◦
(36±1.5 s) rather than the 8.6
′ of the

1994 OY 372 scans; a separation of the two beams of 181±4 s,

5% larger than the 172.4 s derived from the horn spacing and
used in every published position; and the per-horn response at
the six Wow! record offsets, 0.12/0.36/0.78/0.92/0.67/0.16
(negative) and 0.15/0.64/0.91/0.88/0.48/0.10 (positive, after a ramp baseline across a 0.3-peak baseline shift) against
Wow!’s 0.21/0.46/0.85/0.98/0.62/0.18.
Three consequences follow. With the beam fixed at 35–
36.5 s, the Wow! anomaly is a leading excess rather than a two-sided skew: the records E, Q, U, J are fitted by the measured

## Page 4

Figure 2: The two beams measured on OV-221 on 1977 August 15 (continuum chart, digitised and normalised; ramp baseline) compared with a
36-s Gaussian and with the six Wow! records at their offsets from beam centre. Neither horn reproduces the Wow! leading record.
beam, the “5” is reproduced, and the “6” is 2–3 units (≈ 0.1 of
peak) too bright; the best model is the beam plus a component
of 7–12% of peak located 27–31 s earlier (lnL = −5.4 at 35 s,
−9.6 at 36.5 s), while a smooth fade (−29 to −50) and a resolved source (−23.6) fail. Neither horn’s measured response
reproduces that excess: used directly as templates both predict
3.5±1.5 for the “6” record (lnL = −52 to −54), so a 10%
leading shoulder is absent on both horns at the ≈ 2σ level of
this scan (noise ≈ 0.05 of peak). Ehman reports that the 1994
OY 372 scans showed “a plateau only about 10 dB down” on
each side of both horns with unequal amplitudes on opposite
sides, so an asymmetric coma shoulder remains possible instrumentally; it is not seen at the required level in 1977. Finally,
the measured separation moves the first-beam position to RA
19h28m03s ±5
s
. The physical reading becomes: an unresolved
source that was ≈ 2× brighter during the first ten seconds of
the crossing (or had a 10% companion 6–7
′
east) and switched
off, or on, within 181 s on either side; the horn probability of
Sect. 3.1, which rests on the duration prior rather than on the
fade, is unchanged.

3.4 The frequency reference

Méndez et al. (2025) obtain the centre-channel sky frequency
as fc = f2LO − R + 1420.4056 MHz with the 2nd-LO reading f2LO = 120.185 MHz at the peak and a reference R =

120.1 MHz (before 1977 December 13), and, with the inverted

channel axis, channel 2 at fc +0.235 MHz = 1420.726 MHz.
Our astropy reconstruction of their velocity chain is exact:

1420.726 MHz topocentric is −67.6 km s−1; the barycentric

correction is −16.9 km s−1and the standard solar motion
+9.9 km s−1, giving −84.5 and −74.5 km s−1against their
−84±1 and −74±2.
The LO reading, however, is itself a check on R. Méndez
et al. (2026) state that the 2nd LO was software-tuned to hold
the Galactic standard of rest. For the Wow! direction and
epoch the frame offsets of the centre channel are −0.080 MHz
(barycentric), −0.033 MHz (LSR) and +0.166 to +0.180 MHz
(GSR with Θ0 = 220–236 km s−1). Subtracting the GSR offset from the reading gives R = 120.005–120.019 MHz, i.e.
the design value of 120.0 MHz; the LSR gives 120.218, the
barycentre 120.265, and only a barycentric correction applied with the wrong sign returns 120.105 MHz. Either the
LO tracked the GSR as documented and R = 120.0 MHz, or
R = 120.1MHz and the LO was not tracking the GSR at that
moment; the two 2025–2026 papers cannot both be right about
this. The three candidate references give channel-2 frequencies
of 1420.726, 1420.826 and 1420.926 MHz and VLSR = −74,
−95 and −116 km s−1. Méndez et al. (2025) fixed the post-December-13 reference (119.9 MHz) by matching the Wow2
and Wow3 clouds of January 1978 to HI4PI, which is sound,
but those clouds post-date the software change and so never
calibrated the August 1977 value; for that value the paper is
internally inconsistent, giving 120.1 MHz “(not 120.0 MHz)”
in one passage and describing the December 13 update as moving the LO “from 120.0 MHz to its correct value of 119.9 MHz”
in another. The LO reading at the peak, under the documented
GSR tracking, agrees with the second statement. A plot of
LO reading minus predicted frame offset against date over
1977–78 would settle both the frame and R to ±2 km s−1.
Two further points. At l = 11.6
◦
, b = −18.8
◦
a flat rotation
curve (R0 = 8.15 kpc, Θ0 = 236 km s−1; Reid et al., 2019)
gives VLSR = +6 km s−1at 1 kpc, +23 at 3 kpc and +172 at
8 kpc, turning negative only beyond 17 kpc where the sightline
is 5.5 kpc below the plane: all three candidate velocities are
forbidden for circular motion, and any H I host is intermediate-or high-velocity gas. The field lies inside the footprint of
the HVC complex Galactic Center Negative (l ≃ 0–70◦, b ≃

## Page 5

−60◦
to +10◦, VLSR from −350 to ≃ −70 km s−1; Winkel et
al., 2011), 243 compact and mostly unresolved clumps with
almost no diffuse envelope, a natural host population at these
velocities. Finally, the Galactic latitude printed for the positive
horn in Table 4 of Méndez et al. (2025), −17.85◦, does not
follow from its RA and Dec, which give b = −18.82◦(the
negative-horn value is reproduced); a 1◦error propagates into
any cross-match.

4 Origin simulations

Each scenario was tested against five facts: a 38 s point-like
crossing; the skew; detection in one beam and < 2σ in the
other 172 s away; the line frequency; and no recurrence in
178 further Big Ear passes (1977–84) plus 193.5 h of targeted
follow-up. Figure 3 shows the two-beam constraint and the
repeater likelihood.
Steady sources. Any steady celestial source is excluded: the
second beam would have printed ≥ 30 and 178 later passes
stayed blank. A steady source seen through diffractive interstellar scintillation (gamma-distributed intensity, independent
scintles between beams and days) has a maximum likelihood
of 3×10−12 at a mean flux of 11 Jy for modulation index unity,
and 10−44 once the follow-up sensitivity caps the mean flux.
Extended H I clouds of the Wow2/Wow3 type (Méndez et al.,
2025) give 50–60 s crossings at ∼ 3.5σ in both beams every
day.
Repeaters. With the exact one-beam-only geometry (a pulse
covers one beam and misses the other only if it starts or ends
within a 104 s window), 90 Big Ear visits give a maximum
likelihood of 27% for a stochastic repeater, 1.0% once the
193.5 h of follow-up are added (best fit D ≈ 170 s, rate ≈
0.12 d
−1
; 2.6σ tension), reproducing Kipping & Gray (2022)
(32%, 1.8%). A further ≈ 750 h would push every repeater
below 0.27%. One caveat they did not raise: META’s 400 kHz
band centred on the rest frequency would not have contained

1420.726 MHz, so 8 of the 193.5 h may not count; Hobart’s

2.5 MHz band (Gray & Ellingsen, 2002), the ATA and the GBT

did cover it. Strictly periodic repeaters are excluded below
14–40 h (Gray & Ellingsen, 2002; Harp et al., 2020).
Moving objects and interference. The width constrains the
source to the sidereal rate within 4%, i.e. |µ| < 0.6
′′ s−1
: this
excludes Earth satellites and aircraft but allows 435 km s−1
transverse at 1 AU and anything slower than 14◦ d
−1
among
solar-system bodies, which the two-beam test then removes
unless the object moved > 7
′′ s−1
in declination (a circular
orbit radius of ≈ 70000 km). For terrestrial interference, the
often-quoted (1/32)
6 ≈ 10−9
is the probability of one exact
character string, not of a beam-shaped pattern; a Monte Carlo
of 400 lognormally modulated smooth bursts per correlation
time (15, 40, 100 s) passed through the recorder finds that 0.3–
1.5% mimic a crossing in shape and width. Against that stands
the base rate: the Ohio archive holds > 40000 events above
3σ that passed the antenna-pattern filter, and a 30σ event in
the “southern hot spot” within a year of Wow! (Méndez et al.,
2026).

5 A natural one-off transient

Only one natural mechanism satisfies all five facts. Every
broadband emitter (pulsar giant pulses, magnetar radio bursts,
flare continua) is excluded by the blank adjacent channels;
electron-cyclotron bursts from flare stars would need the star
within 0.3 pc; recombination and molecular lines are ≥ 4 MHz
away; extragalactic H I is redshifted. What remains is stimulated or coherent 21-cm emission from cold hydrogen, pumped
on a timescale of a minute.
Maser or coherent burst. The gain arithmetic does not exclude an ordinary maser; the fade does. With τ = NH/(1.82×
1018 Ts ∆v), a cloud with NH = 2×1020 cm−2, ∆v = 2 km s−1
and a 1% hyperfine inversion (|Ts| ≈ 1.7 K) has |τ| ≈ 8 and amplifies the 6 K sky to ≈ 18000 K, the brightness temperature a
1.9
′
source needs for 256 Jy. The widely quoted requirement of
103× normal densities (Méndez et al., 2024, eq. 15) assumes an
inversion of 6×10−7, the limit for a blackbody-shaped pump;
a steep Lyman-α profile allows 10−3–10−2 before multiple
scattering thermalises it. But an amplifier cannot switch off
faster than its light-crossing time: a 17 s fade bounds the path
to 5 × 1011 cm (0.03 AU) and the density to 4 × 108cm−3—
unless the pump sweeps through the gas toward the observer,
so that pump and 21-cm photons travel together and the whole
path contributes within the pump’s duration. That gain-swept
configuration is the one in which the published 21-cm superradiance model (Rajabi & Houde, 2016) has a “minutes”
regime: TR = 1 s, delay ⟨τD⟩ = 66 s, bursts of a few hundred
seconds from samples ∼ 1014 cm long, nH = 10 cm−3, 1%
inversion—numbers that match the Wow! fade, duration and
two-beam window without tuning, with isotropic energies of
only 3×1029 erg at 1 kpc.
Two unproven requirements. Collective emission needs
velocity coherence ∆v ≲ λ/(2πTR) ≈ 3 cm s−1inside each
coherent sample, four to five orders of magnitude below the
350 m s−1thermal spread at 15 K; Rajabi & Houde (2016)
acknowledge this and do not resolve it. And a coherent sample
of width w radiates into a fraction ≈ 3 × 10−14 of the sky
for w = 300 km, so the emission direction must be fixed by
the pump (radially away from the trigger) and Earth must lie
on the trigger–knot line within the knot’s radius: probability
(s/r)
2/4, i.e. 2% for a 15 AU knot 50 AU from its star, 10−9
at
1 pc, 10−12 at 50 pc.
Pump and trigger. Wouthuysen–Field pumping (Wouthuysen, 1952; Field, 1958) fast enough to set up the inversion
within ∼ 60 s requires a Lyman-α flux of ≈ 17 erg cm−2s
−1
at the knot: within 46 AU of a 1035 erg M-dwarf superflare,

## Page 6

Figure 3: (A) The two-beam constraint: a source detected at > 30σ in one beam must have been below 2σ when the other beam crossed it
172 s earlier or later, so a top-hat emitter lasted 70–245 s or faded by > 15× within three minutes. (B) Maximum likelihood over repeat rate for
a stochastic repeater of pulse duration D, with exact single-pulse geometry, 90 Big Ear visits and the follow-up hours of Kipping & Gray (2022)
plus Breakthrough Listen (2022).
150 AU of a 1037 erg giant flare, 0.13 pc of a magnetar giant-flare tail (at 10−4 Lyman-α efficiency) or 50 pc of its 0.2 s
spike. Big Ear’s exposure (14 sky-minutes of 8
′ ×40′ beams
over 1977–84, more than all modern H I surveys combined)
and one event imply an all-sky rate of ∼ 100 events per day
at ≥ 250 Jy (90% range 5–300). Stellar superflares occur at
∼ 3×105 d
−1 Galaxy-wide, so the rate is met if ∼0.1–2% of
superflaring stars host a cold H I knot within ∼ 50 AU; the magnetar trigger proposed in the literature fails on pump efficiency
(a 1018 cm−2 knot is transparent to keV X-rays), on duration
(the spike lasts 0.2 s against a 60 s pump requirement) and on
alignment, together by more than ten orders of magnitude. The
natural hypothesis therefore predicts a dense, cold, tens-of-AU knot of the tiny-scale-atomic-structure type (Heiles, 1997,
2007) at the position of a flaring star whose radial velocity is
−84, −105 or −127 km s−1, a flare that reached Earth within
a minute of 03:16 UTC on 1977 August 16, and a 21-cm light
curve that copies the flare’s. The accessible Helios-2 burst
papers of 1979 list five triangulated events in 1976–77 (none
in August 1977); the complete Vela 5/6 record for that night
remains to be checked. It also predicts, for any smooth luminosity function, hundreds to 105 one-pass narrow spikes at
|VLSR| > 50 km s−1in the RFI-rejection products of ALFALFA,
FAST and HI4PI.

6 An artificial source

The received power flux, ≥ 2.6 × 10−20 W m−2regardless of the signal’s intrinsic width, requires EIRP ≥ 3 ×
1014 (d/pc)

2 W: 2.4 GW into an Arecibo-class dish at 10 pc,

240 GW at 100 pc, 7 TW at 548 pc; a 3 km phased array needs
100 times less (Table 2). Energy is not a constraint for a
Table 2: Transmitter power for the Wow! flux. EIRP = 3 ×
1014(d/pc)

2 W.

d EIRP (W) 300 m dish 3 km array 30 km array

100 AU 7×107 6 W – –

1 pc 3×1014 24 MW 240 kW 2.4 kW
10 pc 3×1016 2.4 GW 24 MW 240 kW
100 pc 3×1018 240 GW 2.4 GW 24 MW
548 pc 9×1019 7 TW 71 GW 710 MW
1 kpc 3×1020 24 TW 240 GW 2.4 GW
civilization a century or two ahead of ours. Nor would our
own technology qualify: Earth’s planetary radars and the 1974
Arecibo message would deliver the Wow! flux only to 0.26–
0.6 pc, all of Earth’s electricity radiated isotropically to 0.08 pc,
and a Kardashev-I civilization to 24 pc; the one Earth analogue
reaching stellar distances is a Starshot-class propulsion beamer
(∼ 1020 W EIRP for minutes per launch), visible to ≈ 570 pc.
Leakage is thus excluded, and the emission was collimated
toward us.
The difficulty is timing. Big Ear watched two 8
′ × 40′
patches and spent ∼ 3 d on each of ∼ 300 declination strips, so
a transmission of duration D at a random moment was caught
with probability ≈ 2(D+72s)/(300×86164s): 2×10−5for
a 3 min ping, 3×10−4for an hour. A sweeping beacon of the
cost-optimised type (Benford et al., 2010), dwelling 2–4 min
on each of 104–105targets, is the only artificial variant with
a quantifiable likelihood, and it peaks at 1–2% (revisit of order a week) once the null follow-ups are counted. Accidental
high-gain beams (propulsion or radar) and in-system probes
need no repetition but cannot be re-observed. The profile’s

## Page 7

gradual 15–20 s decline fits a beam sweeping off us or a power
ramp-down (lnL = −4.7) better than a switched transmitter
(−9.8).
A transmitter radiating at the H I rest frequency in its own
frame fixes its host’s heliocentric velocity at −84.5, −105.6
or −126.7 km s−1for the three references; a signal placed at
the line in the solar-barycentric, LSR or GSR frames would
have appeared at 1420.326, 1420.373 or 1420.571 MHz, none
of which was observed. A Gaia DR3 census of the first-beam
box (3
′ ×40′
around 19h27m55s, through the Harvard VizieR
mirror) returns 33 stars with radial velocities, spanning −200
to +120 km s−1 with a dispersion of 69 km s−1, so that 0.3–
0.5 chance matches per candidate velocity were expected at
±3 km s−1; none occurred. The nearest approaches are a
G = 12.9 star at 870 pc with −75.8 km s−1and two distant
halo stars at −122.5 and −130.7 km s−1; nothing lies near
−105.6 km s−1. The second-beam box (19h25m02s) holds
40 such stars and one match: a G = 14.3, bulge-distance
giant (parallax 0.12 mas) 16′ north of the box centre with
−83.98 km s−1, 0.5 km s−1from the −84.5 prediction; in a
field with an 81 km s−1 velocity spread 0.57 chance matches
were expected at that velocity, so this is a target for follow-up, not evidence. Both censuses constrain only G ≲ 14, i.e.
giants and F–K dwarfs to ∼1 kpc; M dwarfs beyond ∼100 pc
have no Gaia velocities. GASS and LAB spectra at both
positions (0.3
◦ beam) show a single local H I component at
VLSR ≈ 0 km s−1and nothing above ≈ 0.2 K at −74, −95 or
−116 km s−1: no extended gas and no GCN clump lies in the
beams, as the circumstellar-knot variant of Sect. 5 predicts
and the extended-cloud variant does not. The Sun-like star
2MASS J19281982−2640123 proposed by Caballero (2022)
and observed by Breakthrough Listen (2022) lies 5.5
′
east and
17′ north of the revised first-beam position (beam response
≈ 0.12, requiring ≥ 2000 Jy) and has a Gaia radial velocity
of −13.7±6 km s−1; it is no longer a strong candidate. The
expected nearest star in the two 1.5
′ × 40′
error boxes is at
≈ 140 pc, where the signal left in 1521, Earth’s 2012 Arecibo
reply arrives in 2470 and an answer could not arrive before

2926. At any distance beyond ≈ 7 pc the sender could not have

known of human technology.

7 Discussion: a probability assessment

We group the hypotheses as HA (anthropogenic or instrumental), HN (natural one-off transient) and HE (artificial extraterrestrial), and argue for posterior odds of roughly 50–60%,
25–35% and ≲ 10%. The argument is a product of factors,
each of which we state so that readers can substitute their own.
Base rates. The same instrument logged > 40000 narrowband events passing its pattern filter, with a 30σ event elsewhere within a year, and the recorder is known to interact with
gain changes (Méndez et al., 2026); every other candidate technosignature in six decades has resolved to interference. The
prior odds for HA against the union of the other two are therefore large, of order 10:1 or more, before the Wow!-specific
evidence is considered. For HN the prior is the probability that
a mechanism never observed in 70 years of 21-cm astronomy
exists at the required rate, which we put at 0.1–0.3; for HE
the prior is the probability that a transmitting civilization lies
within a few hundred parsecs along this sightline, which no
current data constrain to better than 10−3–10−1.
Shape and width. A beam-matched width (4%) and a 38 s
crossing are automatic for any celestial point source and occur
for ∼1% of random smooth bursts. This is a likelihood ratio
of ∼100 for celestial over terrestrial, per burst; multiplied by
dozens of strong bursts in the archive it leaves HA with an
expected ∼0.1–0.5 Wow!-shaped impostors over the program,
i.e. not improbable.
The fade and the blank second beam. These favour any
intermittent source over any steady one, which is why all steady
sources are excluded (Sect. 4), but they do not discriminate
between HA, HN and HE: interference is intermittent by nature,
a pumped burst ends, and a beam sweeps on. The gradual
decline mildly favours a physical decay or a beam sweep over
a switched transmitter.
Frequency. Being within 0.3 MHz of the hydrogen line is
predicted by HN (the line is the only natural candidate) and is
a plausible deliberate choice under HE, but it carries no weight
against HA: any interference Big Ear could see had to fall in
its 500 kHz window, and the base rate above already counts
in-window events. The velocity, forbidden for disk gas, costs
HN a factor of a few (a halo-velocity host is rarer than a disk
one) and costs HE nothing.
Non-recurrence. 178 Big Ear passes and 193.5 h of follow-up are neutral for one-off versions of all three hypotheses
and penalise repeating ones; the only quantifiable repeater, a
sweeping beacon, retains 1–2%.
The timing coincidence. This is where HE loses. Every
artificial scenario must explain why two small beams happened
to be on the source during the minutes it pointed at us: 10−5–
10−3for one-off emission, ∼ 10−2for the best repeater. HN
pays the same coincidence but has it priced into the rate (one
event in 14 sky-minutes), which is a statement about the all-sky rate rather than about luck; HA pays nothing, because
interference is local and frequent.
The physics penalty. HN in turn pays for two unestablished
requirements (cm s−1coherence; an aligned circumstellar geometry) and for a host population—dense neutral knots within
tens of AU of flaring stars—that has never been observed; we
assess this at a factor of 3–10 against it. HE pays no physics
penalty; HA pays the penalty of having no identified emitter:
a frequency-stable 10 kHz source in a protected band, lasting

## Page 8

minutes, strong enough to look like 250 Jy, never heard again,
which we assess at a factor of 3–10 as well.
Combining: HA starts far ahead on base rate and loses a
factor of order 10 on shape and 3–10 on the missing emitter;
HN starts behind, gains on shape and frequency, and loses 3–10
on physics; HE starts behind, gains on shape and frequency, and
loses 102–104 on timing. The outcome is the ordering above,
with HA and HN within a factor of two of each other and HE
an order of magnitude below. We regard the split between HA
and HN as genuinely open and the position of HE as robust
to any plausible choice of priors short of assuming a nearby
civilization.
Limitations. The per-record noise is taken as 1/
√
10 of the
1 s noise; if the 1 s samples were correlated the asymmetry
significance drops (the skewed model’s advantage falls from
21 to 3 log-units for a threefold larger noise) but the preference
remains. The N50CH freeze threshold is undocumented and
was scanned over 3–15σ. The LO argument rests on the staff’s
statement of GSR tracking and on the published formula; the
LO logs would resolve it. No H I spectrum at the position and
no Gaia census could be retrieved in this work.

8 Tests

Ranked by cost: (1) per-horn beam widths and leading/trailing
half-widths from the 1977 calibrator transits (done here for
OV-221 from one scanned chart; a higher-resolution scan and
the other calibrators would sharpen the ≈ 2σ shoulder limit);
(2) LO reading minus predicted frame offset against date for
1977–78 (days; settles R and the velocity); (3) a Gaia DR3
census of the two error boxes with radial velocities, flagging
−84.5, −105.6 and −126.7±3 km s−1and flare activity (done
here for both boxes: one chance-level match in the second box;
the first box should be repeated 2
′
east and the faint M-dwarf
population remains); (4) VLA/MeerKAT H I absorption at both
positions at the three velocities (single-dish spectra are null);
(5) the Vela 5B/6A record for 03:13–03:16 UTC 1977 August
16 (the published Helios-2 events exclude a triangulated burst
that night); (6) a one-pass narrow-spike search in survey RFI
products; (7) ≥ 750 h of continuous, Hz-resolution, full-Stokes
monitoring of both 40′ boxes, for which the flux makes a small-dish network sufficient.

9 Conclusions

Six quantized numbers still contained one unused observable—
their asymmetry—and the beam measured on the night sharpens what it means: the core is the 36-s beam, unresolved, and
the first record carries a ≈ 10% excess that neither horn’s measured response produces, so the source was briefly brighter (or
accompanied) at the start of the crossing and switched within
181 s on either side; the detection sits in the first beam, now at
RA 19h28m03s, with probability 0.89. The frequency rests on
a 2nd-LO reference that the LO reading itself contradicts under
the documented tracking mode, and the size limit rests on an
unmeasured beam width; both are resolvable from existing
records. No origin is identified. The natural and anthropogenic
readings are within a factor of two of each other; the artificial reading is not excluded by any physics but is an order
of magnitude behind on the single question of why we were
listening.
Data and code availability
All fits, simulations and geometry calculations are reproduced
by seven short Python scripts (numpy, scipy, astropy 8) released
with this manuscript; every number in the tables regenerates in
under 30 minutes.

References

Benford, G., Benford, J., & Benford, D. 2010, Astrobiology,
10, 475; 491
Perez, K., et al. 2022, Res. Notes AAS, doi:10.3847/2515-
5172/ac9408
Caballero, A. 2022, Int. J. Astrobiology, arXiv:2011.06090
Ehman, J. R. 2010, The Big Ear Wow! Signal: 30th Anniversary Report, https://bigear.org/wow20th.htm
Field, G. B. 1958, Proc. IRE, 46, 240
Gray, R. H. 1994, Icarus, 112, 485
Gray, R. H. 2012, The Elusive Wow (Palmer Square Press)
Gray, R. H., & Marvel, K. B. 2001, ApJ, 546, 1171
Gray, R. H., & Ellingsen, S. 2002, ApJ, 578, 967
Harp, G. R., Gray, R. H., Richards, J., Shostak, G. S., & Tarter,
J. C. 2020, AJ, 160, 162
Heiles, C. 1997, ApJ, 481, 193
Heiles, C. 2007, in ASP Conf. Ser. 365, SINS: Small Ionized and Neutral Structures in the Diffuse ISM, arXiv:astro-ph/0701625
Kipping, D., & Gray, R. 2022, MNRAS, 515, 1122
Méndez, A., Ortiz Ceballos, K., & Zuluaga, J. I. 2024,
arXiv:2408.08513
Méndez, A., et al. 2025, arXiv:2508.10657
Méndez, A., Dixon, R. S., & Childers, R. K. 2026,
arXiv:2606.11102
Rajabi, F., & Houde, M. 2016, ApJ, 826, 216
Reid, M. J., et al. 2019, ApJ, 885, 131

## Page 9

Winkel, B., Ben Bekhti, N., Darmstädter, V., et al. 2011, A&A,
533, A105
Wouthuysen, S. A. 1952, AJ, 57, 31
