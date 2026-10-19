## Page 1

From Planetary Chemistry to the Prevalence of Life
A Probabilistic Drake Framework
[Author name(s)]
[Affiliation(s)]
Revised working draft — October 2026

Abstract

The biological factors of the Drake equation describe outcomes without specifying the processes
that produce them. We develop a probabilistic framework in which those factors arise from
transition rates, finite periods of opportunity, and variation among planets. For a single transition,
the probability of completion is 1 − exp(−H), where H is the cumulative hazard. Under a specified
model of candidate generation, H is the product of the number of opportunities and the probability
that an opportunity establishes the required function. Sequential transitions are described by
conditional waiting times rather than products of marginal probabilities; a common replication
clock recovers the hard-steps approximation in its rare-event limit. Population averaging connects
these transition models to expected counts, while an explicit observation model separates the
presence of life from its detection. An illustrative RNA-replicase calibration places substantial
prior weight on widespread abiogenesis and is considerably narrower than a diffuse prior on the
transition rate. The adopted scenario gives a 0.77 prior probability that at least 10% of candidate
worlds become inhabited. This is conditional on the chemical route, its establishment requirements,
and the assumed planetary environments, rather than an empirical estimate of the probability
that Earth is alone. The framework identifies the measurements needed to improve that estimate:
functional frequencies under realistic chemistry, the production and turnover of candidate systems,
the probability of sustained replication, and calibrated biosignature surveys. Its contribution is a
mechanistic connection between chemistry, evolutionary opportunity, and observable populations,
not a choice of logarithmic units.

1 Introduction

The Drake equation’s enduring contribution is its decomposition of a difficult question. It separates
the abundance of suitable astronomical environments from the biological transitions and observable
lifetimes needed to produce detectable civilisations (Drake, 1965). Exoplanet surveys increasingly
constrain the astronomical component, although a planet’s radius and incident flux do not by themselves
establish surface habitability. The biological factors remain much less constrained. Their uncertainty
can dominate predictions even when the astronomical inputs are reasonably well characterised (Bryson
et al., 2021; Sandberg et al., 2018).
A useful next step is therefore not to replace fractions with different units, but to explain where
the fractions come from. The probability that a transition occurs depends on both the opportunities
available and the chance that any one opportunity succeeds. A chemically difficult event can be common
on planets that generate sufficiently many relevant candidates. Conversely, even an accessible function
may never arise where its feedstocks, environmental conditions, or opportunities for establishment are
absent. Subsequent evolutionary innovations introduce an additional constraint: opportunities for a
later transition generally begin only after its predecessors have occurred.

## Page 2

A probabilistic Drake framework
We retain the idea that biological factors can be connected to searches through configurations, but
use it as a modelling hypothesis rather than a universal description of evolution. A search model is
useful when candidates, a sampling process, and a success criterion can be specified. It is less useful
when those quantities conceal adaptive dynamics, long-lived correlations, or environmental changes
that need to be modelled directly. The more general object is a transition hazard: the instantaneous
rate of successful transition, conditional on its not yet having occurred.
This formulation links four parts of the problem. Laboratory experiments constrain functions and
candidate-generation processes. Geochemistry and ecology constrain how opportunities accumulate.
Waiting-time models describe ordered transitions. Population and observation models translate
completed transitions into inhabited worlds and detectable signatures. The resulting framework
preserves the Drake equation’s decomposition while exposing the assumptions needed to turn it into
an inference problem.

2 A probabilistic framework

2.1 From candidate generation to a transition probability

Let w describe a world’s relevant physical conditions and let θ contain parameters shared across
worlds. For transition k, let Ωk be a space of candidate configurations, Fk ⊆ Ωk the set satisfying a
specified functional and establishment criterion, and qk the distribution generating candidates. The
per-opportunity success probability is
pk(w, θ) = qk(Fk | w, θ). (1)
The criterion must match the event of interest. Producing a molecule with catalytic activity is not
automatically the same event as establishing a self-maintaining hereditary system.
For Ak independent, identically distributed opportunities, the probability of at least one success
is exactly 1 − (1 − pk)
Ak . If opportunities instead arrive as a Poisson process with rate ak(t) and
are independently successful with probability pk(t), the successful-event rate is hk(t) = ak(t)pk(t).
More generally, a model may specify hk directly. If the transition becomes available at time s, its
cumulative hazard and completion probability are
Hk(s, t | w, θ) = Z t
s
hk(u | s, w, θ) du, Pk(s, t | w, θ) = 1 − e
−Hk(s,t|w,θ)
. (2)
Here the hazard is conditional on no intervening completion. The displayed notation assumes that
conditioning on the preceding transition time and the specified world state suffices; additional relevant
history must otherwise be retained.
For stationary independent opportunities, Hk ≃ Akpk. This is a rare-per-trial approximation for a
fixed number of Bernoulli trials and an exact expression when the number of opportunities is Poisson
with mean Ak. If the event permanently changes the system, Hk remains an integrated hazard;
interpreting it as the number of realised transitions after the first event would be inappropriate.
Correlation cannot generally be repaired by counting each distinct sequence once. Repeated
independent draws are valid opportunities, whereas correlated draws can have a different first-success
distribution. A proposed effective trial count must be justified by the stochastic process or calibrated
against its waiting-time distribution. Likewise, an uncertain random hazard must be averaged as
E[1 − e
−H], not replaced by 1 − e−E[H]
.
Functional information can still serve as an auxiliary statistic. Under a specified sampling distribution, − log pk measures the rarity of the functional set; under uniform sampling it reduces to the

## Page 3

