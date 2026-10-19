## Page 1

Under what conditions do outer giants coexist
with inner small planets?
Orbital coherence, excitation history, and observational selection
[Author name(s)]
[Institutional affiliation(s)]

15 October 2026

Abstract

Outer giants coexist with inner small planets when formation supplies the inner system and subsequent perturbations avoid destructive differential orbital excitation. We examine the dynamical part of this statement with a
public-catalog audit, a screen of 1,719 synthetic architectures, 694 direct integration jobs including controls and
numerical checks, and 1,008 reduced secular histories. In 24 deliberately stress-selected architectures, coherent eccentricity vectors yield 39/48 encounter-free realizations over 20,000 yr, compared with 11/48 circular starts; halving the
timestep gives 39/48 and 15/48. Removing the giant yields 48/48, whereas shuffling inner apses at fixed eccentricity
magnitudes yields 1/48. Selected coherent realizations persist for one million years, but others fail. Prescribed slow
giant excitation and gradual removal of inner damping can generate low free eccentricity from circular starts. These
histories are reduced disk models, and an apparent faster-growth survival disadvantage disappears on numerical refinement. Scattering produces both weakly forced survivors and damaging trajectories. A fixed California Legacy
Survey selection contains four coexistence hosts among 58 detected-giant hosts. Their modeled coherent eccentricity
harmonics are only 10−4–2 × 10−2 m s−1, making this sample a weak test of orbital coherence. Coexistence is therefore favored by weak differential forcing, sufficiently strong internal coupling or additional precession, and compatible
eccentricity vectors populated by favorable histories. The calculations support this conditional explanation, but do
not establish a universal giant-mass, eccentricity, or separation threshold, a population survival fraction, or a unique
formation pathway.
Keywords: planetary systems — celestial mechanics — planet formation — methods: numerical — methods: statistical

1 Introduction

The presence of a giant planet outside a compact system
does not by itself determine the fate of the inner planets.
Coexistence requires at least two physical conditions: the
inner planets must form, and the later system must avoid
destructive evolution. A third condition governs what is
observed: both populations must be detectable. These
conditions depend on different variables and should not
be inferred from a single observed correlation.
Formation calculations show that the timing of inner
growth, the supply of solids, and disk thermal structure
affect whether small planets develop alongside cold giants
[1]. An exterior giant can restrict inward material transport, but its presence does not imply that the inner region was empty when that restriction began. The present
work does not calculate embryo growth or pebble transport. We address the subsequent dynamical requirement,
while keeping this formation condition explicit.
The observed association between inner small planets
and outer giants also depends on population definitions.
Positive associations have been reported [2, 3, 4], with differences involving giant mass [5], metallicity conditioning
[6], and the distinction between super-Earths and sub-Neptunes [7]. The hot-planet sample of Liu et al. [8]
and the warm-planet sample of Ruggieri et al. [9] probe
different regions of this problem. A single occurrence enhancement is not a universal coexistence condition.
The relevant dynamical ingredients are well established.
An inner system can resist a companion when its mutual
coupling dominates differential external forcing, while secular resonances can amplify the response [10]. Rapid relativistic precession can suppress eccentricity excitation at
very small orbital radii, including in inclined systems [11].
At fixed final outer architecture, the history of scattering
changes the excitation inherited by the inner system [12].
The instantaneous masses and orbital sizes therefore leave
out physically consequential information.
An additional distinction is between scalar eccentricity
and the eccentricity vector. Circular inner orbits in the
presence of an eccentric companion generally contain free
secular oscillations. A coherently precessing eccentric configuration can have less damaging relative motion even
though its individual eccentricities are larger. Forced-eccentricity initial conditions improve packing stability in
a stellar-binary setting [13], and aligned eccentric configurations can survive longer in closely spaced planetary systems [14]. Smooth external excitation and damping can
populate coherent states [15, 16]; these are precedents,
not mechanisms introduced here.
We combine three tests. First, we compare controlled
inner states at fixed giant properties to isolate dynamical sensitivity. Second, we ask whether initially circular
systems reach low free eccentricity through prescribed

## Page 2

growth, damping removal, or self-consistent giant scattering. Third, we use public survey products to assess
whether the predicted orbital states can presently be distinguished. The resulting answer is conditional: weak
forcing can permit coexistence without special coherence,
whereas coherence may matter near a more strongly perturbed boundary. We quantify the evidence and its numerical limitations rather than fitting a universal boundary.

2 A conditional dynamical

framework

2.1 Architecture, state, and history

Let A describe the full architecture, including inner spacing, planet masses, mutual inclinations, and additional
companions. Let z denote the eccentricity vectors and h
their excitation history. A survival probability at age t
would require averaging a conditional survival function,
Psurv(t | O) = ∫S(t | A, z, h) p(A, z, h | O) dA dz dh,
(1)
where O denotes the available observations. This expression is a bookkeeping statement, not an inferred model.
We calculate selected values of S over finite horizons. We
do not infer the distribution supplied by formation, de-project masses, or estimate the posterior average in this
equation.
A large giant pericenter relative to the outermost small
planet often reduces external perturbations. Strong inner
mutual coupling can reduce differential excitation, and
additional apsidal precession can move a system away
from a secular resonance. None supplies a universal one-parameter criterion: the response also depends on the
spectrum of precession frequencies, eccentricity vectors,
resonance proximity, inclination, and perturbation history. Stable coexistence need not be coplanar or apsidally
aligned. Our principal numerical comparison isolates the
planar eccentricity channel.

2.2 Secular states and free-mode action

For planar orbits, write zj = ej exp(iϖj ). In linear
Laplace–Lagrange theory,
z˙ = iAz. (2)
We retain the giant as a gravitating member, including
its backreaction. For j ̸= k, define αjk as the smaller-to-larger semimajor-axis ratio and α¯jk = αjk if j is interior,
otherwise unity. With nj = [G(M∗ + mj )/a3
j
]
1/2
,
Ajj =
nj
4
∑
k̸=j
mk
M∗ + mj
αjkα¯jkb
(1)
3/2
(αjk), (3)
Ajk = −
nj
4
mk
M∗ + mj
αjkα¯jkb
(2)
3/2
(αjk). (4)
The Laplace coefficients are evaluated through a hypergeometric representation and checked independently by
quadrature.
With Wjj = [mj
√
(M∗ + mj )aj ]
1/2
, the adopted matrix is symmetrized as H = W AW−1
. Let U be its
orthonormal eigenvectors, gk the frequencies, and V =
W−1U. The mode kg with maximum U
2
gk is our giant-dominated reference. Normalized to the initial giant eccentricity, the prepared and circular states are
zcoh = egV kg/Vgkg, (5)
zcold = (0, . . . , 0, eg)
T
. (6)
All 48 selected reference modes have aligned apses. This
does not assert that alignment is the only protective configuration. Nor is a linear eigenmode an exact periodic
solution of the finite-eccentricity gravitational problem.
Using c = U
TWz, we normalize the non-reference action as
F =
∑
k̸=kg
|ck|
2
∑
k̸=kg
|ck,cold|
2
, ∆g = min
k̸=kg
|gk − gkg|, (7)
where the cold state has the same instantaneous giant vector. Thus F = 0 for the pure reference mode and F = 1
for circular inner orbits. For z = (1 − η)zcoh + ηzcold,
F = η
2
exactly. This normalization is a diagnostic, not a
new invariant or a universal survival threshold. When the
giant eccentricity is tiny, the denominator can produce a
large ratio despite weak absolute excitation. Nonlinear
evolution, inclination, semimajor-axis drift, and osculating short-period terms further limit its interpretation.

2.3 Relative geometry and encounter

endpoints
For two coplanar ellipses with pj = aj (1−e
2
j
) and p1 ̸= p2,
equality of the polar radii gives the instantaneous intersection diagnostic
X12 =
|p2z1 − p1z2|
|p2 − p1|
. (8)
The osculating curves intersect or touch when X12 ≥ 1.
By contrast, (a1e1 + a2e2)/(a2 − a1) ≥ 1 only indicates
overlap of radial ranges. Alignment can reduce the vector
difference in equation (8) while those ranges overlap.
Neither diagnostic guarantees dynamical stability or
predicts encounter time. Mean-motion resonance overlap
can matter before orbit crossing [17]; angular-momentum-deficit stability supplies a useful sufficient secular condition, but failure of that condition does not prove instability [18]. We therefore use secular geometry for selection and full gravitational integration for finite-time endpoints.

## Page 3

3 Data and numerical design

3.1 Public catalog context

The retained NASA Exoplanet Archive default-solution
snapshot [19], retrieved on 14 October 2026, contains
6,445 planets around 4,842 named hosts. For this contextual audit, an inner small planet has a < 1 au and either
radius 1–4 R⊕ or measured/minimum mass 1–20 M⊕. A
giant has measured/minimum mass 0.3–13 MJ and a = 1–
10 au. Limits are excluded from the relevant selection
branch; missing semimajor axes are inferred from period
and stellar mass when possible.
This definition gives 37 coexistence hosts, 42 qualifying
giants, and ten hosts with multiple selected small planets. Of the giants, five lack eccentricities and two have
eccentricity upper limits. Among the 35 uncensored values, the giant-weighted median qg/ai,out is 17.78, or 6.57
in the multiple-small-planet subset. In comparison, our
stress-selected simulations span 1.81–2.87, with median

1.95. They deliberately probe a more strongly perturbed

regime than most catalog examples.
The count changes with the definition: giant lower-mass cuts of 0.2, 0.3, and 0.5 MJ give 38, 37, and 33 hosts.
At 0.3 MJ, radius-only and mass-only definitions give 24
and 32. The catalog lacks a common survey denominator and recovery function. These are detected examples,
not an occurrence measurement or observationally fitted
simulation initial conditions.

3.2 Controlled architecture ensemble

We generate 1,800 proposals around a solar-mass star,
with random seed 20261014. Each has two or three
coplanar inner planets, a1 = 0.2 au, common adjacent
semimajor-axis ratio uniform on 1.22–1.65, and independently log-uniform masses of 1–12 M⊕. The giant has log-uniform ag = 1–4 au and mass 0.3–10 MJ, and uniform
eg = 0.08–0.50. Rejecting qg/ai,out < 1.8 and prepared
inner eccentricities above 0.5 leaves 1,719 architectures.
We sample the analytic secular evolution at 4,096
epochs over 105 yr. The 24 highest circular-start intersection diagnostics form the stress cohort. A further 24 architectures are drawn from the remaining pool with seed
2718 as a comparison cohort. Selection on a circular-start
diagnostic intentionally enriches the first cohort for possible contrasts; the comparison is not an unbiased population survival experiment or a held-out sample.
Each architecture has four inner-state prescriptions:
circular; prepared coherent; prepared with independent
10% Gaussian fractional eccentricity perturbations and
10◦ Gaussian apsidal perturbations; and prepared eccentricity magnitudes with uniformly shuffled apses. The
giant starts at ϖg = 0. Mean anomalies are randomized
with seeds 101 and 202 and matched across prescriptions.
This gives 384 primary integrations.
We use REBOUND 5.2.2 with WHFast [20], timestep
P1/40, corrector order 11, and a 20,000-yr horizon. Initial
Table 1: Encounter-free completions at 20,000 yr. Counts
are conditional on the selected architectures.
Initial inner state Stress cohort Comparison
Circular 11/48 48/48
Coherent 39/48 48/48
Coherent, perturbed 37/48 48/48
Apses shuffled 1/48 44/48
Circular, no giant 48/48 —
Circular, P1/80 15/48 —
Coherent, P1/80 39/48 —
elements are heliocentric and subsequently transformed
to the center of mass. Encounter termination uses one
fixed distance: the smallest initial mutual Hill radius
among adjacent inner pairs, applied to all particle pairs in
that architecture. Escape beyond 100 au, unbound osculating orbits, and sampled pericenters inside 0.00465 au
are also monitored. Every non-completed primary run
reaches the encounter endpoint. An encounter is not a
simulated destruction event; remaining multiplicity is not
followed afterward.
Additional runs remove the giant, halve the timestep,
compare with adaptive IAS15 [21], vary the initial mode
loading, and extend selected systems to 106 yr. The baseline comprises 628 distinct jobs. The history study adds
66, for 694 direct jobs in total. This count includes pilots,
controls, and reruns of the same initial configurations, not
694 independent systems (Appendix A).

