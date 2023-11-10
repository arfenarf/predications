This codebook.txt file was generated on 20180326 by Jake Vasilakes


-------------------
GENERAL INFORMATION
-------------------


1. Title of Dataset: Annotated Semantic Predications from SemMedDB.


2. Author Information


  Principal Investigator Contact Information
        Name: Rui Zhang
           Institution: University of Minnesota, Institute for Health Informatics and College of Pharmacy
           Address: 8-100 PWB, 516 Delaware St. SE, Minneapolis, MN 55455, USA
           Email: zhan1386@umn.edu


  Associate or Co-investigator Contact Information
        Name: Jake Vasilakes
           Institution: University of Minnesota, Institute for Health Informatics
           Address: 8-100 PWB, 516 Delaware St. SE, Minneapolis, MN 55455, USA
           Email: vasil024@umn.edu


  Associate or Co-investigator Contact Information
           Name: Rubina Rizvi
           Institution: University of Minnesota, Institute for Health Informatics and College of Pharmacy
           Address: 8-100 PWB, 516 Delaware St. SE, Minneapolis, MN 55455, USA
           Email: rizvi007@umn.edu


3. Date of data collection (single date, range, approximate date): 20180201


4. Geographic location of data collection (where was data collected?): Minneapolis, MN 55455


