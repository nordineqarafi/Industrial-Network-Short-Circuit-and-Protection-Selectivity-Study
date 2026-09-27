# Methodology and engineering limits

## 1. Construct an equivalent network

Represent the upstream source, cables, transformers, and motor contributions at the relevant fault location. Keep resistive and reactive terms separate, then combine the path impedances at a common voltage base. For a transformer, the impedance must be referred to the side where the fault is evaluated by the square of the voltage ratio.

The report derives source impedance from the upstream short-circuit power, cable resistance from length and cross-section, cable reactance from its inductance, and transformer impedance from rated power and short-circuit voltage. A load-flow or ETAP project file is not present in this repository.

## 2. Calculate and cross-check fault levels

The report uses the IEC 60909 voltage-factor approach for the initial symmetrical three-phase short-circuit current:

\[ I''_{k3} = \frac{c U_n}{\sqrt{3}\,|Z_k|} \]

It also evaluates peak making current with a factor dependent on the equivalent resistance/reactance ratio. The calculation considers high fault levels for equipment ratings and low fault levels when checking whether a relay threshold will detect a fault. Results are compared with the ETAP values **reported in the reference material**.

## 3. Check equipment and relay coordination

Compare the calculated symmetrical and peak currents with device breaking and making ratings at the relevant voltage. The coordination exercise addresses instantaneous and delayed overcurrent stages (ANSI 50/51). Starting from downstream feeders, place upstream devices at higher current thresholds or longer operating times where the studied network allows it, accounting for breaker clearing times and margins.

The report describes a graded chain from motor feeder through distribution board to coupling. Exact feeder IDs and relay thresholds are intentionally retained only in the local PDF; they are neither generic recommendations nor independently validated setpoints.

## Evidence boundary

The supplied PDF is the only project artifact available here. It explicitly attributes many figures and numerical settings to a separate source document. This repository therefore describes the method and the reported findings, and does not imply that the ETAP simulation was recreated, that a live installation was changed, or that the figures are newly licensed for redistribution. For an engineering sign-off, independently verify the network input data, current revision of applicable standards, device curves and clearing times, and the original ETAP model.
