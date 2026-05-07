# VEHICLE-ODI: A Relational Decision Architecture for Orbital Debris Prioritization

**Article type proposed:** Hypothesis and Theory  
**Target journal/section:** Frontiers in Space Technologies, Space Debris  
**Author:** Roberto Borda Milan  
**ORCID:** https://orcid.org/0009-0009-9047-1036  
**Affiliation:** VEHICLE Systems Lab, Santa Cruz, Bolivia  
**Correspondence:** Roberto Borda Milan, contact@vehiclesystemslab.com  
**Website:** https://vehiclesystemslab.com

**Running title:** VEHICLE-ODI for orbital debris prioritization

**Word count:** manuscript text excluding references, approximate.

```{=openxml}
<w:p><w:r><w:br w:type="page"/></w:r></w:p>
```

# Abstract

Orbital debris is commonly addressed through detection, cataloguing, orbit determination, conjunction assessment, mitigation rules and, increasingly, active debris removal. These layers are indispensable, yet they do not fully resolve a prior decision problem: when many objects, fragments, clouds and orbital regions compete for limited observation, maneuver and intervention capacity, which debris matters most first? This manuscript introduces VEHICLE-ODI (Orbital Debris Intelligence), a relational decision architecture that treats the orbital debris environment as a structured field under tension rather than as a list of isolated catalogued objects. The architecture applies the Borda Milan Pyramid and the VEHICLE Formula-as-Architecture to represent intact bodies, fragments, debris clouds, vulnerable assets and orbital regions as nodes and relations in a dynamic graph. It distinguishes external relational tension, internal object incoherence, propagation potential, regional vulnerability and admissible intervention pathways. Six operational regimes, A1-A6, are proposed to classify debris relevance: critical conjunction risk, recovered object, fragmentation pressure, filtered fragment, dangerous rigid mass and fluid fragmentation cloud. An experimental Orbital Tension Index (OTI) is introduced as a bounded, explainable signal for comparing structural stress across orbital regions over time. VEHICLE-ODI is not presented as a replacement for space situational awareness, astrodynamics, space traffic management or active debris removal. It is proposed as a decision-support layer for prioritizing what should be observed, avoided, stabilized, moved or removed first. A minimal synthetic simulation design is provided to make the hypothesis testable before operational use. The contribution is a formal, auditable language for debris prioritization before removal.

**Keywords:** orbital debris; space sustainability; space situational awareness; space traffic management; active debris removal; relational systems; structural coherence; Orbital Tension Index; VEHICLE-ODI; Borda Milan Pyramid

# 1. Introduction: orbital debris as a relational risk field

Earth orbit is no longer a sparse technical environment. It is a shared operational domain populated by active satellites, inactive spacecraft, rocket bodies, mission-related objects, collision fragments, diffuse fragment clouds, uncertainty volumes and strategic orbital regions. The European Space Agency's 2025 public assessment describes a rapidly growing environment, with about 40,000 tracked objects and an estimated population of more than 1.2 million objects larger than 1 cm in orbit (European Space Agency, 2025). This scale forces a practical shift from object awareness alone toward structural prioritization.

The debris problem is not only a matter of counting objects. The operational relevance of an object depends on orbit, relative velocity, uncertainty, proximity to valuable assets, persistence, fragmentation potential, legal-operational constraints and the region through which it propagates. A small object in a sensitive corridor may be more important than a larger object in a less consequential relation. A large inactive body may be quiet today while carrying latent fragmentation potential in a dense altitude band. A diffuse cloud may be less dramatic than a single intact mass but may distribute risk across many relations.

VEHICLE-ODI begins from this observation: orbital debris is not merely an inventory. It is a relational risk field. The field changes as objects move, covariance evolves, assets maneuver, conjunctions emerge, and fragmentation events create new objects and new relations. The central question is therefore not only where debris is, but which relations concentrate tension.

The hypothesis advanced here is that a graph-based, projection-governed decision architecture can make orbital debris prioritization more explicit and explainable before observation, avoidance, stabilization, relocation or removal resources are allocated. The architecture is not intended to replace astrodynamics or operational tracking. It is intended to sit above existing sources of orbital knowledge as a structural decision layer.


![Figure 1. VEHICLE-ODI relational decision architecture. Orbital objects, fragments, debris clouds, protected assets and orbital regions are converted into structured graph nodes. External and internal tension components feed the Orbital Tension Index and A1-A6 operational regimes, producing supervised decision-support recommendations before observation, avoidance, stabilization, relocation or removal actions are considered.](VEHICLE_ODI_Figure_1.png){width=6.3in}


