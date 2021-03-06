# Changelog

**2016-10-07** Cristian Baldenegro <c.baldenegro@cern.ch> / <crisx.baldenegro@gmail.com>

 * Added EFT for &gamma;&gamma; &rarr; AZ, according to Sylvain and Gero's computations.
   Datacard: `dataQED_AZanom`
 * In 2017-02-15 corrected the ME to include two operators which induce the Z&gamma; process.

**2016-09-23** Cristian Baldenegro <c.baldenegro@cern.ch> / <crisx.baldenegro@gmail.com>

 * Correction for &gamma;&gamma; &rarr; Spin2 &rarr; &gamma;&gamma; (-1 factor when calling `Mxxxx` matrix elements)
 * Couldn't run `dataQED_ZZanom` anymore; now it's corrected.

**2016-06-20** Cristian Baldenegro <c.baldenegro@cern.ch> / <crisx.baldenegro@gmail.com>

 * Exclusive &gamma;&gamma; &rarr;  HH (`IPROC=16071`) and &gamma;&gamma; &rarr; Dijet (`IPROC=16070`) were included
 * Matrix elements calculated by Gero von Gersdorff and Sylvain Fichet
 * Correspond to Datacards:  `dataQED_HHexoticSPin0EvenResonances` and `dataQED_GluGluexoticSpin0EvenResonances` respectively
 * New parameters (`F0H` and `F0G`)

**2016-05-20** Cristian Baldenegro <c.baldenegro@cern.ch> / <crisx.baldenegro@gmail.com>

 * Exclusive &gamma;&gamma; &rarr; ZZ (IPROC=16066) and &gamma;&gamma; &rarr; &gamma;Z (`IPROC=16068`)
 * Exclusive &gamma;&gamma; &rarr; W^+^W^-^ (IPROC=16067) and &gamma;&gamma; &rarr; &gamma;&gamma; (`IPROC=16069`) processes included
 * Helicity amplitudes from Gero von Gersdorff and Sylvain Fichet
 * Corresponding datacards:
    * `dataQED_ZZexoticSpin0EvenResonances` and `dataQED_AZexoticSpin0EvenResonances`
    * `dataQED_WWexoticSpin0EvenResonances` and `dataQED_AAexoticSpin2Resonances`
 * New parameters `F0Z` (1/coupling for &varphi; &rarr; ZZ), and `AF0ZG` (1/coupling for &varphi; &rarr; &gamma;Z)
 * New parameter `F0W` (1/coupling for &varphi; &rarr; W^+^W^-^)
 * Such exclusive productions are included in the same subroutine calling section as Matthias' (`AAANOM=3`, `AAEXOTIC=1`)

**2015-07-24** Matthias Saimpert <matthias.saimpert@cern.ch>

  * **Important bug corrections**: symmetry factor was omitted for &gamma;&gamma; &rarr; &gamma;&gamma;, now added. As a result, &gamma;&gamma; &rarr; &gamma;&gamma; xsec twice smaller

**2015-06-25** Matthias Saimpert <matthias.saimpert@cern.ch>

  * exclusive &gamma;&gamma; &rarr; &gamma;&gamma; studies, exotic spin 0-even resonance added
  * `IPROC=16065`, associated datacard, `dataQED_AAexoticSpin0EvenResonances`
  * new parameters `AAF0` (1/coupling), `AAW` (width const), `AAA2` (dumping factor for &radic;s dependence of the width)

**2015-01-20** Christophe Royon <christophe.royon@cern.ch>, Murilo Rangel <murilo.rangel@cern.ch>

  * correct for normalisation for reggeon (applied in PDFs and not in flux)
  
**2014-11-26** Christophe Royon <christophe.royon@cern.ch>

  * new code for heavy ion flux (`NFLUX=11`) 
  * new cards to transmit `BMIN`
  * new code and fluxes for proton ion, ion proton via Pom/Photon exchange 
  * bug fix for photon pom

**2014-09-11** Matthias Saimpert <matthias.saimpert@cern.ch>

  * Fix for &gamma;&gamma; &rarr; &gamma;&gamma;, high energy limit implemented (&radic;s &gg; m)
  * Final release for &gamma;&gamma; &rarr; &gamma;&gamma; :)

**2014-08-18** Matthias Saimpert <matthias.saimpert@cern.ch>

  * Anomalous &gamma;&gamma; &rarr; &gamma;&gamma; with compHEP routine found to be wrong (around a factor 2.1 too small)
  * Code from Gero and Sylvain replaced the compHEP routine, everything is now in agreement
  * Possibility to switch back to compHEP routine by commenting/uncommenting `fpmc.f l. 3435`
  * The new `EFT` routine takes interferences with SM &gamma;&gamma; production via W loop into account

**2014-03-20** Matthias Saimpert <matthias.saimpert@cern.ch>

  * General update/upgrade of the QED Diphoton exclusive process
  * `IPROC=16060`, SM QED Exc diphoton production (W + massive fermions loops included)
  * (old routine is `IPROC=19800` kept for comparison purpose but is most likely to be WRONG)
  * `IPROC=16061`, SM QED Exc diphoton production at high mass (massive fermion loops EXCLUDED)
  * `IPROC=16062`, SM QED  Exc diphoton production at low mass (W loop EXCLUDED)
  * `IPROC=16063`, General exotic vector contributions with SM interf (SM fermion loops EXCLUDED)
  * `IPROC=16064`, General exotic fermion contributions with SM interf (SM fermion EXCLUDED)
  * Corresponding datacards added

**2014-01-21** Christophe Royon <christophe.royon@cea.fr>

  * with Goergiy Stelmakh,
  * add Reggeon (`NFLUX=10`), Pomeron-Reggeon (`NFLUX=19`), Reggeon Pomeron (`NFLUX=21`)
  * Photon-Pomeron (`NFLUX=20`), Pomeron-Photon (`NFLUX=22`)

**2013-12-12** Matthias Saimpert <matthias.saimpert@cern.ch>

  * Adding &gamma;&gamma; &rarr; &gamma;&gamma; anomalous couplings (`IPROC=16016`) based on [arXiv:1311.6815 [hep-ph]](https://arxiv.org/abs/1311.6815)
  * Adding `~/External/comphep_interface/sqme_aaaa` folder
  * Modifications of `~/Examples/ffcard.`, `module.`, `module_reco.`, `fpmc_main.` and `Fpmc/fpmc`.

**2013-03-26** Oldrich Kepka <oldrich.kepka@cern.ch>

  * Adding `setup_lxplus.sh`, to be used on lxplus to configure CERNLIB

**2012-06-05** Rafal Staszewski

  * New `Examples/fpmc_main.f` created to supersede `module.f` and `module_reco.f`.
    `module` and `module_reco` are disabled in the Makefile.
    The new executable is called `fpmc`.
  * The information from jet alg. was not stored into ntuple.
    A change in `External/ntuple.f` was needed to fix it.
  * New `OUTPUT` option added to steering, determining the generator output.
    Possible values:

    * 0 : Only the text output with the cross section at the end.
    * 1 : Ntuple with few histograms and a list of particles for each event.
    * 2 : Jet CONE algorithm is performed and its output is also stored in the ntuple.

**2011-05-09**  Oldrich Kepka  <oldrich.kepka@cern.ch>

  * Tagging version `fpmc_v01-05`
  * cleanup of ntuples, version for testing 