4 Dependence on orbital state

4.1 Prepared, circular, and shuffled

states
Table 1 gives the primary endpoint counts. Among 48
stress-cohort realizations per prescription, 39 coherent
states complete the horizon, versus 11 circular states.
Mildly perturbed coherent states yield 37 completions;
shuffled apses yield only one. In the comparison cohort,
circular, prepared, and mildly perturbed states all give
48/48, while shuffled states give 44/48.
The shuffled control preserves scalar eccentricity magnitudes and changes apsidal phases and mode content.
Only two stress-cohort shuffles initially have intersecting inner conics; excluding them leaves 1/46 completions.
The poor outcome is therefore not explained by initializing most of those systems with intersecting ellipses. Conversely, removing the giant from all 48 matched circular
stress realizations gives 48/48 completions. The particular inner systems do not encounter in isolation over the
test interval.
The coherent advantage remains in aggregate at half
the timestep: 39/48 coherent and 15/48 circular completions. However, 12 of 96 matched endpoint labels differ
between resolutions. The totals must not be interpreted

## Page 4

Figure 1: Primary controlled experiment. The stress cohort was selected for large circular-start secular intersection diagnostics;
the comparison cohort was randomly selected from the remaining pool. Two mean-anomaly realizations per architecture are
matched across states. These completion fractions describe selected finite-time integrations, not population occurrence or long-term survival probabilities.
as exact probabilities. Independent IAS15 and finer WHFast runs agree on the selected cases 24 and 1332, where
circular starts encounter and prepared starts complete
20,000 yr. Case 916 is a failure example: both states
encounter with both validation methods, including some
configurations that completed at the coarser resolution.

4.2 Continuous mode loading

Case 24 has inner semimajor axes of 0.2000, 0.300735,
and 0.452207 au. The corresponding masses are 1.0104,
8.0459, and 11.6860 M⊕. Its 6.3436 MJ giant lies at
1.626068 au. At the sampled eg = 0.409649, qg/ai,out ≃
2.12.
Holding the masses and axes fixed, we scan seven giant eccentricities from 0.15 to 0.45 and five loadings
η = 0, 0.25, 0.5, 0.75, 1, each with two matched phases.
The initial inner vectors are (1 − η)zcoh and the giant
vector is unchanged, so F = η
2
initially. All 42 realizations with η ≤ 0.5 complete. Circular states complete
through eg = 0.30 but encounter at each sampled value
from 0.35 to 0.45. At η = 0.75, both phases complete
through 0.35, one at 0.40, and neither at 0.45 (Fig. 2).
This is a resolved dependence on initial state in one architecture, not a calibrated universal eccentricity cutoff.

4.3 Persistence and delayed failure

Twelve integrations of cases 24 and 1332 use P1/80 and
a 106-yr horizon. Both coherent and both perturbed
case-24 realizations complete, while its circular starts encounter by 4,451 yr. For case 1332, one coherent realization completes and one encounters at 199,309 yr; the perturbed realizations encounter at 21,718 and 9,333 yr, and
both circular starts before 438 yr. Across the two selected
Figure 2: Case-24 loading scan. The prepared mode has η =
0, while circular inner orbits have η = 1. Each cell contains
only two phase realizations. Changing η changes mode content
and angular momentum deficit; it does not specify a formation
timescale.
architectures this gives 3/4 coherent, 2/4 perturbed, and
0/4 circular completions.
These extensions demonstrate that an advantage can
persist for one million years, while a 20,000-yr completion can conceal delayed failure. They do not yield a lifetime distribution or gigayear stability certificate. Linear
mode preparation does not remove nonlinear interactions,
resonances, or sensitivity to phase.

5 Generating coherent orbital

states
Prepared initial conditions establish a possible dynamical
advantage, but do not show whether formation populates

## Page 5

those states. We therefore begin the inner system circular
or nearly circular and evolve prescribed giant excitation,
damping removal, or giant instabilities. The disk calculations model orbital responses, not self-consistent planet
formation.

5.1 Linear excitation and gas removal

For each of the 48 selected architectures, we solve
z˙ = [iA + diag(−γi, . . . , −γi, +γg)] z, (9)
starting at zero inner eccentricity and eg = 0.001. Here
γg = 1/τg and γi = d/τg. We evaluate the matrix exponential and stop when the giant reaches the specified
architecture’s target eccentricity. Five values x = τg∆g =
0.01, 0.1, 1, 10, 100 and three damping ratios d = 0, 1, 10
give 720 histories. The inverse angular-frequency gap
1/∆g is not a full 2π secular period.
Without inner damping, median final F decreases from
0.99985 at x = 0.01 to 0.43766 at x = 1, 0.00835 at
x = 10, and 7.2×10−5 at x = 100. Slow forcing allows the
inner vectors to approach the evolving coherent response.
Strong damping changes that response: at x = 10, d = 10,
median F = 0.48458. Damping can hold the system away
from the gas-free mode, so immediate removal need not
leave low free eccentricity.
From all 48 endpoints at x = 10, d = 10, we switch
off giant pumping and set γi(t) = γi,0 exp(−t/τd). Six removal parameters y = τd∆g = 0, 0.01, 0.1, 1, 10, 100 give
288 further histories. We follow nonzero removal times
for 12τd. Median F is 0.48458 for instantaneous removal,
0.47833 at y = 0.1, 0.15345 at y = 1, and about 2×10−11
at y = 10. The last value reflects the ideal linear model
and finite residual damping at the stopping time; it is
not a physically meaningful ten-decimal-place coherence
prediction.
The mechanisms have close precedents in gradual excitation and apsidal capture [15], and in the response to
growth, damping, and scattering [16]. Hydrodynamic calculations permit giant eccentricity growth in some disk
cavities [22], motivating the sign of the prescribed forcing.
They do not calibrate our exponential rates or constant
damping ratios. The smallest x values are limiting experiments. Disk gravity, gap structure, mass growth, and
ordinary migration torques are absent.

5.2 Matched-target direct integrations

We test the selected case-24 architecture with full Newtonian integration between symmetric eccentricity kicks. A
baseline kick preserves the osculating semimajor axis, orientation, and mean anomaly, and multiplies eccentricity
by exp(γ∆t/2) on either side of the gravitational interval.
Coordinates are synchronized and marked as modified after each kick. Inner eccentricities start at zero and the
giant at 0.001. Primary integrations use P1/40 and 20-yr
kick intervals.
Eight fixed-duration pilot runs produced slightly different final giant eccentricities because short-period terms
matter at such small initial eg. We retain them as pilots.
The primary eight runs instead stop pumping at the same
target eg = 0.409649, then apply immediate or gradual
damping removal and follow 100,000 yr of gas-free evolution. Two mean-anomaly seeds are used per prescription.
The endpoint is the same close-approach diagnostic as in
the controlled experiment.
Slow pumping lasts approximately 35,500–36,200 yr.
In the gradual-removal case, τd = 6013 yr and damping decays for about 72,158 yr before the gas-free follow-up. The final giant eccentricity remains near 0.408–0.410.
Slow growth without inner damping gives F = 0.0217–
0.0226, whereas gradual damping removal gives 0.0118–
0.0153. Immediate removal with d = 10 leaves 0.369–

0.410. All six complete.

At the primary resolution, the two x = 1, d = 0
cases encounter approximately 38,200 and 92,600 yr after pumping stops. However, both complete on refinement to P1/80 and 5-yr kicks, with final F = 0.359 and

0.490. Their higher excitation is reproduced, but the

faster-growth survival disadvantage is not. Figure 4 retains this failed convergence check. Three refined slow
histories also complete and preserve the action contrast
(Table 2). Two seeds and one selected architecture cannot
yield a general survival probability.

5.3 Damping with associated orbital

drift
To test the fixed-semimajor-axis assumption, four further
primary histories let damping conserve specific orbital angular momentum:
a
′ = a
1 − e
2
1 − e
′2
. (10)
This prescription includes damping-associated inward
drift, but not the full torque-driven migration of a gas
disk. In one gradual-removal realization the inner axes
shrink by about 12%, 20%, and 29%. Both gradual-removal cases complete, with F = 0.0662–0.0930, while
one of two instantaneous-removal cases encounters.
Two refined drift runs retain that particular encounter/completion contrast for seed 101. However, the
gradual case changes from F = 0.0662 to 0.0216. The
action amplitude is not numerically converged, and this
small experiment does not establish a sharp gas-removal
threshold. It shows that low free action can arise without
inserting the final coherent state, while identifying orbital
drift as an important sensitivity.

6 Giant scattering

Giant scattering supplies a more self-consistent source
of excitation, although our initial architecture grids re-

## Page 6

Figure 3: Generation of low free-mode action in 1,008 reduced linear histories. Shading represents the 16th–84th percentile
across the 48 selected architectures, not uncertainty on a population mean. Left: giant eccentricity growth at different inner
damping strengths. Right: removal of damping from the x = 10, d = 10 endpoints. The very small linear values do not carry
over quantitatively to finite-eccentricity direct integrations.
Table 2: Matched-target growth histories in case 24. F is the median over the final 10,000 yr, sampled from osculating elements,
when a run completes. The refined fixed-axis tests use P1/80 and 5-yr kicks. The fast-growth survival contrast fails refinement;
no survival threshold is inferred.
Prescription Primary completions Primary final F Refinement result
x = 1, d = 0, fixed axes 0/2 Encounter
endpoints
Both complete; F = 0.359, 0.490
x = 10, d = 0, fixed axes 2/2 0.0217–0.0226 One checked: 0.0218, complete
x = 10, d = 10, instant removal, fixed
axes
2/2 0.369–0.410 One checked: 0.386, complete
x = 10, d = 10, y = 10, fixed axes 2/2 0.0118–0.0153 One checked: 0.0148, complete
x = 10, d = 10, instant removal, orbital
drift
1/2 Survivor: 0.285 Encounter realization still encounters
x = 10, d = 10, y = 10, orbital drift 2/2 0.0662–0.0930 One checked: 0.0216, complete
main deliberately small. We retain the three case-24 inner planets at initial e = 0.001 and initialize outer giants
at e = 0.01, inclination 0.5
◦
, with randomized orientations and anomalies. Histories are integrated for up to
100,000 yr. An inner encounter terminates a run; it is
not followed to physical destruction.

6.1 Two-giant instabilities

The two-giant grid uses masses (3, 1),(1, 3),(3, 3) MJ, the
innermost giant at 3 au, and separation 2.5 mutual Hill
radii. Four seeds give 12 primary histories with MERCURIUS [23] at P1/40. Giant collisions merge perfectly
inelastically, taking each initial radius as one Jupiter radius. Unbound bodies are removed only beyond 100 au,
and energy changes from mergers and removals are accounted for explicitly. The artificial inner collision radii
implement the encounter diagnostic, not physical planet
radii.
Ten histories reach the horizon after a giant merger
with the inner system retained, one ejects a giant and
retains the inner system, and one reaches an inner encounter. The merger remnants have eg ≃ 0.004–0.035
and qg/ai,out ≃ 6.9–8.1. Their coexistence is largely explained by weak forcing; it does not require special alignment or low normalized F. Near-zero giant eccentricity
can make that normalization particularly misleading.
The ejection survivor has eg ≃ 0.232, qg/ai,out ≃ 4.62,
and F ≃ 0.129. A twice-finer realization also ejects a
giant and retains the inner system but gives F ≃ 0.562.
The individual low-action amplitude is therefore not a
converged prediction. Three refined two-giant runs all
complete; the original encounter, which had an elevated
energy residual, becomes a merger survivor. We do not
count that coarse encounter as a verified physical failure.