# 2. Problem: prioritization before removal

Current orbital safety practice depends on observation, tracking, catalogues, orbit propagation, conjunction assessment, collision avoidance, mitigation guidelines, post-mission disposal, passivation and emerging active debris removal. These layers are necessary. However, the practical bottleneck increasingly takes the form of prioritization. There are more potentially relevant objects than there are sensors, analysts, maneuvers, removal missions, legal permissions or funding pathways.

A system may know many objects and still struggle to decide which object, relation or orbital region should receive priority. This problem becomes more difficult when decision candidates are heterogeneous. A short-term conjunction, a tumbling rocket body, an inactive satellite, a recovered object, a fragment cloud and a low-relevance tracked fragment do not represent the same kind of decision object. Treating them only through one scalar risk score may hide structural differences that matter for action.

VEHICLE-ODI therefore proposes a regime-based prioritization layer. Instead of asking only whether an object has a high or low risk value, the system asks what type of relevance the object or relation expresses. Is it an immediate conjunction problem? Is it a large rigid mass with latent fragmentation potential? Is it a diffuse cloud that increases regional stress? Is it a filtered fragment that should remain known but not prioritized? Is it a recovered or reclassified object that changes the tension field?

The claim is deliberately modest. VEHICLE-ODI does not claim to predict all collisions, replace propagation models, remove objects, or decide legal authority. It proposes an architecture for organizing existing and synthetic information into a relational field where different forms of tension can be compared. Its value is interpretive and computational: making the prioritization problem explicit, auditable and testable.

# 3. Borda Milan Pyramid integration

The Borda Milan Pyramid provides the conceptual path from observed domain to structured decision support. In VEHICLE-ODI, the pyramid is used to convert orbital objects and regions into a graph of structured nodes, measure relational and internal tension, classify operational regimes and support admissible decision pathways.

Table 1 summarizes the interpretation.

| Pyramid layer | VEHICLE-ODI interpretation |
|---|---|
| Observed domain | Orbital debris, active spacecraft, inactive bodies, orbital regions, conjunction corridors and debris clouds. |
| Relational conversion | Objects and regions become nodes in a graph; conjunctions, shared corridors, uncertainty volumes and propagation pathways become relations. |
| Structured node | Each node carries an E.I.A.R.(V)-type state describing external relations, internal condition, admissible actions, risk propagation and value-weighted vulnerability. |
| Dual tension | External tension across relations and internal incoherence inside objects are measured together. |
| Projection-governed correction | Candidate responses are projected onto admissible action sets such as observe, avoid, stabilize, move, remove or filter. |
| Operational regimes | A1-A6 classify the type of debris relevance rather than only its magnitude. |
| Attractor discovery | Simulation identifies persistent high-tension structures, recurring debris corridors and latent fragmentation attractors. |
| Decision support | Analysts receive a ranked and explained map of orbital priorities before expensive or irreversible interventions are considered. |

This pyramid interpretation is important because it prevents VEHICLE-ODI from becoming a loose metaphor. Each level defines a transition: from domain observation to graph construction, from graph construction to tension measurement, from tension measurement to regime classification, and from classification to decision support.

# 4. VEHICLE-ODI architecture

VEHICLE-ODI represents the orbital environment as a dynamic graph:

\[
G(t) = (N(t), E(t)).
\]

The node set \(N\) may include active payloads, inactive satellites, rocket bodies, large fragments, fragment-cloud abstractions, protected orbital regions, high-value assets, corridor segments and uncertainty volumes. The edge set \(E\) represents relations that matter for decision-making: conjunction proximity, shared orbital corridor, fragmentation influence, asset exposure, region vulnerability, legal-operational coupling, maneuver feasibility and sensor uncertainty.

Each node \(i\) carries a structured state:

\[
S_i = (E_i, I_i, A_i, R_i, V_i).
\]

In the ODI context, \(E_i\) represents external orbital relations such as proximity pressure, corridor density or exposure to other nodes. \(I_i\) represents internal object condition, including instability, age, stored energy, tumbling state, mass, non-cooperative status or fragmentation potential. \(A_i\) represents admissible action pathways, such as observe, avoid, stabilize, move, remove or filter. \(R_i\) represents risk reception and propagation relations. \(V_i\) represents value-weighted vulnerability, including crewed assets, mission-critical satellites, protected orbital bands or strategically sensitive regions.