5. Information about funding sources that supported the collection of the data:
This research was supported by National Center for Complementary & Integrative Health Award (#R01AT009457) (Zhang),
the Agency for Healthcare Research & Quality grant (#1R01HS022085) (Melton),
and the National Center for Advancing Translational Science (#U01TR002062) (Liu/Pakhomov/Jiang).




--------------------------
SHARING/ACCESS INFORMATION
-------------------------- 


1. Licenses/restrictions placed on the data: None


2. Links to publications that cite or use the data: N/A. In submission.


3. Links to other publicly accessible locations of the data: None


4. Links/relationships to ancillary data sets: None


5. Was data derived from another source? Yes
           If yes, list source(s): SemMedDB ver 30 December 2016


6. Recommended citation for the data:




---------------------
DATA & FILE OVERVIEW
---------------------


1. File List
   A. Filename: annotated_predications.csv       
      Short description: 3000 annotated semantic predications from SemMedDB.

   B. Filename: README.txt
      Short description: This file.      


2. Relationship between files: README_substance_interactions.txt describes the metadata associated with substance_interactions.csv.




3. Additional related data collected that was not included in the current data package: None




4. Are there multiple versions of the dataset? No






--------------------------
METHODOLOGICAL INFORMATION
--------------------------


1. Description of methods used for collection/generation of data: 
1 million semantic predications were extracted from the SemMedDB ver 30 December 2016 release according to the following criteria:
(1) The predicate must be one of INTERACTS_WITH, STIMULATES, or INHIBITS, which specifically denote substance interactions;
(2) The subject and object entities of semantic predication must be a gene, drug, or dietary supplement according to the UMLS
semantic type of the entities.


2. Methods for processing the data: <describe how the submitted data were generated from the raw or collected data>
3000 of the 1 million predications were randomly selected for annotation, stratifying the selection to give equal
representation to drugs and dietary supplements in the subject and object position. Two expert annotators devised an annotation guideline and
established agreement by annotating the same subset of 200 predications. Once agreement was reached, they independently annotated the remaining 2800. 


3. Instrument- or software-specific information needed to interpret the data: None


4. Standards and calibration information, if appropriate: None


5. Environmental/experimental conditions: None


6. Describe any quality-assurance procedures performed on the data: Statistical tests were performed to ensure that the selected 3000
predications were a representative subsample of the initial 1 million. 


7. People involved with sample collection, processing, analysis and/or submission:
Jake Vasilakes (data collection, processing, annotation, and submission),
Rubina Rizvi (data annotation)





-----------------------------------------
DATA-SPECIFIC INFORMATION FOR: substance_interactions.csv
-----------------------------------------
<create sections for each dataset included>


1. Number of variables: 26


2. Number of cases/rows: 3000


3. Missing data codes: There is no missing data


4. Variable List

    Example. Name: Gender 
             Description: Gender of respondent
                    1 = Male
                    2 = Female
                    3 = Other                

    A. Name: PMID
       Description: The PubMed identifier of the citation to which the sentence belongs.

    B. Name: PREDICATE
       Description: The string representation of the predicate.
                    INTERACTS_WITH, STIMULATES, INHIBITS

    C. Name: INDICATOR_TYPE
       Description: The part of speech of the predicate, such as VERB for verbal predicates and NOM for nominalizations and other argument-taking nouns.
                    
    D. Name: PREDICATE_START_INDEX
       Description: The first character position (in the source document) of the text denoting the relation.
                    
    E. Name: PREDICATE_END_INDEX
       Description: The last character position (in the source document) of the text denoting the relation.
                    
    F. Name: SUBJECT_TEXT
       Description: The text that maps to the subject entity.
                    
    G. Name: SUBJECT_SEMTYPE
       Description: The UMLS semantic type of the subject entity.
                    
    H. Name: SUBJECT_START_INDEX
       Description: The first character position (in the source document) of the text denoting the subject entity. Note that this index is offset by the index of the
            start of the sentence in the source document, which was not available in this version of SemMedDB. Consequently, this index is not reconcilable
            with the sentence in the SENTENCE column.
                    
    I. Name: SUBJECT_END_INDEX
       Description: The last character position (in the source document) of the text denoting the subject entity. Note that this index is offset by the index of the
            start of the sentence in the source document, which was not available in this version of SemMedDB. Consequently, this index is not reconcilable
            with the sentence in the SENTENCE column.
                    
    J. Name: SUBJECT_SCORE
       Description: The confidence score of the mapping between the subject string and the subject concept.

    K. Name: SUBJECT_DIST
       Description: The distance of the subject mention (counted in noun phrases) from the predicate mention (0 for certain indicator types, such as NOM)

    L. Name: SUBJECT_MAXDIST
       Description: The number of potential arguments (in noun phrases) from the predicate mention in the direction of the subject mention
            (0 for certain indicator types, such as NOM)

    M. Name: SUBJECT_CUI
       Description: The UMLS CUI of the subject of the predication

    N. Name: SUBJECT_NOVELTY
       Description: The novelty score of the subject of the predication

    O. Name: OBJECT_TEXT
       Description: The text that maps to the object entity.
                    
    P. Name: OBJECT_SEMTYPE
       Description: The UMLS semantic type of the object entity.
                    
    Q. Name: OBJECT_START_INDEX
       Description: The first character position (in the source document) of the text denoting the object entity.
                    
    R. Name: OBJECT_END_INDEX
       Description: The last character position (in the source document) of the text denoting the object entity.
                    
    S. Name: OBJECT_SCORE
       Description: The confidence score of the mapping between the object string and the object concept.

    T. Name: OBJECT_DIST
       Description: The distance of the object mention (counted in noun phrases) from the predicate mention (0 for certain indicator types, such as NOM)

    U. Name: OBJECT_MAXDIST
       Description: The number of potential arguments (in noun phrases) from the predicate mention in the direction of the object mention
            (0 for certain indicator types, such as NOM)

    V. Name: OBJECT_CUI
       Description: The UMLS CUI of the object of the predication

    W. Name: OBJECT_NOVELTY
       Description: The novelty score of the object of the predication

    X. Name: TYPE
       Description: Whether the source sentence was taken from the title or the abstract.
            'ti': the title
            'ab': the abstract

    Y. Name: SENTENCE
       Description: The actual string or text of the sentence.

    Z. Name: LABEL
       Description: The annotated label of the semantic predication.
                'y': The semantic predication is correct (i.e. it is asserted in the sentence)
                'n': The semantic predication is incorrect (i.e. it is not asserted in the sentence)