6.2 Three giants: numerical sensitivity

The three-giant grid begins at 2 au, has 3.5 mutual-Hill-radius adjacent spacing, and uses equal masses of either

## Page 7

Figure 4: Generated histories in the selected compact architecture. Time zero marks the end of giant pumping. All histories
begin with circular inner orbits. The cross marks the primary faster-growth encounter; the refined faster-growth trajectory
completes. Green and purple curves have gradual damping removal; purple includes damping-associated orbital drift and has a
resolution-sensitive final action. These differences constrain interpretation of the reduced disk model.
1 or 3 MJ. Eight MERCURIUS runs yield seven inner encounter endpoints and one surviving three-giant system.
Eight reruns with TRACE [24], twice-finer timesteps, and
adaptive stellar-pericenter handling reproduce the endpoint count but not the encounter times. Two TRACE
encounters retain elevated energy residuals.
Independent IAS15 checks of those two realizations give
one encounter at 17,960 yr with relative energy residual
2.3 × 10−10, and one completion of its shorter 30,000-
yr check horizon with residual 5.3 × 10−15. Thus the
seven-of-eight encounter count is not a converged physical
fraction. The two- and three-giant grids also differ in
initial radii, spacing, and masses, so their contrast cannot
be attributed to planet number alone.
Scattering can leave weakly perturbed coexistence systems, produce relatively coherent survivors, or damage
the inner system, consistent with history-dependent theory [12, 16]. We do not infer the frequencies of these
channels. Planar free-mode diagnostics are omitted for
contact-censored pilots and unsuitable highly inclined or
multiple-remnant endpoints. In a chaotic problem, agreement of one trajectory is not a substitute for statistical
convergence of a much larger ensemble.

7 Public survey tests

7.1 Fixed sample and injection recovery

data
We freeze the California Legacy Survey (CLS) public
repository [25, 26] at commit 689d491 (full hash in Appendix B). The planet table includes 164 known planets
and 14 newly catalogued candidates under status codes
K and C; both are retained. The primary cuts are inner minimum masses 2–30 M⊕ at 0.03–1 au and giant
minimum masses 0.3–13 MJ at 1–10 au. This survey definition differs deliberately from the catalog’s contextual
union definition. Membership is determined from tabulated medians, without treating marginal uncertainty as
independent posterior draws.
The selection gives 39 small planets, 68 giants around
58 giant hosts, and four coexistence hosts: HD 11964
A, HD 164922, HD 190360, and HD 219134. For a phase
comparison we pair the outermost qualifying small planet
with the innermost qualifying giant once per host. The
cuts and one-pair-per-host rule were recorded before inspecting these conditional results; subsequent sensitivity analyses are exploratory, not externally preregistered

## Page 8

tests.
We retain all 58 per-star recovery files, totaling 58,000
injection tests, with pinned URLs, retrieval times, and
hashes. The public snapshot supplies 1000 tests per star,
compared with 3000 described in CLS I. The period floor
is about two days. A secondary completeness benchmark therefore uses 0.04–1 au with the same mass interval, avoiding extrapolation below injection support. This
common domain contains 6,432 injections and eight detected small planets in the same four hosts. The original
primary cuts are unchanged.
The frozen repository provides marginal orbital summaries and author-side paths to chains, but does not supply the joint posterior chains for the four systems. We
do not synthesize pseudo-posteriors from independently
sampled marginal intervals. Unknown inclinations, node
angles, and masses remain relevant to a three-dimensional
dynamical interpretation.

7.2 Precision of eccentricity vectors

For the selected small planets, the quoted marginal 68%
argument-of-periastron widths are approximately 122◦,
97◦, 22◦, and 80◦; for their giants they are 44◦, 144◦, 3
◦
,
and 127◦. Only HD 190360 has both arguments tightly
constrained. These RV arguments do not give mutual
three-dimensional apsidal directions without inclinations
and nodes. Circular-orbit angle degeneracy, wrapping,
and posterior correlations preclude a valid alignment significance from four marginal point pairs.
We instead calculate a feasibility forecast: the inner
eccentricity expected if the giant-dominated linear mode
were occupied. This uses all qualifying planets in each
host, minimum masses, the tabulated stellar mass, coplanarity, and leading relativistic precession 3GM∗n/(c
2a).
The leading small-eccentricity RV harmonic is Kiei,coh,
where Kiis the tabulated semiamplitude. These are
model predictions at point estimates, not inferred mode
occupations.
The predicted harmonics span approximately 10−4–2×
10−2 m s−1(Table 3). Even an ideal uniformly sampled
sinusoidal fit with independent errors σRV = 1 m s−1
would require
N3σ ≃
18σ
2
RV
(Kiei,coh)
2
, (11)
from σA ≃
√
2/N σRV. The resulting range is 4.4 × 104–
1.8 × 109 measurements. Correlated noise and uncertain
orbital parameters make this estimate optimistic. It identifies a poor coherence-test sample, not a practical observing proposal.
HD 190360’s measured inner eccentricity is much larger
than the pure giant-mode forecast. This argues against
that particular mode occupation at the point estimates,
but not against coherence being protective in a closely
perturbed compact system. Its wide giant pericenter does
not require the protection being tested in case 24.
Among 1,314 recovered common-domain injections
across all giant hosts, mean cos(ωinj − ωg) = 0.0055
and half are within 90◦ of the giant argument. Among
229 recovered injections in the four coexistence hosts,
the aligned fraction is 0.441. The files do not reveal a
strong universal alignment preference in discovery recovery. They do not measure the distinct selection for an
informative eccentricity vector, so this audit cannot calibrate a phase test.

7.3 Conditional completeness