The total system tension is written as:

\[
T(X) = T_{ext}(X) + \lambda T_{int}(X),
\]

where \(T_{ext}\) describes relational pressure across graph edges and \(T_{int}\) describes internal incoherence within nodes. The parameter \(\lambda\) allows scenario-specific calibration. In an early implementation, \(T_{ext}\) may combine conjunction probability proxies, relative velocity, covariance, density, asset value exposure and corridor sensitivity. \(T_{int}\) may combine fragmentation potential, mass, tumbling state, residual energy, age and non-cooperative status.

A projection-governed update can be expressed as:

\[
V_{op}(S_i) = P_K[S_i - \gamma \nabla_{S_i}T(X)],
\]

\[
S_i(t+1) = (1-\alpha)S_i(t) + \alpha V_{op}(S_i(t)).
\]

Here \(P_K\) projects a candidate correction onto the admissible set \(K\). In an operational context, \(K\) encodes legal, physical, mission, sensor and coordination constraints. This is central to the architecture: a high tension value is not permission to act. It is a reason to examine which admissible responses exist.

# 5. A1-A6 operational regimes

VEHICLE-ODI introduces A1-A6 as a taxonomy of orbital debris relevance. The regimes are not intended to replace probability of collision, catalog identifiers or mission-specific risk assessment. They provide an interpretive language that explains why a node or relation has become important.

| Regime | Name | Meaning | Typical decision support |
|---|---|---|---|
| A1 | Critical conjunction risk | A relation expresses immediate or near-term conjunction pressure involving vulnerable assets or sensitive corridors. | Refine tracking, examine covariance, prepare avoidance planning and human review. |
| A2 | Recovered object | An object or relation has been reclassified, reacquired, stabilized or removed from a previous high-tension interpretation. | Update catalogue relation, reduce obsolete alerts, preserve audit trail. |
| A3 | Fragmentation pressure | A body or cluster expresses elevated likelihood of fragment generation or propagation stress. | Study passivation history, internal incoherence, regional exposure and long-term mitigation value. |
| A4 | Filtered fragment | A fragment remains known but does not currently dominate regional tension under declared assumptions. | Maintain awareness without priority escalation. |
| A5 | Dangerous rigid mass | A large inactive or non-cooperative body carries latent systemic danger because collision or breakup could generate many fragments. | Long-term removal candidate analysis, stabilization study or priority observation. |
| A6 | Fluid fragmentation cloud | A distributed debris field increases regional vulnerability even when no single object dominates. | Regional mapping, density modeling, corridor warning and OTI monitoring. |

The regime taxonomy separates type from magnitude. A node may have moderate immediate conjunction risk but high latent mass danger. Another may be small but positioned in a high-value corridor. A cloud may have no dominant object but still raise regional stress. The A-regimes allow the system to explain these distinctions.

# 6. Orbital Tension Index

The Orbital Tension Index (OTI) is proposed as a normalized research signal for comparing structural tension by orbital region over time. It is not a universal risk number and should not be interpreted as an operational collision probability. Its role is to summarize relational stress in a defined region under a declared model.

For a region \(R\) at time \(t\), a first experimental form may be written as:

\[
OTI_R(t) = Normalize\left[\sum_{i \in R} w_iT_i(t) + \sum_{(i,j) \in E_R} w_{ij}\tau_{ij}(t)\right],
\]

where \(T_i(t)\) is node tension, \(\tau_{ij}(t)\) is edge tension, \(w_i\) and \(w_{ij}\) encode mission value or regional sensitivity, and the normalization maps the result onto a bounded scale such as 0-1 or 0-100.

The value is meaningful only with explicit assumptions. An OTI score should therefore be accompanied by the dominant contributing regimes A1-A6. A region whose OTI is driven by A1 events should be interpreted differently from one driven by A5 masses or A6 clouds.

The index has three intended uses. First, it can identify regions whose tension is increasing. Second, it can compare intervention candidates under a shared decision language. Third, it can evaluate whether simulated actions reduce structural tension. A useful OTI is therefore not merely high or low; it is explainable.

# 7. Minimal simulation and conceptual example