A probabilistic Drake framework
10
5 104 10
3 102 10
1 10
0 10
1 10
2
Cumulative hazard H
0.0
0.2
0.4
0.6
0.8
1.0
Probability of at least one transition
Transition probability
Rare-event / saturation approximation
Figure 1: The transition probability as a function of cumulative hazard. The approximation min(1, H)
captures the rare-event and saturation limits but is not used for the numerical population averages
reported here. The horizontal axis describes an integrated transition rate, not an information budget.
familiar sequence-space definition (Hazen et al., 2007). The probability and its generating distribution
are primary. Changing the logarithm’s base does not change any prediction, and a rarity estimate
under a laboratory distribution is not automatically valid under prebiotic synthesis.

2.2 Rare events and saturation

Equation (2) has two useful limits:
1 − e
−H ≃
(
H, H ≪ 1,
1, H ≫ 1.
(3)
A transition is unlikely when little cumulative opportunity has accumulated and nearly certain
when the integrated success rate is large. Completion probabilities of 0.01 and 0.99 correspond to
H = 0.01005 and H = 4.605, respectively: a factor of approximately 458 in cumulative hazard, or
2.66 orders of magnitude. This is a relatively narrow crossover when plausible hazards span many
orders of magnitude, but it is not a physical discontinuity (Figure 1).
The useful logarithmic approximation is − log(1 − e
−H) ≃ [− log H]+, with a uniform error bound
given in Appendix A.1. It is a numerical convenience, not an additional law. In particular, the
crossover does not imply that intermediate population prevalences require fine-tuning. Mixtures
of very favourable and very unfavourable worlds can produce any intermediate fraction, and the
conclusion also depends on the prior distribution of hazards.

2.3 Sequential transitions

Let Tk be the completion time of the kth required transition, with T0 = 0, and let gk(t | w, θ) be its
density. For a serial model in which the previous completion time and the specified state contain the
relevant history,
gk(t | w, θ) = Z t
0
gk−1(s | w, θ)hk(t | s, w, θ)e
−Hk(s,t|w,θ) ds, g0(s) = δ(s). (4)

## Page 4

A probabilistic Drake framework
The probability of reaching state X by age T is the integral of the final-stage density up to T. Rates
can be set to zero outside the relevant environmental windows. Competing pathways, reversals, or
extinctions require a larger state model rather than an extra scalar correction.
A product of full-window probabilities generally gives each transition more time than it actually
has. Even two transitions with the same constant rate h illustrate the distinction: their sequential
completion probability is 1 − e
−hT (1 + hT), not (1 − e−hT )
2
. Dividing the latter by two repairs only
its leading rare-event term; it fails when both transitions become easy. The factorial hard-steps
factor is therefore derived only under its own assumptions in Section 3.5, not appended to the general
equation.

2.4 From worlds to expected populations

Let ZX denote the random number of worlds reaching state X, and let µX = E[ZX] denote its
expectation. Conditional on θ, a population of nhab candidate worlds with characteristics drawn from
π(w | θ) has
µ
ever
X (T | θ) = nhab Z
PX(T | w, θ)π(w | θ) dw. (5)
The reference time and eligible population must be specified. A present-day stellar census is not itself
a count of all habitable opportunities over Galactic history.
For a time-dependent formation history, let b(tb, w | θ) dtb dw be the expected number of candidate
worlds born in the corresponding interval. The expected number currently in state X is
µ
now
X (t0 | θ) = Z t0
0
Z
b(tb, w | θ)P{X is occupied at age t0 − tb | w, θ} dw dtb. (6)
The occupancy probability includes the time to reach X and the duration or survival of that state.
Under stationary formation over a sufficiently long history, this reduces to the Drake-like expression
µ
now
X = Rhab Ew
h
P
reach
X (w) ℓX(w)
i
, (7)
where ℓX(w) is the mean total time spent in X conditional on reaching it. Replacing this expectation
by a product of separate means additionally requires an independence assumption. Detectability
belongs in an observation model unless X has explicitly been defined as a detectable state.

2.5 Planetary variation and uncertainty

Physical variation among planets and uncertainty about shared parameters are different levels of the
model. At fixed θ, the inhabited fraction for a single origin transition is
flife(θ) = Ew[1 − e
−H0(w,θ)
]. (8)
A prior or posterior over θ then induces uncertainty about this fraction. Averaging over w is not a
substitute for learning θ, and uncertainty shared by all planets does not disappear in a large Galaxy.
For illustration, suppose log H0 ∼ N (m, s2) across worlds. In the deep rare-event limit at fixed s,
flife ≃ E[H0] = e
m+s
2/2
. Relative to a homogeneous population with hazard equal to the median e
m,
dispersion increases the mean hazard and can substantially increase the inhabited fraction. However,
since 1 − e
−H is concave,
E[1 − e
−H] ≤ 1 − e−E[H]
. (9)

## Page 5

A probabilistic Drake framework
Table 1: Astronomical assumptions used solely for the reference-population calculation. U denotes
a uniform distribution; LogUnif is uniform in the logarithm. The normal distributions for log η use
natural logarithms and variances as their second parameter.
Quantity Adopted scenario
Galactic stars LogUnif(1011, 3 × 1011)
Observable-universe stars LogUnif(1022, 5 × 1022)
G, K, M shares 0.06, 0.12, 0.79; other classes omitted
GK occurrence log ηGK ∼ N (log 0.30, 0.6
2
)
M occurrence log ηM ∼ N (log 0.15, 0.8
2
)
Atmosphere-retention fractions fatm,GK ∼ U(0.3, 1); fatm,M ∼ LogUnif(10−3, 0.3)
The population-scale assumptions draw on Bryson et al. (2021); Reylé et al. (2021); Licquia and Newman (2015); Frank
and Sullivan (2016). The atmospheric distributions are additional scenario assumptions, not results inferred from these
references. Distributions are independent here except where a parameter is explicitly shared. A formation-history
calculation is needed for a count over all past opportunities.
At fixed arithmetic mean hazard, heterogeneity cannot increase the average success probability above
the homogeneous case. There is no universal diversity bonus independent of the comparison being
made.
Successful worlds are sampled according to π(w | life, θ) ∝ Plife(w, θ)π(w | θ). They are consequently
biased toward favourable conditions. An unusually productive prebiotic Earth is one possible
implication if opportunity varies strongly between planets and dominates their success probabilities;
it is not required when rarity instead reflects a shared chemical barrier or other selection effects.
Appendix A.2 gives the lognormal calculation explicitly.

3 Constraining the transition model

3.1 The astronomical population

We write the abundance of candidate worlds schematically as n⋆
P
s xsηsfatm,s, where s indexes stellar
classes, xs is their share, ηs is the mean number of rocky habitable-zone planets per star, and fatm,s
describes atmosphere retention. Occurrence rates constrain ηs, but incident flux and atmospheric
retention are not complete habitability criteria (Bryson et al., 2021). Planet age, composition, water
availability, and stellar history can affect both eligibility and transition hazards.
For a numerical reference population, we retain the scenario assumptions in Table 1. Independent
propagation gives a Galactic candidate count with median 7.1 × 109 and central 68% interval
(3.4–14.7) × 109. Applying the same candidate fraction to an assumed (1–5) × 1022 stars gives a
reference count of order 1021 for the observable universe. These are conditional population scales, not
new empirical determinations of genuinely habitable worlds. In particular, the adopted atmospheric
fractions are scenario priors, not measurements of all temperate rocky planets.
A population of 7.1 × 109 worlds has an expected one successful world when its average completion
probability is approximately 1.4 × 10−10. The corresponding threshold for the reference observable-universe population is of order 10−21. This is the probabilistic content of the comparison between
astronomical abundance and biological rarity (Frank and Sullivan, 2016); logarithmic units add no
physical constraint. An expected count near one is a crossover in the count distribution, not a
statement that exactly one world exists.

## Page 6

A probabilistic Drake framework

3.2 Abiogenesis: from catalytic activity to establishment

Laboratory selection provides a concrete way to study pk under controlled conditions. A particularly
relevant example is the QT45 RNA polymerase ribozyme. The published study demonstrated synthesis
of its complementary strand and synthesis of the original strand in separate reactions; this establishes
an important catalytic capability, not an autonomous, sustained replication cycle under uncontrolled
planetary conditions (Gianni et al., 2026; MRC Laboratory of Molecular Biology, 2026). The earlier
preprint estimated a sequence-space frequency of approximately 4.4 × 10−18 for its motif under a
specified calculation (Gianni et al., 2024). Such estimates motivate route-specific priors, but do not
directly measure the probability that a planet originates life.
For this route, at least three links must be made explicit. The first is the frequency of suitable
molecular configurations under the relevant chemistry, rather than under an ideal random library.
The second is whether compatible components meet with suitable substrates and cycling conditions.
The third is whether their interaction establishes sustained heredity rather than a transient copying
event. Performance, fidelity, degradation, product inhibition, compartment dynamics, and substrate
supply can enter that last probability. They need not be independent.
A minimal compartment model makes the distinction quantitative. Suppose a compartment-generation event contains a Poisson number of functional molecules with mean λc = ncp1, where nc is
its expected candidate occupancy and p1 the functional probability per candidate. The probability of
containing at least ν functional molecules is
bν(λc) = 1 − e
−λc
νX−1
j=0
λ
j
c
j!
. (10)
Let Kc be the number of independent compartment-generation events and ρ the probability of
establishment conditional on an event satisfying this occupancy requirement. For rare successful
events,
H0 ≃ Kc ρ bν(ncp1) ≃ Kc ρ
(ncp1)
ν
ν!
. (11)
The second approximation requires ncp1 ≪ 1. If every event consumes a fresh group of nc candidates,
so that a total of A candidates corresponds to Kc = A/nc, then for ν = 2,
H0 ≃
A nc p
2
1 ρ
2
. (12)
This recovers the useful co-localisation scaling. It does not demonstrate that two randomly chosen
active molecules are mutually compatible or sufficient for life. The parameter ρ represents precisely
that missing connection, and must be defined to avoid double-counting requirements already included
in p1.
The mapping from A to Kc is a physical assumption, not a counting identity for arbitrary
environments. Long-lived compartments, repeated encounters, unequal occupancies, and exchange
between pores can alter it. Compartment volume and concentration should also be constrained jointly:
allowing occupancy to increase while ignoring encounter times and dilution can create spurious gains.

3.3 Candidate production and an illustrative calibration

For a stationary oligomer-production scenario, a first estimate of the number of newly generated
candidates is
A ≃ V cNA
Tpre
τ
, (13)

## Page 7

A probabilistic Drake framework
Table 2: Route-specific illustrative priors. Decimal logarithms are used only to express broad ranges
compactly. Standard deviations are squared in the normal-distribution notation. The numerical
implementation preserves unrounded endpoints; their provenance is documented in the accompanying
revision notes.
Quantity Adopted scenario
Functional motif frequency log10 pfold ∼ U(−17.37, −13.55)
Performance adjustment log10 aperf ∼ U(−9.03, 0)
Chemical sampling adjustment log10 bchem ∼ U(−1.51, 3.01)
Compartment occupancy log10 nc ∼ U(3.01, 9.03)
Median candidate exposure across worlds log10 Ae ∼ N (36.12, 4.522)
World-to-world exposure dispersion sd(log10 A | θ) = 1.81
Required occupancy; establishment ν = 2; baseline ρ = 1
The baseline assumes the listed quantities are independent at the parameter level and attributes interplanetary scatter
to A alone. These choices simplify the illustration but are not implied by the underlying chemistry. ρ = 1 is an
optimistic limiting case, not an experimental result.
where V is the active volume, c the molar concentration of candidates of the required kind, NA
Avogadro’s constant, Tpre the available interval, and τ their replacement time. This is an exposure
estimate. Its interpretation requires compatible definitions of production, turnover, and candidate
identity. A general version integrates V (t)c(t)NA/τ (t) over time, with zero contribution outside the
relevant chemical conditions (Scharf and Cronin, 2016, for planetary-scale opportunity modelling).
To examine the consequences of a laboratory-motivated route, let p1 = pfoldaperfbchem. Here aperf ≤ 1
is a conditional reduction for the specified performance requirement and bchem is a multiplicative
adjustment for the sampling chemistry. Table 2 specifies an illustrative scenario in probabilities and
opportunity counts. The entries are assumptions informed to different degrees by experiments; they
are not a jointly measured posterior. In particular, a performance–rarity relation observed for other
RNA functions is not established for autonomous replication (Carothers et al., 2004).
For the median world in a parameter draw, these choices give log10 He
0 ≃ 3.4 ± 7.9 before any
additional establishment penalty. The comparison prior is specified directly as log10 H0 ∼ N (0, 502),
with the same hazard on every world conditional on the draw, following the broad rate uncertainty used
by Sandberg et al. (2018). A diffuse prior should be placed on a nonnegative hazard, not implemented
through a putative per-trial probability that can exceed one. The route-specific log-hazard dispersion
is approximately 6.3 times smaller (Figure 2). That narrowing is conditional on choosing the route
and its parameter ranges; it is not equivalent to a sixfold reduction achieved by new data.

3.4 Heredity and later evolutionary transitions

The ability to maintain heredity constrains which catalytic systems can establish. In the simple
single-peak replication model, a master sequence with error-free copying probability Q and relative
replication advantage σ requires Qσ > 1. With independent per-site error probability ϵ across L
relevant sites, Q = (1 − ϵ)
L (Eigen, 1971). This is a useful consistency check on a proposed replicator.
It is not a universal upper bound on the negative logarithm of functional sequence frequency.
Functional sets can contain neutral networks and tolerate many sequence changes; copying fidelity,
mutational robustness, and function rarity are distinct properties. Establishment should be assessed
with a model of the actual genotype–phenotype and replication dynamics rather than by converting
every constrained site into a fixed information cost. Likewise, failure of one copying mechanism does
not show that all excess functionality must arise in a single random assembly event.

## Page 8

A probabilistic Drake framework
150 100 50 0 50 100 150
log10 median cumulative hazard
0.00
0.01
0.02
0.03
0.04
0.05
Prior density
Diffuse hazard prior
Route-specific scenario ( = 1)
Figure 2: The route-specific prior on the median cumulative hazard compared with a diffuse hazard
prior. Both distributions concern uncertainty in a model parameter. The separate world-to-world
dispersion is integrated when computing the inhabited fraction. Narrower prior support is not, by
itself, stronger empirical evidence.
After heredity exists, a transition hazard can depend on mutation, selection, population structure,
recombination, ecological interactions, and the persistence of intermediate genotypes. Counting all
cells that have ever existed provides neither the number of eligible trials for every innovation nor
a universal bound on the number of coordinated mutations evolution can achieve. Fitness-valley
crossing, for example, depends on the dynamics of intermediates as well as on individual mutation
probabilities (Weissman et al., 2009). The opportunity-rate description remains useful when those
dynamics can be reduced to a justified effective hazard.

3.5 The replication-clock hard-steps limit

Suppose n ordered transitions have hazards hk(t) = αkr(t) after their predecessors have occurred, where
the same nonnegative opportunity clock r(t) applies to every step. Define cumulative opportunities
U(T) = R T
0
r(t) dt. If αkU(T) ≪ 1 for every required transition, then
Pn(T) ≃
U(T)
n
n!
Yn
k=1
αk. (14)
Conditional on completion, the coordinates U(T1), . . . , U(Tn) have, to leading order, the distribution
of the ordered values of n independent uniforms on [0, U(T)]. Appendix A.3 gives the derivation.
Constant r recovers the familiar T
n hard-steps scaling (Carter, 1983).
This result preserves two important conclusions. Available biological opportunity, not calendar
time alone, can control transition probabilities. Also, conditional timing in this rare-event model
does not identify the individual rate scales αk: their common multiplicative contribution cancels
when conditioning on completion. Earth-like chronologies can therefore be compatible with very
different unconditional probabilities of reaching observers. Inferring even the number of steps requires
assumptions about the opportunity clock and the transitions included.
Environmental gating and intrinsic rarity can coexist, but one does not generally reduce to the other.

## Page 9

A probabilistic Drake framework
Table 3: Recomputed prior-predictive summaries for the reference population. µ = nhabflife is an
expected count over the scenario’s specified opportunities. The final column is prior mass below a
mean-count threshold, not the probability that Earth is alone. Results use 106 parameter draws.
Scenario P(He0 > 1) P(flife ≥ 0.1) P(µ < 1)
Route-specific, ρ = 1 0.661 0.772 0.013
Same priors, ρ = 10−3 0.520 0.646 0.037
Same priors, ρ = 10−6 0.377 0.505 0.084
Same priors, ρ = 10−9 0.247 0.362 0.161
Same priors, ρ = 10−12 0.144 0.234 0.271
Diffuse hazard comparator 0.500 0.508 0.422
A more flexible model is hk(t) = rk(t)αk(t)gk(t), where gk describes the environmental permissibility
of step k. A gate may prevent a transition even while unrelated organisms are abundant. The
common-clock theorem applies only when these effects can actually be represented by proportional
rates. Otherwise Equation (4) or a corresponding state model is needed. This gives a common
framework for comparing hard-step and environment-gated accounts without claiming that they are
observationally equivalent (Mills et al., 2025).

4 Consequences and observational tests

4.1 What the illustrative abiogenesis model implies

An independent Monte Carlo propagation of Tables 1 and 2, with numerical averaging of Equation (8),
gives P(He
0 > 1) = 0.661 and P(flife ≥ 0.1) = 0.772 for the baseline scenario. The median expected
count in the reference population is approximately 4.3 × 109. The diffuse hazard prior gives P(flife ≥
0.1) = 0.508. Thus the route-specific assumptions favour widespread abiogenesis relative to the diffuse
comparator, without making that conclusion certain.
Table 3 exposes a missing sensitivity: establishment after co-localisation. Decreasing ρ shifts
log10 H0 by log10 ρ. The example values are stress tests, not estimated probabilities or a confidence
range. More generally, changing pathways, correlating chemical inputs, adding missing prerequisites,
or truncating the favourable environmental tail can alter the inference beyond one-at-a-time variations
of existing parameters.
The supported conclusion is conditional but substantive: a specified small-replicase route does not
require an extremely low planetary success probability under these opportunity and establishment
assumptions. The stronger assertion that laboratory measurements already establish a small probability
of Galactic solitude does not follow. That claim would require both a defensible likelihood for the
chemical parameters and an explicit treatment of how our own existence enters the data.

4.2 Expected counts, solitude, and observer selection

For conditionally independent worlds with completion probabilities fj (θ),
P(ZX = 0 | θ) = Y
j
[1 − fj (θ)], µX(θ) = X
j
fj (θ). (15)
When individual probabilities are small, the zero-count probability is approximately e
−µX . At µX = 1,
this is about 0.37, not certainty of either solitude or company. Shared uncertainty requires integrating

## Page 10

A probabilistic Drake framework
Equation (15) over the parameter distribution; exponentiating a posterior mean count is generally
incorrect.
If D includes the relevant terrestrial and observational evidence, the probability of no other inhabited
worlds is
P(Zother = 0 | D) = Z Y
j̸=⊕
[1 − fj (θ)] p(θ | D) dθ. (16)
A probability that µ is below one, or below two, answers a different question. Nor can a known
inhabited Earth simply be subtracted from an unconditioned expected population without updating
the model.
Conditioning on at least one inhabited world somewhere in the observable universe is one possible
selection event, not a unique prescription for conditioning on our observations. The relevant likelihood
depends on what is sampled: planets, inhabited histories, observer-producing histories, or observers.
Earth’s early evidence for life also enters through uncertain habitability and detection times, together
with the time needed for observers to emerge (Spiegel and Turner, 2012; Kipping, 2020). The illustrative
prior propagation above is deliberately not presented as this posterior calculation. Appendix A.4
gives a simple conditional-timing likelihood to make the distinction explicit.

4.3 Host stars and technological states

The replication-clock limit supplies a conditional prediction for host-star statistics. If comparable
worlds around different stellar classes have the same per-opportunity transition coefficients, and differ
mainly in usable opportunity Us, the production of observer-bearing histories scales as U
n
s
in the
rare-event regime. Additional hard steps therefore strengthen the preference for stellar populations
offering larger accumulated opportunity. A G-dwarf host can favour fewer such steps when the
comparison population of longer-lived stars has comparable chemistry, productivity, and observer
weighting.
A quantitative likelihood nevertheless requires the distribution of stellar formation times, age-limited
habitable windows, productivity, and a definition of the observer sample. Counting worlds that ever
produced observers is not the same as counting observers alive today. Host luminosity or spectral
class can change both environmental hazards and detectability. Bayes factors for ranges of step counts
further require priors within those ranges and over nuisance parameters. The host-star argument is
consequently a useful proposed test, not a model-independent measurement of the number of hard
steps (Haqq-Misra et al., 2018). An appropriate weighting expression is given in Appendix A.5.
For technology, the same distinction between occurrence and occupancy applies. Under stationary
births and a representative constant lifetime ℓ, a reference population formed approximately uniformly
over Tpop would have µ
now
tech ≃ nhabPtechℓ/Tpop. Taking nhab ≃ 7 × 109 and Tpop = 1010 yr solely as
an illustration, a mean contemporary count of one requires Ptech ≃ 1.4 × 10−4for ℓ = 104 yr, or
1.4 × 10−6for ℓ = 106 yr. These are conditional rate–lifetime tradeoffs, not sharp boundaries between
possible and impossible civilisations.
Non-detections constrain the abundance of sources only through the surveys’ selection functions. A
geometric fraction of a proposed SETI search space is not automatically the probability of detecting
a civilisation; the distribution of sources within that space matters (Wright et al., 2018). A single
detection would be transformative, but would not independently identify evolutionary probabilities,
emission properties, and lifetimes.

## Page 11

A probabilistic Drake framework

4.4 Biosignatures as model comparison

The likelihood that a process produces a functional system and the likelihood that it produces an
observation are related modelling problems, not generally the same probability. Let L and A denote
biotic and abiotic hypotheses, and let d be the observed data. The evidential comparison is the Bayes
factor
BFL,A(d) =
R
p(d | ψL,L)π(ψL | L) dψL
R
p(d | ψA, A)π(ψA | A) dψA
. (17)
Posterior odds equal prior odds times this factor. For continuous observations the quantities integrated
are likelihood densities; the probability of one exact measured value is not the relevant event probability.
There is a useful special connection to the transition model. If a pre-specified signature event E is
triggered by at least one abiotic production event with Poisson mean HA, then P(E | A) = 1 − e
−HA .
For HA ≪ 1, log BF(E) ≃ − log HA + log P(E | L). This expresses the sound underlying idea: a
persuasive signature must be difficult for a realistic abiotic model to generate and plausible under a
biotic alternative. The Poisson representation is an additional model of the observation, however, not
a universal identity for spectra or molecular complexity.
Atmospheric composition, molecular ensembles, disequilibria, and temporal variability should
therefore be evaluated through competing generative models. A gas is not intrinsically weak evidence
merely because it is a single species, nor is a complicated pattern intrinsically strong evidence if
abiotic alternatives or measurement systematics predict it. Statistical significance is also not a
model-independent conversion to evidence for life: a p-value is not a Bayes factor, and calibrations
require stated assumptions (Sellke et al., 2001). The same caution applies to molecular-complexity
thresholds and to technosignatures. A thermodynamic dissipation bound, for example, becomes a
detection prediction only after specifying a process rate, temperature, and observable emission model
(Landauer, 1961).

4.5 What surveys and experiments can establish

For target i, let fi(θ) be the probability of life in the specified sense, di the probability of a positive
classification given life, and αi the probability of a positive classification without life. The detection
efficiency can include whether an inhabited planet currently produces a detectable signature. Then
qi(θ) = αi + (di − αi)fi(θ), Yi ∼ Bernoulli(qi(θ)
)
. (18)
The joint likelihood is the product over targets conditional on shared parameters; uncertainty in
calibration or population structure must then be integrated. Unknown efficiency can be confounded
with prevalence, and target selection must be included when the surveyed planets do not represent
the population of interest.
A few dozen well-characterised planets can strongly distinguish nearly ubiquitous life from extremely
rare life under suitably concentrated priors. The crossover in Equation (3) helps explain why such
priors arise in some chemical models, but does not by itself guarantee a decisive survey.
For a specific forecast, take independent targets with known d = 0.6 and α = 0.02, and define
S = {flife ≥ 0.1}. Under the route-specific baseline, 25 targets reduce the expected uncertainty about
S by 0.449 nats out of a prior entropy of 0.537 nats, and give a posterior probability above 0.95 or
below 0.05 in 84% of prior-predictive outcomes. Five targets achieve that decision threshold in 62% of
outcomes (Table 4). These forecasts support the value of modest surveys within the specified model.
They do not include unknown shared calibration errors or establish a prior-independent sample-size
guarantee.

## Page 12

A probabilistic Drake framework
Table 4: Recomputed survey forecasts under Equation (18) with known detection efficiency 0.6 and
false-positive rate 0.02. The target proposition is S = {flife ≥ 0.1}. Entropy reduction uses natural
logarithms; “resolves S” means a posterior probability at least 0.95 or at most 0.05. Values are
conditional on each stated prior and this observation model.
Prior Targets Entropy reduction (nats) Probability of resolving S
Route-specific baseline 5 0.328 0.615
Route-specific baseline 25 0.449 0.838
Diffuse hazard comparator 5 0.582 0.912
Diffuse hazard comparator 25 0.678 0.990
0.0 0.1 0.2 0.3 0.4 0.5 0.6
Inhabited fraction of target population
0.0
0.2
0.4
0.6
0.8
1.0
Probability of 25 non-detections
Perfect detection; no false positives
Detection 60%; false positives 2%
Figure 3: The likelihood of 25 non-detections under two explicitly calibrated observation models. The
horizontal dotted line marks a probability of 0.05. A small survey’s ability to establish a prevalence
threshold depends on efficiency, false positives, the population model, and prior uncertainty, not just
the shape of the single-world transition curve.
The dependence on the inferential question is important. For 25 independent targets with perfect
detection and no false positives, zero detections have probability (1 − f)
25. At f = 0.1 this is 0.0718,
and the exact one-sided 95% frequentist upper limit after zero detections is 1 − 0.051/25 = 0.113. Thus
25 non-detections do not quite exclude a prevalence of 10% even in this ideal case. With d = 0.6 and
α = 0.02, their probability at f = 0.1 rises to 0.131 (Figure 3). These are likelihood calculations, not
posterior conclusions.
Laboratory and geochemical measurements address complementary factors in H0. Functional
screening under realistic synthesis conditions constrains candidate probabilities. Measurements of
oligomer abundance and turnover constrain exposure. Encapsulated, sustained replication constrains
establishment and the relation between occupancy and successful heredity. Multiple plausible chemical
routes should be tested rather than treating one as exhaustive. Route hazards can be added when
they are distinct competing event channels in the same eligible state; simply adding probabilities of
overlapping functional sets double-counts configurations.
A genuinely independent second origin would provide a particularly important likelihood contribution, especially in an environment predicted to offer fewer opportunities. It would not impose a
deterministic lower bound on every world’s success probability or guarantee that life is common: rare

## Page 13

A probabilistic Drake framework
events can occur, routes can differ, and shared ancestry or transfer must be excluded (Spiegel and
Turner, 2012).
Experiments can be compared by their expected reduction in uncertainty about a stated proposition,
such as S = {flife ≥ 0.1}. For design a, one suitable quantity is H(S | D) − Ey|a,D[H(S | D, y, a)],
where H is entropy. This is a genuine information-theoretic quantity, but its numerical value depends
on the prior, the experiment’s likelihood, and the decision threshold. A claim that a particular
programme will settle the prevalence of life requires those assumptions and a reproducible calculation,
rather than the transition crossover alone.

5 Discussion

The framework is deliberately modular. A mechanistic model can refine a transition hazard without
changing the population accounting; a new survey can improve the observation model without
pretending to determine the chemical mechanism uniquely. This separation also clarifies identifiability.
A measured transition fraction often constrains a cumulative hazard but cannot distinguish many
low-probability opportunities from fewer high-probability ones. Laboratory data and environmental
measurements are needed to separate those contributions.
Three limits deserve emphasis. First, a convenient search model is not evidence that all relevant
chemistry is independent sampling. Persistent networks, spatial correlations, changing feedstocks, and
prior selection can change both the generated candidates and their chances of establishment. Second,
a chosen functional route is not the full event “life originates”. Alternative routes can raise the total
hazard, while missing prerequisites can lower it; both are structural uncertainties. Third, a planet is
not an isolated Bernoulli trial if material transfer, common formation history, or shared environments
create dependence. Independence is a conditional modelling assumption whose adequacy depends on
the scale of the population.
The framework builds directly on existing work rather than claiming a new probability law. The
single-event expression is the standard waiting-time relation used in abiogenesis models (Sandberg et
al., 2018); planetary exposure modelling connects it to physical opportunities (Scharf and Cronin,
2016). The replication-clock limit extends the interpretation of hard-step timing without removing its
assumptions (Carter, 1983; Mills et al., 2025). Functional rarity remains useful when its sampling
measure and success criterion are specified (Hazen et al., 2007). The astronomical abundance threshold
is the inverse of a candidate-population size (Frank and Sullivan, 2016). Their integration is valuable
because it turns informal biological fractions into quantities linked to explicit mechanisms, data, and
tests.
The illustrative RNA calculation sustains the motivating optimism: widespread abiogenesis is
compatible with a concrete small-replicase route and substantial planetary opportunity. Its uncertainty
is narrower than that of a deliberately diffuse rate model. The narrowing should not be oversold. It
arises partly because the chemical route, parameter support, and missing establishment probability
have been fixed. Progress means measuring those assumptions, comparing alternative mechanisms,
and reporting how posterior predictions change, not merely choosing a tighter prior.

6 Conclusion

A biological factor in the Drake equation can be treated as the probability that a specified transition
completes within a finite period of opportunity. The central quantitative object is the cumulative
hazard, built where possible from candidate production, functional probability, and successful es-

## Page 14

A probabilistic Drake framework
tablishment. Ordered transitions require conditional waiting times; observable populations require
formation histories, occupancy durations, and detection models.
This perspective preserves the useful conclusions of an opportunity-based account. Astronomical
abundance can compensate for low per-world probabilities. Favourable planets can contribute
disproportionately, although the effect of heterogeneity depends on the comparison population.
Evolutionary timing may constrain aspects of an opportunity clock while leaving absolute transition
rates weakly identified. Laboratory results can motivate substantially more informative chemical
models, and modest, well-calibrated surveys can be highly discriminating.
The remaining uncertainty is attached to identifiable questions: which chemical systems can establish
heredity, how often they are generated in realistic environments, how much relevant opportunity
planets provide, and which observations distinguish life from abiotic alternatives. The purpose of
the framework is not to declare those questions settled. It is to make their assumptions explicit and
connect their answers to the prevalence of observable life.
Code and numerical scope. The accompanying recompute.py independently implements the
illustrative priors, numerical population averages, reference counts, establishment stress tests, and
three figures in this revision. The reported run uses 106 draws and seed 20261014; the quadrature
is checked against adaptive integration. The code also computes Table 4 under its explicitly known
survey calibration. It does not estimate an observer-conditioned solitude posterior, a host-star Bayes
factor, or laboratory-experiment utilities; those require additional likelihoods and assumptions.
Acknowledgements. The submitted manuscript acknowledged AI assistance from Claude (Anthropic). This revision additionally used ChatGPT (OpenAI) for mathematical restructuring, editing,
and an independent numerical implementation. The author(s) should review the analysis, source
attributions, and journal disclosure requirements before submission.
A Technical details
A.1 A bound for the logarithmic approximation
For H ≥ 1, 1 − e
−H increases from 1 − e−1
to one. For 0 < H < 1, (1 − e
−H)/H decreases from one
to 1 − e
−1
. Hence
(1 − e
−1
) min(1, H) ≤ 1 − e
−H ≤ min(1, H), (19)
which gives
0 ≤ − log(1 − e
−H) − [− log H]+ ≤ − log(1 − e−1
) ≃ 0.459. (20)
The logarithm is natural here. Under a justified product model these errors add across factors, but
the bound does not control the error from replacing a sequential process by such a product. The
exact Bernoulli exponent is −A log(1 − p) = Ap{1 + p/2 + O(p
2
)}; thus the Poisson replacement has
a relative exponent error of order p.
A.2 The lognormal population average
Let X = log H ∼ N (m, s2), s > 0. Replacing the exact success function by min(1, eX) gives
E[min(1, eX)] = Φ(m
s
)
+ e
m+s
2/2Φ

−
m + s
2
s
!
. (21)

## Page 15

A probabilistic Drake framework
This follows by completing the square in the truncated normal moment. It is an upper approximation to
the exact inhabited fraction, with a universal multiplicative lower bound obtained from Equation (19).
Numerical calculations in the main text use the exact expectation instead. In the limit m → −∞ at
fixed s, saturation becomes negligible in the relevant part of the distribution and the result tends to
e
m+s
2/2
.
In the same rare-event limit, weighting worlds by success multiplies their density by e
X. Consequently, X among successful worlds is approximately N (m + s
2
, s2). This is a conditional sampling
bias, not proof of an anomalous Earth. Its applicability depends on the assumed source of interplanetary variation, the accuracy of the rare-event limit, and any additional observer selection.
Predictions dominated by an extrapolated upper tail should be checked against physical truncations
and finite-population sampling.
A.3 Ordered completion on a common clock
Set u = U(t) and U = U(T). In this coordinate, stage k has constant hazard αk after stage k − 1.
The joint completion density on 0 < u1 < · · · < un < U is
Yn
k=1
αk exp{−αk(uk − uk−1)}, u0 = 0. (22)
When P
k αkU is small, replacing the exponential factors by one has a relative error of that order.
The ordered simplex has volume U
n/n!, yielding Equation (14). Normalisation by the completion
probability removes Q
k αk and gives the uniform order-statistics density n!/Un
.
For equal constant hazards h, the exact completion probability for n stages is the Erlang cumulative
distribution,
Pn(T) = 1 − e
−hT
nX−1
j=0
(hT)
j
j!
. (23)
It approaches (hT)
n/n! only in the rare-event limit and approaches one when hT is large. For step-specific opportunity clocks, the leading rare-event result is instead an ordered integral of Q
k hk(tk).
It does not generally factor into a product of full-window hazards divided by n!.
A.4 A simple observer-conditioned timing likelihood
Assume, solely for illustration, that abiogenesis has constant hazard h from time zero, that the
observation establishes completion by te, and that observers can exist only if completion occurs by
a known deadline tmax ≥ te. If that deadline is the entire selection model, the likelihood of the
early-completion observation conditional on selection is
P(Tlife ≤ te | Tlife ≤ tmax, h) = 1 − e
−hte
1 − e−htmax
. (24)
As h → 0 this tends to te/tmax, rather than zero; for very large h it tends to one. The evidence is
therefore limited under this selection model. Uncertain dates, variable hazards, and stochastic later
evolution require integration over the appropriate additional variables (Spiegel and Turner, 2012;
Kipping, 2020).

## Page 16

A probabilistic Drake framework
A.5 Host-star likelihoods
Let bs(tb) describe eligible world births around stellar class s, gn,s(u | ψ) the density of first observer-producing completion at planetary age u, and ωs(t0, tb + u, ψ) the expected contribution of that
completed history to the specified observer sample. Then a general weight is
Ws(n, ψ) = Z t0
0
bs(tb)
Z t0−tb
0
gn,s(u | ψ)ωs(t0, tb + u, ψ) du dtb, P(s | n, ψ, O) = Ws P
s
′ Ws
′
. (25)
Setting ωs = 1 counts successful world histories by the present, not all observers currently alive.
Observation at a particular epoch generally needs a duration-dependent weight. Environmental gates
and age limits enter gn,s; spectral effects on productivity enter the opportunity clock. A comparison
of composite hypotheses such as n ≤ 2 and 3 ≤ n ≤ 6 must average the host likelihood over specified
within-hypothesis priors for n and ψ. These requirements prevent a conditional host preference from
being mistaken for a universal Bayes factor.

References

Bryson, S., et al. 2021. The occurrence of rocky habitable-zone planets around solar-like stars from Kepler data.
AJ, 161, 36.
Carothers, J. M., Oestreich, S. C., Davis, J. H., and Szostak, J. W. 2004. Informational complexity and
functional activity of RNA structures. JACS, 126, 5130–5137.
Carter, B. 1983. The anthropic principle and its implications for biological evolution. Phil. Trans. R. Soc. A,
310, 347–363.
Drake, F. D. 1965. In Current Aspects of Exobiology, ed. G. Mamikunian and M. H. Briggs (Oxford: Pergamon),
323.
Eigen, M. 1971. Selforganization of matter and the evolution of biological macromolecules. Naturwissenschaften,
58, 465–523.
Frank, A., and Sullivan, W. T. 2016. A new empirical constraint on the prevalence of technological species in
the universe. Astrobiology, 16, 359–362.
Gianni, E., et al. 2024. A polymerase ribozyme that can synthesize both itself and its complementary strand.
bioRxiv. doi:10.1101/2024.10.11.617851.
Gianni, E., Kwok, S. L. Y., Wan, C. J. K., et al. 2026. A small polymerase ribozyme that can synthesize itself
and its complementary strand. Science, 391, 1022–1028. doi:10.1126/science.adt2760.
Haqq-Misra, J., Kopparapu, R. K., and Wolf, E. T. 2018. Int. J. Astrobiol., 17, 77.
Hazen, R. M., Griffin, P. L., Carothers, J. M., and Szostak, J. W. 2007. Functional information and the
emergence of biocomplexity. PNAS, 104, 8574–8581. doi:10.1073/pnas.0701744104.
Kipping, D. 2020. An objective Bayesian analysis of life’s early start and our late arrival. PNAS, 117, 11995–12003.
doi:10.1073/pnas.1921655117.
Landauer, R. 1961. Irreversibility and heat generation in the computing process. IBM J. Res. Dev., 5, 183–191.
Licquia, T. C., and Newman, J. A. 2015. ApJ, 806, 96.
Mills, D. B., Macalady, J. L., Frank, A., and Wright, J. T. 2025. A reassessment of the “hard-steps” model for
the evolution of intelligent life. Science Advances, 11, eads5698. doi:10.1126/sciadv.ads5698.

## Page 17

A probabilistic Drake framework
MRC Laboratory of Molecular Biology. 2026. Bridging the gap from chemistry to life: discovery of a tiny RNA
that can copy itself. Research account of Gianni et al. (2026), accessed 14 October 2026.
Reylé, C., et al. 2021. A&A, 650, A201.
Sandberg, A., Drexler, E., and Ord, T. 2018. Dissolving the Fermi paradox. arXiv:1806.02404.
Scharf, C., and Cronin, L. 2016. Quantifying the origins of life on a planetary scale. PNAS, 113, 8127–8132.
Sellke, T., Bayarri, M. J., and Berger, J. O. 2001. Calibration of p values for testing precise null hypotheses.
The American Statistician, 55, 62–71. doi:10.1198/000313001300339950.
Spiegel, D. S., and Turner, E. L. 2012. Bayesian analysis of the astrobiological implications of life’s early
emergence on Earth. PNAS, 109, 395–400. doi:10.1073/pnas.1111694108.
Weissman, D. B., Desai, M. M., Fisher, D. S., and Feldman, M. W. 2009. The rate at which asexual populations
cross fitness valleys. Theor. Popul. Biol., 75, 286–300. doi:10.1016/j.tpb.2009.02.006.
Wright, J. T., Kanodia, S., and Lubar, E. 2018. How much SETI has been done? Finding needles in the
n-dimensional cosmic haystack. AJ, 156, 260.
