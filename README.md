# Correlations


Correlations child8: (LHC17l ): 

We should get several lines saying: Received Number collisions.

We get as many lines as Data Frames the input file contains.


https://alimonitor.cern.ch/catalogue/#/alice/data/2017/LHC17l/000277907/pass2/PWGZZ/Run3_Conversion/316_20220630-0042_child_8

https://alimonitor.cern.ch/catalogue/#/alice/data/2017/LHC17l/000277907/pass2/PWGZZ/Run3_Conversion/316_20220630-0042_child_8

https://alimonitor.cern.ch/catalogue/#/alice/data/2017/LHC17l/000277907/pass2/PWGZZ/Run3_Conversion/316_20220630-0042_child_8

https://alimonitor.cern.ch/catalogue/#/alice/cern.ch/user/v/vvalenci

/alice/data/2017/LHC17l/000277907/pass2/PWGZZ/Run3_Conversion/316_20220630-0042_child_8/AOD/046

Command to execute:

1)
o2-analysis-cf-firstcfcorr | o2-analysis-collision-converter --aod-file AO2D_316_20220630-0042_child_8_AOD_046.root  > execution.log

2)
o2-analysis-cf-firstcfcorr --aod-file AO2D_316_20220630-0042_child_8_AOD_046.root | o2-analysis-collision-converter | o2-analysis-centrality-table | > execution.log o2-analysis-multiplicity-table | o2-analysis-timestamp  | o2-analysis-event-selection  | o2-analysis-zdc-converter 

3)(both works..)
o2-analysis-cf-firstcfcorr -b --configuration json://handsonconfig.json | o2-analysis-collision-converter -b --configuration json://handsonconfig.json | o2-analysis-centrality-table -b --configuration json://handsonconfig.json | o2-analysis-multiplicity-table -b --configuration json://handsonconfig.json | o2-analysis-timestamp -b --configuration json://handsonconfig.json | o2-analysis-trackselection -b --configuration json://handsonconfig.json | o2-analysis-trackextension -b --configuration json://handsonconfig.json | o2-analysis-zdc-converter  -b --configuration json://handsonconfig.json | o2-analysis-event-selection -b --configuration json://handsonconfig.json > execution.log

o2-analysis-cf-firstcfcorr --configuration json://handsonconfig.json | o2-analysis-collision-converter --configuration json://handsonconfig.json | o2-analysis-centrality-table --configuration json://handsonconfig.json | o2-analysis-multiplicity-table --configuration json://handsonconfig.json | o2-analysis-timestamp --configuration json://handsonconfig.json | o2-analysis-trackselection --configuration json://handsonconfig.json | o2-analysis-trackextension --configuration json://handsonconfig.json | o2-analysis-zdc-converter  --configuration json://handsonconfig.json | o2-analysis-event-selection --configuration json://handsonconfig.json





//ancien auto o2 correlations

o2-analysistutorial-corr --aod-file AO2D-LHC21k6-1.root --configuration json://corr.json | o2-analysis-collision-converter | o2-analysis-multiplicity-table  | o2-analysis-event-selection | o2-analysis-track-propagation > execution.log

Correlations Generic Framework:
https://github.com/AliceO2Group/analysis-tutorials/tree/master/o2at-2/PWGCF/GenericFramework/src



////////////

o2-analysis-cf-flow-gfw-tutorial --aod-file AO2D.root --configuration json://handsonconfig.json | o2-analysis-centrality-table --configuration json://handsonconfig.json | o2-analysis-multiplicity-table --configuration json://handsonconfig.json | o2-analysis-timestamp --configuration json://handsonconfig.json | o2-analysis-trackselection --configuration json://handsonconfig.json | o2-analysis-trackextension --configuration json://handsonconfig.json | o2-analysis-zdc-converter  --configuration json://handsonconfig.json | o2-analysis-event-selection --configuration json://handsonconfig.json

o2-analysis-cf-flow-gfw-tutorial --aod-file AO2D_run3.root --configuration json://handsonconfig.json | o2-analysis-centrality-table --configuration json://handsonconfig.json | o2-analysis-multiplicity-table --configuration json://handsonconfig.json | o2-analysis-timestamp --configuration json://handsonconfig.json | o2-analysis-trackselection --configuration json://handsonconfig.json | o2-analysis-trackextension --configuration json://handsonconfig.json | o2-analysis-zdc-converter  --configuration json://handsonconfig.json | o2-analysis-event-selection --configuration json://handsonconfig.json

Good Flow (only working for run3…):

 [O2Physics/latest ninja/latest] ~/Desktop/correlations_files/flow %> sh run.sh run3