A first validation phase should remain simulation-based. Synthetic scenarios allow the model to be tested without reliance on sensitive operational data. A minimal experiment may begin with 1,000 synthetic orbital nodes distributed across low Earth orbit bands. Nodes include active payloads, inactive satellites, rocket bodies, large fragments and fragment-cloud abstractions. Edges are created when nodes share a region, approach within a threshold, influence a vulnerable asset or belong to the same propagation field.

At each timestep, the simulation updates region membership, uncertainty volumes and relations. It then recomputes edge tension, internal incoherence, A1-A6 classification and OTI by region. The output is not an autonomous command. The output is a ranked and explained decision map.

A conceptual example illustrates the difference between object size and relational importance. A large dead satellite in a sparse orbit may enter A5 because of latent fragmentation potential, but it may not produce high immediate OTI. A smaller fragment crossing a high-value corridor may enter A1 because of immediate relational tension. A diffuse cloud from an older fragmentation event may enter A6 because distributed propagation increases regional vulnerability even when no single object dominates the system. The decision architecture therefore separates immediate conjunction pressure, latent mass danger, fragmentation potential and regional cloud propagation.

Minimal pseudocode is shown below.

```
Input: graph G=(N,E), node states S_i, weights w_i and w_ij,
       lambda, gamma, alpha, region definitions R

for each timestep t:
    update orbital region membership and uncertainty volumes
    compute external edge tension T_ext over E
    compute internal incoherence T_int for each node
    T = T_ext + lambda * T_int

    for each node i:
        estimate gradient or local tension contribution
        candidate = S_i - gamma * grad_i
        projected = project_K(candidate)
        S_i_next = (1-alpha) * S_i + alpha * projected
        classify node relation into A1-A6

    compute OTI_R(t) for each orbital region R
    output ranked decision map and dominant tension explanations
```

A stronger second phase would increase scale to 5,000 and 10,000 synthetic nodes, test sensitivity to weighting schemes, compare A-regime assignments with expert judgment, and measure whether simulated interventions reduce OTI. Historical fragmentation scenarios and public catalog-derived approximations could later be used where legally and technically appropriate.

# 8. Relation to SSA, STM and active debris removal

VEHICLE-ODI is designed as a complementary architecture. Space situational awareness provides observation, catalogues, uncertainty estimates and object-state knowledge. Space traffic management provides coordination, operational procedures and collision-avoidance context. Active debris removal provides possible physical intervention against selected objects. ODI sits above and between these layers as a decision structure for prioritization.

The architecture should ingest, not replace, astrodynamic and sensor-derived information. It should use conjunction products, covariance information, object characteristics, region occupancy, mission value layers and debris environment models where available. Its contribution is to convert these inputs into a structural map of tension and regime classification.

This distinction is important for scientific positioning. ODI should not claim capabilities that require validated propagation or privileged sensor infrastructure. Instead, it focuses on a defensible research contribution: formalizing the prioritization problem and offering a graph-based, projection-governed architecture that can be tested first with synthetic scenarios and later with approved datasets.

# 9. Ethical and governance boundaries

Orbital debris intelligence is not only a technical problem. Debris objects are associated with states, companies, missions, liability frameworks, national security interests and international norms. Any decision-support architecture that ranks objects for observation, maneuver, stabilization or removal must therefore remain transparent about assumptions and limits.

VEHICLE-ODI should be governed by four principles. First, decision support must remain explainable: every priority should state which variables and regimes drive the result. Second, the system must distinguish scientific prioritization from legal authority: a high A-regime label is not permission to intervene. Third, the architecture should be auditable and reproducible in synthetic settings before real datasets are used. Fourth, it should support orbital safety, sustainability and coordination rather than unilateral enforcement.

The first stage should therefore remain simulation-based. Synthetic nodes allow researchers to test graph construction, regime classification, OTI behavior and sensitivity to assumptions without creating diplomatic or operational risk. Only after the model is validated should institutional partnerships consider approved data, legal review and operational pilots.

# 10. Testable hypotheses

The architecture can be converted into testable research hypotheses:

1. A graph-based representation of orbital debris can distinguish decision-relevant regimes that are not captured by object-level scalar scoring alone.
2. A combined external/internal tension model can identify different forms of priority, including immediate conjunction pressure, latent rigid-mass danger and diffuse cloud propagation.
3. A normalized OTI can detect regional stress changes across simulation time and can be decomposed into explainable A1-A6 contributors.
4. Projection-governed admissible action sets can reduce false interpretation by separating high tension from legal or physical permission to intervene.
5. Expert review of synthetic scenarios can evaluate whether A-regime classifications align with domain intuition and operational usefulness.

