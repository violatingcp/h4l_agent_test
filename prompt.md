# Analysis Title: H=>4L Mass measurment with CMS Open Data 

# You are performing a Higgs boson measurement in the 4 lepton (electron or muon) decay channel using CMS Open Data from 2017 at √s = 13 TeV. The final state is 4 electrons or 4 muons or 2 electron s and 2 muons from a Z boson (on or off shell) decay that are loosely isolated, and ideally come from a Higgs boson decay. Your goal is to produce distributions of key observables — particularly the 4 lepton mass making a clean selection of Higgs events  — showing the Higgs signal contribution on top of Standard Model backgrounds, with this mass distribution we then ask that you perform a fit of the mass and compute the mu value. This loosely follows the official CMS publication (JHEP 11 (2017) 047, arxiv 1706.09936 in docs directory). Make sure that you the mass extraction code and the mu extraction fit code are easy to reproduce from this setup.   Lastly, for the fake muon background just use drell-yan+jets Monte Carlo, don't bother with a full fake rate esimtate. Also for lepton efficiency and trigger efficiency systematic uncertainties, I would not bother with them now. Just focus on getting the overall normalizations of the background with reasonable uncertatines, a good selection, and extraction of the mass and mu values. This should be a quick analysis, we don't need to be thorough in our review, so I would cut the exploration steps (step 1 and step 2) short, and get a fit and mass with a nice plot that you can put in the analysis note. Also the analysis note does not need to be as thorough as normal a note that is less than 20 pages is fine, we shoudl just try to get the main idea here. 

# Data source: flat ntuples produced with the script h4l_ntuplize.py that is run on NANOAOD from CMS open data
# Below we list the samples and their cross sections

#data_secret_10fb.root  2017 Data run at √s = 13 TeV with exactly 10/fb of integrated luminosity
#GluGluToHToZZ.root cross-section:0.00602392 pb fullname:GluGluHToZZTo4L_M125_TuneCP5_13TeV_powheg2_minloHJJ_JHUGenV7011_pythia8
#VBF_HToZZ.root   cross-section:0.00048794 pb      fullname:VBF_HToZZTo4L_M125_TuneCP5_13TeV_powheg2_JHUGenV7011_pythia8
#ZHToZZ.root      cross-section:0.000098394 pb     fullname:ZH_HToZZ_4LFilter_M125_TuneCP5_13TeV_powheg2-minlo-HZJ_JHUGenV7011_pythia8
#WPHToZZ.root     cross-section:0.0001072352 pb   fullname:WplusH_HToZZTo4L_M125_TuneCP5_13TeV_powheg2-minlo-HWJ_JHUGenV7011_pythia8
#WMHToZZ.root     cross-section:0.0000670716 pb     fullname:WminusH_HToZZTo4L_M125_TuneCP5_13TeV_powheg2-minlo-HWJ_JHUGenV7011_pythia8/NANOAODSIM/106X_mc2017_realistic_v9-v2
#ZZTo4L.root      cross-section:1.325e+00 pb      fullname:ZZTo4L_TuneCP5_13TeV_powheg_pythia8
#DYJetsToLL.root  cross-section:5.396e+03 pb      fullname:DYJetsToLL_M-50_TuneCP5_13TeV-madgraphMLM-pythia8
#TTBar.root       cross-section:5.270e+01 pb      fullname:TTJets_DiLept_TuneCP5_13TeV-madgraphMLM-pythia8
#GGZZ2E2Mu.root  cross-section:0.003185        fullname:GluGluToContinToZZTo2e2mu_TuneCP5_13TeV-mcfm701-pythia8
#GGZZ4E.root  cross-section:0.001575        fullname:GluGluToContinToZZTo4e_TuneCP5_13TeV-mcfm701-pythia8
#GGZZ4Mu.root  cross-section:0.001619        fullname:GluGluToContinToZZTo4mu_TuneCP5_13TeV-mcfm701-pythia8
