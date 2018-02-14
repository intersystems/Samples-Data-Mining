# Samples-Data-Mining
This is the README file for SAMPLES-DATA-MINING. 
The end of the file has setup instructions.
************************************************************************************
Use or operation of this code is subject to acceptance of the license available in the code 
repository for this code.
************************************************************************************
SAMPLES-DATA-MINING is meant for use with the InterSystems IRIS. It provides a copy of the 
Iris data set, which is well known in pattern recognition literature. You can use this data 
to explore the Predictive Model Markup Language (PMML) capability of InterSystems IRIS Data 
Platform. 

If you have a suitable license, you can also use this data with InterSystems IRIS Business Intelligence.

In addition to the data, the sample also includes various analytics model elements based on this data.

## Contents of the DataMining package
* `DataMining.IrisDataset` is the core class. This class defines the data set. See [this article](http://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=APMML). 
* `DataMining.PMML.Iris` defines a PMML model based on this data. See [this article](http://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=APMML). 
* `DataMining.IrisCube` is a cube definition based on the same data. To use this class, 
  you must have a license that includes analytics capabilities. 
* The classes in `DataMining.ClusterAnalysis` provide a demo and test for the Cluster Analysis 
  algorithms included as part of the InterSystems IRIS analytics capabilities. To use this class, 
  you must have a license that includes analytics capabilities. 

These classes all provide detailed descriptions, visible as part of the class reference.
After you have set up the sample, go to http://localhost:57772/csp/documatic/%25CSP.Documatic.cls

Replace `localhost` with the name of your InterSystems IRIS server instance, and replace 57772 with the
superserver port used by that instance.

## Setup instructions
1. Clone or [download](http://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=asamples) the repository.
2. If you have not yet created a namespace in InterSystems IRIS, follow the [detailed instructions](http://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=ASAMPLES_createns) to do so.
3. Open the InterSystems IRIS Terminal.
4. Enter the following command (replacing `mynamespace` with the namespace where you want to load the sample):
```
   ZN "mynamespace"
   ```
5. Enter the following commands (replacing with the full path of the `buildsample/buildsampledatamining.mac` file):
```
   do $system.OBJ.Load("full-path-to-buildsampledatamining.mac","ck")

   do ^buildsampledatamining
   ```
6. Then answer any prompts.

