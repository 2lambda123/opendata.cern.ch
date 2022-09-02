[[stripping21r1p2 lines]](./stripping21r1p2-commonparticles)

# StdLooseDetachedKpi

**CombineParticles/StdLooseDetachedKpi**

|                  |                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Inputs           | ['Phys/ [StdLooseKaons](./stripping21r1p2-stdloosekaons) /Particles', 'Phys/ [StdLoosePions](./stripping21r1p2-stdloosepions) /Particles'] |
| DaughtersCuts    | {}                                                                                                                                           |
| CombinationCut   | (AM\<2.2\*GeV) & (ADOCACHI2CUT(30, ''))                                                                                                      |
| MotherCut        | (VFASPF(VCHI2)\<25)                                                                                                                          |
| DecayDescriptor  | [K\*(892)0 -\> K+ pi-]cc                                                                                                                   |
| DecayDescriptors | []                                                                                                                                         |
| Output           | None                                                                                                                                         |