For a transparent secondary calculation, we assume uniform planet density in log a and log m over the common
domain. We estimate per-star recovery probability with
a Gaussian kernel in those coordinates, using reference
bandwidth 0.25 dex and a fixed 33×29 grid. Bandwidths
of 0.15 and 0.4 dex and direct in-domain recovery fractions are retained as sensitivity checks. The injection eccentricities follow the survey prescription. We condition
throughout on stars with detected qualifying giants.
We divide the 58 hosts at the median present tidal
proxy
Tg =
∑
g
mg
a
3
g
(1 − e
2
g
)
3/2
, (12)
which is 0.100924 MJ au−3. This proxy is not a substitute for the full differential secular forcing. All four coexistence hosts, including all eight common-domain small
planets, lie in the lower half. Summed mean completeness gives effective exposures of 7.864 and 5.600 stars in
the lower and higher halves, respectively, each containing
29 actual stars.
The formal count/exposure estimates are 1.017 and 0
planets per detected-giant host, or 0.594 overall. The
total varies from 0.554 to 0.670 across completeness estimators. These are planet-count benchmarks under an
assumed distribution, not fractions of hosts containing
planets. Zero detections also do not imply a zero upper
uncertainty bound. Treating the eight planets as eight independent formation outcomes would overstate evidence
because they occupy only four hosts.
An illustrative Bernoulli host model with assumed
multiplicity from one to four planets per occupied host
gives conditional probabilities of 0.088–0.106 that all four
detected hosts lie in the lower half. These are plug-in, model-dependent tail calculations, not calibrated discovery p-values; host-fraction uncertainty and realistic
within-system correlations are omitted. Median metallicities of the two halves are 0.192 and 0.160 dex. Four coexistence hosts cannot support a controlled analysis of metallicity, giant detection, architecture, and small-planet sensitivity.
The pattern is compatible with reduced forcing favoring coexistence, but does not establish a new empirical
relation. Giant mass and separation effects have already
been examined in CLS [3, 5]; stable-zone proxies also appear in the recent homogeneous GAPS analysis [9]. The

## Page 9

Table 3: The four selected CLS coexistence hosts. Separation uses the paired giant and outermost selected small planet.
Coherent amplitudes include leading relativistic precession. The last column is the modeled harmonic, not the harmonic implied
by the measured eccentricity.
Host qg/ai,out Median measured ei Modeled ei,coh Ki (m s−1) Kiei,coh (m s−1)
HD 11964 A 12.36 0.106 0.004760 4.260 0.02028
HD 164922 5.89 0.096 0.000931 2.307 0.002147
HD 190360 20.56 0.165 0.001932 5.446 0.01052
HD 219134 12.34 0.077 0.000029 3.432 0.000101
public data chiefly identify where a test of orbital coherence lacks precision and dynamical relevance.

8 Conditions for coexistence

8.1 Three physical requirements

The combined evidence supports three conditional requirements. First, the formation history must supply and
assemble the inner planets. The timing of giant growth
relative to inner growth, material transport, and disk evolution matters [1]. Our simulations begin after planetary
masses have been assigned, so this remains a literature-based prerequisite rather than a result of the integrations.
Second, the architecture and evolving perturbations
must avoid destructive differential excitation. A sufficiently distant or low-eccentricity giant can leave the inner system weakly forced. A tightly coupled inner system
or rapid additional apsidal precession can reduce its response. Secular resonances, close encounters, inclined perturbations, and other companions can undermine those
protections. The large pericenter ratios in most catalog
examples and the low-eccentricity scattering merger remnants illustrate coexistence without requiring a special
apsidal state.
Third, where the giant’s forcing is stronger, the inner
eccentricity vectors can materially change the finite-time
outcome. Small free components relative to an appropriate coherent mode can reduce relative orbital excursions.
The matched circular/coherent/shuffled experiments isolate this effect, and selected long extensions show persistence beyond the main horizon. However, coherent preparation is neither necessary in weakly forced systems nor
sufficient for indefinite survival. The operative requirement is avoiding damaging relative motion, not minimizing each planet’s scalar eccentricity.

8.2 History and a testable prediction

The reduced disk calculations show that initially circular inner planets can reach low free action through sufficiently slow giant excitation or gradual removal of damping. Strong damping alone need not prepare the gas-free
mode. Scattering can also leave benign remnants, but the
final giant orbit does not uniquely encode what the inner
system experienced.
A candidate observational prediction is therefore conditional: at fixed, compact, approximately coplanar architecture, systems near a strong differential-forcing boundary
should preferentially retain small free eccentricity vectors;
this preference should weaken in widely separated, weakly
forced systems. The predicted quantity includes amplitudes and orientations together. Alignment alone does
not identify gradual growth: in the single-frequency impulsive limit, zi/zforced = 1 − exp(i∆gt) has nonnegative
real part despite substantial free eccentricity [16].
In the fixed-axis case-24 histories, gradual versus immediate damping removal reduces final F by roughly a factor
of 25–35. That factor is not a population prediction: the
orbital-drift experiment is quantitatively sensitive, physical disk-induced precession is absent, and only one architecture has direct growth histories. A credible quantitative test would need a broad physical disk ensemble and
an observational likelihood for full eccentricity vectors,
including their measurement selection. The present CLS
sample supplies neither a strongly forced comparison set
nor sufficiently informative vectors.
The contribution of this work is the explicit controlled
comparison, the connected history tests, and the reproducible survey-feasibility audit. Slow-excitation coherence, forced-eccentricity protection, and scattering-history dependence already have direct precedents [15, 10,
12, 13, 16]. We do not claim a new secular mechanism or
an independently established novel population law.

8.3 Numerical and physical scope

