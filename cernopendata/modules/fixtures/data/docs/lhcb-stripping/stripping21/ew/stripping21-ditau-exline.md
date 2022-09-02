[[stripping21 lines]](./stripping21-ew)

# StrippingDitau_EXLine

## Properties:

|                |                                                                                             |
|----------------|---------------------------------------------------------------------------------------------|
| OutputLocation | Phys/Ditau_EXLine/Particles                                                                 |
| Postscale      | 1.0000000                                                                                   |
| HLT            | HLT_PASS('Hlt2SingleTFElectronDecision') \| HLT_PASS('Hlt2SingleTFVHighPtElectronDecision') |
| Prescale       | 1.0000000                                                                                   |
| L0DU           | None                                                                                        |
| ODIN           | None                                                                                        |

## Filter sequence:

**CheckPV/checkPVmin1**

|        |     |
|--------|-----|
| MinPVs | 1   |
| MaxPVs | -1  |

**LoKi::VoidFilter/SelFilterPhys_StdAllNoPIDsElectrons_Particles**

|      |                                                                                              |
|------|----------------------------------------------------------------------------------------------|
| Code | CONTAINS('Phys/ [StdAllNoPIDsElectrons](./stripping21-stdallnopidselectrons) /Particles')\>0 |

**LoKi::VoidFilter/SelFilterPhys_StdAllNoPIDsPions_Particles**

|      |                                                                                      |
|------|--------------------------------------------------------------------------------------|
| Code | CONTAINS('Phys/ [StdAllNoPIDsPions](./stripping21-stdallnopidspions) /Particles')\>0 |

**CombineParticles/Ditau_EXLine**

|                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inputs           | [ 'Phys/ [StdAllNoPIDsElectrons](./stripping21-stdallnopidselectrons) ' , 'Phys/ [StdAllNoPIDsPions](./stripping21-stdallnopidspions) ' ]                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| DaughtersCuts    | { '' : 'ALL' , 'e+' : '(0.01 \< TRPCHI2) & (1.0 \> BPVIP()) & (2 \>= SUMCONE( 0.1, ONE, "Phys/StdAllNoPIDsPions")) & (10000.0 \< PT) & (0.7 \< E / ( E + SUMCONE( 0.5, E, "Phys/StdAllNoPIDsPions" ) ) ) & (20 \> TRCHI2DOF) & (50.0 \< PPINFO(LHCb.ProtoParticle.CaloPrsE,0)) & (0.1\*P \< PPINFO(LHCb.ProtoParticle.CaloEcalE,0)) & (0.05\*P \> PPINFO(LHCb.ProtoParticle.CaloHcalE,99999))' , 'e-' : '(0.01 \< TRPCHI2) & (1.0 \> BPVIP()) & (2 \>= SUMCONE( 0.1, ONE, "Phys/StdAllNoPIDsPions")) & (10000.0 \< PT) & (0.7 \< E / ( E + SUMCONE( 0.5, E, "Phys/StdAllNoPIDsPions" ) ) ) & (20 \> TRCHI2DOF) & (50.0 \< PPINFO(LHCb.ProtoParticle.CaloPrsE,0)) & (0.1\*P \< PPINFO(LHCb.ProtoParticle.CaloEcalE,0)) & (0.05\*P \> PPINFO(LHCb.ProtoParticle.CaloHcalE,99999))' , 'pi+' : '(0.01 \< TRPCHI2) & (1.0 \> BPVIP()) & (2 \>= SUMCONE( 0.1, ONE, "Phys/StdAllNoPIDsPions")) & (2000.0 \< PT) & (0.1 \< E / ( E + SUMCONE( 0.5, E, "Phys/StdAllNoPIDsPions" ) ) )' , 'pi-' : '(0.01 \< TRPCHI2) & (1.0 \> BPVIP()) & (2 \>= SUMCONE( 0.1, ONE, "Phys/StdAllNoPIDsPions")) & (2000.0 \< PT) & (0.1 \< E / ( E + SUMCONE( 0.5, E, "Phys/StdAllNoPIDsPions" ) ) )' } |
| CombinationCut   | (AALLSAMEBPV)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| MotherCut        | (8000.0 \< MM)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| DecayDescriptor  | [Z0 -\> e+ pi-]cc                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| DecayDescriptors | [ '[Z0 -\> e+ pi-]cc' ]                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Output           | Phys/Ditau_EXLine/Particles                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |