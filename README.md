# NostaJig PS3

![License](https://img.shields.io/badge/license-NC%20%2F%20Credit%20Required-red)
![Material](https://img.shields.io/badge/material-1.5mm%20Steel-lightgrey)
![Platform](https://img.shields.io/badge/platform-PS3%20Fat%20%2F%20Slim-blue)
![Format](https://img.shields.io/badge/format-STP-yellow)
![Rework](https://img.shields.io/badge/rework-BGA%20%2F%20RSX-green)

![NostaJig PS3](assets/99.jpeg)


> A PS3 BGA rework jig designed to prevent board flex and 21 20 errors during RSX reflow.

![NostaJig PS3](assets/1.png)

---

## The Problem

The PS3JIGV2wtf_Are_calipers is widely used for PS3 BGA rework. It has a structural flaw.

At the board clamping section, the jig narrows to a thin strip. Under reflow
temperatures this section deflects, pulling the board down at the RSX footprint
during soak and reflow. The result is lifted solder balls at the BGA perimeter -
on boards that were fine going in.

This manifests as Syscon error **21 20** after rework. The jig caused it.

![PS3JIGV2wtf_Are_calipers - thin section that warps](assets/3.png)
*PS3JIGV2wtf_Are_calipers - the thin section at the board edge deflects under heat*

---

## NostaJig PS3

Designed from scratch to eliminate warp-induced board flex and shield the
capacitor zone near the Cell during RSX rework.

![NEC/TOKIN shielding zone](assets/2.png)
*The cutout geometry shields the NEC/TOKIN capacitor area from direct heater exposure*

### Improvements over PS3JIGV2wtf_Are_calipers

| | PS3JIGV2wtf_Are_calipers | NostaJig PS3 |
|---|---|---|
| Warp under reflow temps | Present | Eliminated |
| Board edge clamping stability | Marginal | Reinforced |
| Cell / NEC-TOKIN zone shielding | None | Integrated |
| RSX ball lift risk | Real | Significantly reduced |

### Specs

- Material: 1.5 mm steel
- Two-part design - top plate and support frame
- Triangulated cutout geometry for thermal expansion distribution
- Compatible with standard IR/hot-air rework station beds (Honton HT-490 and similar)

---

## Files

`PS3JIG_CALIPERS_ARE_BETTER.stp` - send it wherever you want. Local laser cutter,
online sheet metal service, whatever. 1.5 mm steel, no special finish required.

---

## Usage

1. Place the bottom support frame on the rework station bed
2. Seat the PS3 mainboard, component side up
3. Apply the top plate, align to board edges
4. Clamp per your station's procedure
5. Run your RSX reflow profile as normal

![NostaJig PS3 mounted in rework station](assets/4.png)
*Seated in the Honton HT-490 - board held flat across the full RSX footprint*

---

## Background

After tracing enough post-rework 21 20 errors back to jig flex rather than
the reflow profile, this was built to remove that variable. The board needs
to stay flat.

---

## License

Personal and non-commercial use only.
You may not sell this design or manufactured parts derived from it.
If you share, modify, or redistribute this design in any form,
you must credit NostaMods and link back to this repository.

---

*NostaMods - [github.com/jw0710](https://github.com/jw0710)*