The direct disk integrations omit disk gravity, full migration torques, planet mass growth, inclination evolution, stellar oblateness, tides, and relativistic terms. The
observed-system mode forecasts include leading relativity but remain linear, coplanar, and based on minimum
masses. In case 24, relativistic contributions are below
0.6% of the corresponding Newtonian diagonal rates; even
a small frequency shift can matter near a resonance, so
this comparison does not establish relativistic robustness.
The stress selection, two phase seeds per architecture,
single direct-growth architecture, small scattering grids,
and finite integration horizons prevent population inference. Coarse-to-fine endpoint changes are retained. In
particular, the faster-growth encounter contrast disappears entirely on refinement, and one low-action scattering realization does not preserve its amplitude. No sim-

## Page 10

Figure 5: Public-survey feasibility. Left: common-domain recovery probability versus present tidal proxy. The dotted line is
the median split; blue symbols identify the four detected coexistence hosts. Right: measured marginal inner eccentricities with
68% intervals and model coherent amplitudes. These comparatively wide systems need not occupy a pure giant mode to coexist.
The figure is a selection and measurement audit, not a posterior test of mode occupation.
ulation here establishes gigayear stability or the physical
destruction of a planet at our encounter endpoint.

9 Conclusions

Outer giants can coexist with inner small planets when
their formation histories produce both populations and
subsequent evolution leaves sufficiently little damaging
differential excitation in the inner system. Weak external forcing, strong internal coupling or additional precession, and coherent eccentricity vectors are complementary
ways to satisfy the dynamical part of this condition.
Our controlled integrations demonstrate that orbital
state can change finite-time encounter outcomes at fixed
giant mass, semimajor axis, and eccentricity. Reduced
growth and damping-removal models can generate low
free action from circular starts, but a general survival
boundary has not been established. Scattering admits
both weakly forced survivors and damaging histories.
The selected public survey systems mainly test weak forcing and have insufficiently informative eccentricity vectors to distinguish the proposed coherence mechanism.
The evidence therefore favors a conditional answer involving architecture, orbital state, and excitation history.
It does not justify a universal giant-property threshold,
compulsory apsidal alignment, a uniquely identified formation channel, or a new occurrence law.
Data and code availability
The retained research products include public catalog
and survey snapshots, queries, pinned source URLs and
hashes, architecture definitions, random seeds, direct-run outcomes and sampled histories, numerical checks,
and figure scripts. The two accompanying research
archives preserve the baseline and history/survey analyses separately. The typesetting source for this combined
manuscript includes the figures and can be compiled independently; it does not replace the full numerical archives.
No public repository DOI or preprint identifier has yet
been assigned.
Authorship and preparation
Author names and affiliations are placeholders. This
manuscript was assembled with AI-assisted literature synthesis, code generation, numerical analysis, and writing.
Scientific responsibility, authorship, and independent expert review remain to be established before submission.
No preprint submission or peer-review acceptance is implied.
A Validation and run inventory
Independent quadrature checks the Laplace coefficients to
maximum relative discrepancy 2.0 × 10−13 in the tested
cases. Independent complex-ODE integration agrees with
the mode solution to 2.7 × 10−13 in absolute eccentricity.
The quadratic secular angular momentum deficit is conserved to relative 1.4 × 10−15, and the conic-intersection
formula agrees with direct polar sampling for 1000 random ellipse pairs. Increasing secular screen sampling from
4,096 to 16,384 epochs changes three pilot maxima by at
most 0.015%.
For the growth problem, eigendecomposition agrees
with an adaptive ODE solution to 1.3 × 10−11 and a sep-

## Page 11

Table 4: Inventory of distinct jobs. Numerical checks revisit initial conditions; an executed job may end at an encounter. The
two sides list different experiment families, not matched pairs.
Controlled-state experiments Jobs
Development pilots 6
Four-state primary comparison 384
Selected IAS15/finer WHFast checks 24
Additional full-cohort refinement 84
Loading/eccentricity scan 70
One-million-year extensions 12
No-giant controls 48
Controlled-state subtotal 628
Reduced linear histories
Eccentricity growth 720
Damping removal 288
Linear-history total 1008
Generated-history experiments Jobs
Fixed-duration growth pilots 8
Matched-target growth 8
Slow-growth refinement 3
Faster-growth refinement 2
Damping-associated drift 4
Drift refinement 2
Contact-censored scattering pilots 6
Two-giant merger/ejection histories 12
Two-giant refinement 3
Three-giant histories 8
Three-giant TRACE checks 8
Three-giant IAS15 checks 2
History subtotal 66
Total distinct direct integration jobs: 628 + 66 = 694.
arate matrix-exponential calculation to 1.6 × 10−14. The
F = η
2
identity and the damping angular-momentum
identity are verified. A one-orbit kick test agrees with analytic exponential eccentricity change and a synchronized
implementation to better than 10−10.
Among completed primary controlled integrations, the
largest sampled relative energy error is 9.4 × 10−8. Regular prepared case-24 IAS15 runs have errors below 6 ×
10−15. Successful primary growth histories have residual
gravitational energy errors of order 10−11 after subtracting applied work. Energy diagnostics check numerical
implementation; they neither validate the disk model nor
bound errors between sampled outputs near a close encounter.
Table 4 counts distinct jobs. The 96-run stress-cohort
refinement combines 84 additional runs with 12 finer WHFast runs already in the selected 24-run validation set.
They must not be counted twice. Six baseline pilots
and six contact-censored scattering pilots remain in the
archives. Contact-endpoint action estimates are excluded
from the physical conclusions. The two IAS15 scattering checks stop at 30,000 yr unless an encounter occurs,
rather than the 100,000-yr main scattering horizon.
B Survey provenance
The full frozen CLS repository revision is
689d49178f8cab5a0c8d5291035786423c530953.
The retained planet and stellar tables, observing summaries, 58 recovery files, and manifests make the selection auditable. Mass and axis columns are interpreted
in Jupiter masses and au before conversion. Published
lower/upper quantile columns are quantile values, not
symmetric errors. Missing observing metadata for one selected host is retained as missing rather than filled with
zero or used to drop that star.
The primary observational hypothesis concerned apsidal alignment among eccentric small planets and eccentric
giants. The full-vector formulation arose during interpretation of the history experiments. The fixed analysis plan
and follow-up decision log distinguish these stages. No external preregistration or independent validation sample is
claimed.
The illustrative host-level calculation conditions on exactly four detected coexistence hosts and assumes identical multiplicity per occupied host. It is only a sensitivity
check on the effect of counting planets instead of systems.
A selection-aware population analysis would additionally
need a latent multiplicity distribution, joint orbital posteriors, uncertainty in completeness and host occupation,
giant detection selection, and stellar covariates. Those
quantities cannot be identified from four detected hosts
in this restricted sample.
Analysis scripts were replayed from the retained research archives without rerunning the direct integrations.
Numerical summaries and scientific figures reproduced,
with only negligible floating-point serialization differences
in two extension tables. The new combined manuscript
reorganizes those retained results; it adds no new dynamical integrations or independent observations.

