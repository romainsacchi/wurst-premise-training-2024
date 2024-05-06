# exercise-car-europe ![GitHub release (latest by date)](https://img.shields.io/github/v/release/premise-community-scenarios/scenario-example-bread) [![DOI](https://zenodo.org/badge/496564841.svg)](https://zenodo.org/badge/latestdoi/496564841)


Description
-----------

This is an example of a repository containing a custom prospective scenario for analysing the environmental
impacts of the future European car fleet.

Sourced from publication
------------------------

None

Data validation 
---------------

None

Test 
----

GitHubAction ![example workflow](https://github.com/premise-community-scenarios/exercise-car-europe/actions/workflows/main.yml/badge.svg?branch=main)


Ecoinvent database compatibility
--------------------------------

ecoinvent 3.9.1 cut-off

IAM scenario compatibility
---------------------------

Compatible with the following IAM scenarios:
* IMAGE SSP2-Base
* IMAGE SSP2-RCP26

How to use it?
--------------

```python

    import brightway2 as bw
    from premise import NewDatabase
    from datapackage import Package
    
    
    fp = r"https://raw.githubusercontent.com/romainsacchi/exercise-car-europe/main/datapackage.json"
    cars_scenario = Package(fp)
    
    bw.projects.set_current("your_bw_project")
    
    ndb = NewDatabase(
            scenarios = [
                {"model":"image", "pathway":"SSP2-Base", "year":2050,},
                {"model":"image", "pathway":"SSP2-RCP26", "year":2030,},
            ],        
            source_db="ecoinvent 3.9.1 cutoff",
            source_version="3.9",
            key='xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx',
            external_scenarios=[
                cars_scenario, # <-- list datapackage objects here
            ] 
        )
    
    ndb.update_external_scenario()
```

