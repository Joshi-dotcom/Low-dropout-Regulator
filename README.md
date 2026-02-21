---

## PMOS and NMOS LDO Architectures

The two primary LDO architectures differ in the choice of pass transistor: NMOS or PMOS.  
The block-level structures are shown below.

<p align="center">
<img src="docs/pmos_nmos_architecture.png" width="700">
</p>

Both architectures consist of:

- Error Amplifier (EA)
- Pass Transistor
- Feedback Network (R1, R2)
- Load (ZL)

The key distinction lies in the gate drive requirements and dropout behavior of the pass device.

---

## PMOS vs NMOS LDO Comparison

| Feature | PMOS LDO | NMOS LDO |
|----------|-----------|-----------|
| Pass Device | PMOS | NMOS |
| Dropout Mechanism | VSD(sat) limited | RDS(on) limited |
| Gate Drive Requirement | No charge pump required | Requires gate voltage > VIN |
| Loop Gain | Higher intrinsic gain | Moderate |
| Complexity | Moderate | Higher (gate boosting required) |
| Area | Larger | Smaller |
| Speed | Slower | Faster |
| Design Suitability | Low-power analog systems | High-current applications |

---

### Design Choice Justification

Although NMOS pass devices provide lower on-resistance and faster transient response, they require a boosted gate voltage to maintain low dropout operation. This typically necessitates a charge pump, increasing design complexity and power overhead.

A PMOS-based LDO avoids the need for gate boosting circuitry, simplifies implementation, and provides sufficient loop gain for stable regulation. For moderate load currents and low-power applications, PMOS offers a balanced trade-off between performance and implementation complexity.


**Author**
Joshita Meesala