References

[1] Danti, Lambrechts, and Lorek (2025). Super-Earth
formation in systems with cold giants.
https://arxiv.org/abs/2506.17091.
[2] Zhu and Wu (2018). The Super Earth-Cold Jupiter
Relations. https://arxiv.org/abs/1805.02660.
[3] Rosenthal, L. J., et al. (2022). The California Legacy
Survey III. On The Shoulders of (Some) Giants.
https://arxiv.org/abs/2112.03399.

## Page 12

[4] Van Zandt et al. (2025). The TESS-Keck Survey XXIV:
Outer Giants may be More Prevalent in the Presence of
Inner Small Planets.
https://arxiv.org/abs/2501.06342.
[5] Lefevre-Forjan and Mulders (2025). Saturns, but not
super-Jupiters, occur more frequently in the presence of
inner super-Earths.
https://arxiv.org/abs/2506.21204.
[6] Van Zandt and Petigura (2024). No evidence for a
metallicity-dependent enhancement of distant giant
companions to close-in small planets in the California
Legacy Survey. https://arxiv.org/abs/2410.23071.
[7] Chen et al. (2026). Sub-Neptunes Show a Stronger
Correlation with Cold Jupiters than Super-Earths
Especially in Metal-rich Systems.
https://arxiv.org/abs/2604.20203.
[8] Liu, Zhu, Gan, and Dai (2026). TESS planets in known
radial velocity cold Jupiter systems: Hot super Earth
occurrence is enhanced by cold Jupiters.
https://arxiv.org/abs/2602.11017.
[9] Ruggieri, A., et al. (2026). The GAPS Programme with
HARPS-N at TNG LXXVII. Occurrence rates of small
close-in planets in the presence of cold Jupiters.
https://arxiv.org/abs/2607.09320.
[10] Pu, B. and Lai, D. (2018; corrected version 2021).
Eccentricities and Inclinations of Multi-Planet Systems
with External Perturbers.
https://arxiv.org/abs/1801.06220.
[11] Xuan and Wyatt (2020). Evidence for a high mutual
inclination between the cold Jupiter and transiting
super Earth orbiting pi Men.
https://arxiv.org/abs/2007.01871.
[12] Pu, B. and Lai, D. (2021). Strong Scatterings of Cold
Jupiters and their Influence on Inner Low-mass Planet
Systems: Theory and Simulations.
https://arxiv.org/abs/2008.05698.
[13] Quarles, B. and Lissauer, J. J. (2018). Long-term
Stability of Tightly Packed Multi-planet Systems in
Prograde, Coplanar, Circumstellar Orbits within the
Alpha Centauri AB System.
https://arxiv.org/abs/1801.06131.
[14] Gratia and Lissauer (2020). Eccentricities and the
Stability of Closely-Spaced Five-Planet Systems.
https://arxiv.org/abs/1908.01117.
[15] Chiang, E. I. and Murray, N. (2002). Eccentricity
Excitation and Apsidal Resonance Capture in the
Planetary System Upsilon Andromedae. ApJ 576, 473.
https://arxiv.org/abs/astro-ph/0205273.
[16] Rodet, L. and Lai, D. (2022). Eccentric debris belts
reveal the dynamical history of the companion
exoplanet. MNRAS 516, 5544.
https://doi.org/10.1093/mnras/stac2621.
[17] Tamayo, Murray, Tremaine, and Winn (2021). A
Criterion for the Onset of Chaos in Compact, Eccentric
Multiplanet Systems.
https://arxiv.org/abs/2106.14863.
[18] Laskar and Petit (2017). AMD-stability and the
classification of planetary systems.
https://arxiv.org/abs/1703.07125.
[19] NASA Exoplanet Archive (2026). Planetary Systems
table and TAP access documentation.
https://exoplanetarchive.ipac.caltech.edu/docs/
TAP/usingTAP.html.
[20] Rein, H. and Tamayo, D. (2015). WHFast: a fast and
unbiased implementation of a symplectic
Wisdom–Holman integrator.
https://arxiv.org/abs/1506.01084. REBOUND
software: https://github.com/hannorein/rebound.
[21] Rein, H. and Spiegel, D. S. (2015). IAS15: a fast,
adaptive, high-order integrator for gravitational
dynamics. https://arxiv.org/abs/1409.4779.
[22] Romanova, M. M., et al. (2023). Eccentricity Growth of
Massive Planets inside Cavities of Protoplanetary Discs.
https://arxiv.org/abs/2303.17784.
[23] Rein, H., et al. (2019). Hybrid Symplectic Integrators
for Planetary Dynamics.
https://arxiv.org/abs/1903.04972.
[24] Lu, T., Hernandez, D. M., and Rein, H. (2024).
TRACE: a code for Time-Reversible Astrophysical
Close Encounters.
https://arxiv.org/abs/2405.03800.
[25] Rosenthal, L. J., et al. (2021). The California Legacy
Survey I. A Catalog of 178 Planets from Precision
Radial Velocity Monitoring of 719 Nearby Stars over
Three Decades. https://arxiv.org/abs/2105.11583.
[26] Rosenthal, L. J. CLSI public data repository, frozen
commit listed in the text.
https://github.com/leerosenthalj/CLSI/.