These hypotheses make the proposal falsifiable. If A-regimes fail to improve interpretability, if OTI is unstable under reasonable assumptions, or if expert review finds the taxonomy misleading, the architecture should be revised.

# 11. Limitations

VEHICLE-ODI is a conceptual and computational architecture, not a finished operational product. It does not replace sensor networks, catalogues, propagation models, conjunction assessment, maneuver planning, licensing, legal review or mission-specific engineering. Its present contribution is the formal organization of debris prioritization as a relational tension problem.

The proposed OTI requires calibration and may be sensitive to model weights, region definitions, covariance assumptions and value assignments. The A1-A6 taxonomy requires validation against expert judgment, simulated scenarios and historical cases. Without such validation, regime labels should be interpreted as research classifications rather than operational alerts.

The model must also avoid overstating intervention readiness. Active debris removal remains technically, legally, economically and diplomatically complex. ODI may help identify candidates and explain why they matter, but it does not by itself solve capture, ownership, liability or mission design.

# 12. Conclusion

VEHICLE-ODI proposes that the orbital debris problem should be read not only as a catalogue of objects but as a relational field under tension. The central question is not only how many objects exist or where they are, but which relations concentrate risk, which bodies carry latent fragmentation potential, which clouds propagate systemic vulnerability and which regions are drifting toward unacceptable structural stress.

By applying the Borda Milan Pyramid and the VEHICLE Formula-as-Architecture, ODI converts objects, fragments, debris clouds and orbital regions into structured nodes and relations. It introduces A1-A6 operational regimes and an experimental Orbital Tension Index to support prioritization before removal. The architecture is intentionally complementary: it does not replace SSA, STM, astrodynamics or ADR missions. It provides a decision layer for deciding what to observe, avoid, stabilize, move or remove first.

The next step is a synthetic simulation phase. Such a phase should test graph construction, A1-A6 classification, OTI behavior, sensitivity to parameters and comparison with expert prioritization. If validated, VEHICLE-ODI may contribute a useful language for orbital sustainability: structural decision intelligence before intervention.

# Statements

**Author contributions.** Roberto Borda Milan developed the VEHICLE-ODI concept, the Borda Milan Pyramid interpretation, the A1-A6 taxonomy and the manuscript.

**Conflict of interest.** The author declares no commercial or financial relationships that could be construed as a potential conflict of interest.

**Funding.** No external funding was received for this conceptual manuscript.

**Data availability.** No empirical dataset was analyzed in this manuscript. The proposed simulation phase is synthetic and should be implemented in future work with clearly documented assumptions and reproducible code.

**Ethics statement.** This manuscript proposes a decision-support architecture for orbital safety and sustainability. It does not propose autonomous intervention, unilateral enforcement or operational use without legal, institutional and technical review.

**Acknowledgments.** The author acknowledges the prior work of the international space debris research community, whose observation, modeling, mitigation and governance efforts make new decision architectures possible.

# References

Barry, K. (2022). Space debris mitigation and remediation: historical best practices and lessons learned for economically preserving and utilizing common areas. *New Space*, 10(3). doi: 10.1089/space.2021.0022.

European Space Agency. (2025). *ESA Space Environment Report 2025*. ESA Space Safety.

Inter-Agency Space Debris Coordination Committee. (2021). *IADC Space Debris Mitigation Guidelines*, IADC-02-01, Revision 3.

Kessler, D.J., and Cour-Palais, B.G. (1978). Collision frequency of artificial satellites: the creation of a debris belt. *Journal of Geophysical Research: Space Physics*, 83(A6), 2637-2646. doi: 10.1029/JA083iA06p02637.

Krisko, P.H. (2007). The predicted growth of the low-Earth orbit space debris environment: an assessment of future risk for spacecraft. *Proceedings of the Institution of Mechanical Engineers, Part G: Journal of Aerospace Engineering*, 221(6), 975-985. doi: 10.1243/09544100JAERO192.

Liou, J.-C., and Johnson, N.L. (2006). Risks in space from orbiting debris. *Science*, 311(5759), 340-341. doi: 10.1126/science.1121337.

Organisation for Economic Co-operation and Development. (2022). *Earth's Orbits at Risk: The Economics of Space Sustainability*. OECD Publishing.

VEHICLE Systems Lab. (2026). VEHICLE-ODI project page. Available at: https://vehiclesystemslab.com.