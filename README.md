## validateIt: An R Package for Topic and Label Validation

This is forked from Luwei's Github page: https://github.com/Luwei-Ying/validateIt. 

Previously, the file directory had looked like this: 

```
validateIt
│   README.md
│   NAMESPACE
│   DESCRIPTION
│
└───R
│   │   checkAgree.R
│   │   combMass.R
│   │   ...
│   
└───man
│   │   checkAgree.Rd
│   │   combMass.Rd
│   │   ...
│    
└───tests
│   │   testthat.R
│   └───testthat
│       │   testcombMass.R
│       │   testevalResults.R
│       │   ...   
└───data
    │   allR4WSItasktest.rda
    │   goldR4WSItest.rda
    │   ...
    
```

Now it looks like this: 

```
validateIt
│   README.md
│   NAMESPACE
│   DESCRIPTION
│
└───R
│   │   checkAgree.R
│   │   combMass.R
│   │   ...
│   
└───man
│   │   checkAgree.Rd
│   │   combMass.Rd
│   │   ...
│
└───tests
    │   testthat.R
    └───testthat
    │   │   testcombMass.R
    │   │   testevalResults.R
    │   │   ...
    └───testdata
        │   allR4WSItasktest.rda
        │   goldR4WSItest.rda
        │   ...
    
```

Previously, all test files started by loading datasets from the /data folder using lines like this: 
```
load("../../data/modtest.rda")
```

Because the directory has changed, the lines need to be replaced with something like this: 
```
load("../testdata/modtest.rda")
```
