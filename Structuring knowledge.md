# Building a knowledge graph 

The first steps involve capturing high level concepts in your domain, like Findings, Procedures, Anatomic Structures, Health Care Sites.  Spreadsheets are the best way to wrangle your knowledge into a format that can be later loaded into a graph.  Spreadsheets allow you to organize a lot of information (knowledge) in one place;  they are an essential early step in building a knowledge graph. 

## Concept creation
## Procedures

### PROCEDURE LABELS
Labels must be human readable and make sense to a user from your domain. Use normal but orderly clinical language not "billing-ese".  But they should be consistent.

Get rid of 'Interventional Radiology' or any text that denotes concepts that don't describe the procedure.  Procedure should be only a combination of  "Process on Structure using Object"

  *"Reconstruction of...(structure).. using (.....) or whatever."*  
  *"Repair of...(structure).. using (.....) or whatever."*

**Laterality:** Is left/ right important to you?  If not (I don't use it) then consolidate / get rid of laterality. Including laterality could double your concept count. 

**Capitalization:** All labels capitalized first letter only.  

**Acronyms/ Abbreviations:** No abbreviations unless they are common acronyms (IV).  You can use both the string and the acronym so, when searching, either could be matched.  

  *"Fracture of zygomaticomaxillary complex ZMC"*

**Commas:** No commas, dashes, or hypens in labels (messes with .csv files).  Instead, use 
- ```semicolon ;```
- ```pipe |```
- ```underscore _```  

**uuri:**  unique uniform resource indicator.  Every concept in the graph has a uuri. each uuri is a random 10 character string of num/cap/lowercase. To get the random strings, use [random.org](https://www.random.org/strings/)

### GET SNOMED CONCEPTS

We want to create a separate snomedConcept for every proceduure (if an analogous SNOMED concept exists) because 
- browsing snomed gives you lots of new concepts
- its the terminology that the most other teminologies map to, so it becomes a key to other terminologies like CPT and ICD.

There are two kinds of relationships to SnomedConcept:  

```(:ProcedureArchetype)-[:equivalentTo]->(:SnomedConcept)```
- The vast majority of SNOMED concepts you save will have :equivalentTo relationships to your Procedure.  These should be **exact** matches.  If there is no exact match, that's not surprising.  Only about 60% of OMS procedures have an exact matching SNOMED concept.

```(:ProcedureArchetype)-[:relatedTo]->(:SnomedConcept)```

- Sometimes you will notice concepts that aren't equivalent, but are related. Saving these can be helpful for uploading old legacy data into the graph, if an exact match doesn't exist.

**Getting SNOMED concepts**
- Go to [SNOMED CT Intl Browser](http://browser.ihtsdotools.org/) and 'Go Browsing'. Find your concept by text matching or browsing parent / child concepts.  Once you find it, paste the ID and the label and the type of concept i.e. (procedure) into your spreadsheet.  

```71917006 | Repair of lip (procedure)```  

This should be a string that includes both the SCTID number the concept label and type.  While here, notice if there are any sibling/ parent/ child concepts that you would like to include as Procedures in your graph. 
