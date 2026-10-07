# IsometricAnimation

Author of the combined integration: **Drishtant Kaushal**.

One skill for functional SVG objects, hover diagrams and hybrids. It combines rounded solids and a shared motion scheduler with projected screens, buttons, arithmetic, keyboard input and Web Audio. This is an adapted integration, not a byte-identical copy of either upstream project.

## Complete collection

[Open the collection](examples/index.html). It contains **46 working examples**: all 27 source figures, seven supplied skill showcases, two complete functional originals, ten recorded-object reconstructions. The earlier three smaller examples remain as authoring references.

The calculator retains decimals, percent, sign, deletion, chaining and its original layout. The synth retains the full white/black keyboard, four waveforms, octaves, chords and dragging. These now use shared motion and input. The video objects preserve the observed mechanisms through independently written models; their geometry is interpretive rather than pixel parity. The gallery labels that distinction.

[Eight automation references](skills/isometric-animation/references/inspiration.md) describe mechanisms beyond the videos, with concrete inputs, outputs and implementation judgments. Earlier gear and A* experiments were rejected and archived. Watch escapement, lens focus, convolution, signal decomposition, bicycle forces and hex navigation are research candidates.

## Modes

| Mode | Output | Rules |
| --- | --- | --- |
| object | Working calculators, typed displays, switches and instruments | Screen text and labels are allowed; controls produce actual output. |
| diagram | Hover explanations and exploded assemblies | No SVG labels or audio; identity comes from monochrome geometry; captions stay outside. |
| hybrid | Working controls with inspectable construction | Hover changes presentation; pressing changes functional state. |

All modes share one camera, rounded geometry, face transforms, stable rest-pose hit targets, one scheduler per stage and teardown. Light and dark themes are built in. Reduced motion lands geometry immediately while preserving functional input and audio. Rendering sleeps offscreen; an already playing sound is not stopped merely by scrolling.

## Use the skill

The installable folder is `skills/isometric-animation`, including its scripts, runtime, examples and this README. Copy that complete folder into your agent's skill directory, or install this directory as a local Claude Code plugin. Invoke `isometric-animation` and describe the object or diagram and what its controls should do.

From the package root:

```sh
node skills/isometric-animation/scripts/build.mjs skills/isometric-animation/examples/calculator.js examples/pocket-calculator.html
node skills/isometric-animation/scripts/validate.mjs examples/pocket-calculator.html
```

The builder writes portable HTML and a companion `README.md` with the distribution notices. Keep them together when sharing. It refuses to replace a different README in an existing output directory.

## Verification

Node 22 or later runs the build and static validation with no dependencies. Browser checks use the development dependency `playwright-core` and a locally installed Chrome browser.

```sh
npm ci
npm test
npm run build:examples
npm run build:catalog
node skills/isometric-animation/scripts/look.mjs skills/isometric-animation/examples/exploded-stack.js --target stack
```

Static validation checks runtime integrity, syntax, mode selection, lifecycle declarations, fixed input routing and obvious external dependencies. It is not a sandbox or a proof of visual correctness. Inspect the generated screenshots and test the actual output. The package tests exercise all three profiles, keyboard and pointer arithmetic, sound, dragging, simultaneous holds, focus loss, cancellation, reduced motion, extreme poses and remounting.

## Scope

This package implements SVG projection and interaction. It does not include a WebGL shader engine or claim to recreate an author's full article or unpublished gallery. The diagram profile uses the rounded silhouette vocabulary; object and hybrid profiles also allow the surface details needed for operation.

## Credits and provenance

- [ai-iso-skill](https://github.com/MrBongoC/ai-iso-skill), by **Tolga Cohce**, contributed the functional-object approach, face-local SVG projection and input/output patterns. Source snapshot `44b4da7714148eef547cc1b102e433472dfe3531`.
- [Hairline](https://github.com/lucasmarkes/hairline), by **Lucas Marques**, contributed the bundled geometry, spring/tween scheduler, lifecycle core and diagram rules. Source snapshot `bc782244216620434b14736df1d74daed2d05046`.

Drishtant Kaushal authored the integration profiles, projection adapter, unified input ownership, combined bench, builder, validator, recorded-object reconstructions and verification. The complete source figures, showcases and functional originals are adapted from the credited projects. Upstream copyrights remain with their respective authors. Project naming does not transfer those copyrights.


### Additional explanatory references


The rejected gear and pathfinding experiments were independently implemented, informed by [Gears](https://ciechanow.ski/gears/) by **Bartosz Ciechanowski** and [Introduction to A*](https://www.redblobgames.com/pathfinding/a-star/introduction.html) by **Amit Patel**. Research also reviewed Ciechanowski's [Mechanical Watch](https://ciechanow.ski/mechanical-watch/), [Cameras and Lenses](https://ciechanow.ski/cameras-and-lenses/) and [Bicycle](https://ciechanow.ski/bicycle/), Patel's [Hexagonal Grids](https://www.redblobgames.com/grids/hexagons/), [Circles, Sines and Signals](https://jackschaedler.github.io/circles-sines-signals/) by **Jack Schaedler**, and [Image Kernels](https://setosa.io/ev/image-kernels/) by **Victor Powell**. Their articles and illustrations are research references; their website code and graphics are not included in this package.

The ten recorded-object reconstructions are based on the user's supplied gallery recording. Its source implementation and author identity are unverified. The source screenshots show **@wheresryan22**; no identity relationship with either repository author is assumed.

## MIT license for the integration

MIT License

Copyright (c) 2026 Drishtant Kaushal

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Upstream MIT notice: ai-iso-skill

MIT License

Copyright (c) 2026 Tolga Cohce

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Upstream MIT notice: Hairline

MIT License

Copyright (c) 2026 Lucas Marques

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
