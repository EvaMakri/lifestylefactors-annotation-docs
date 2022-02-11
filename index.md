---
layout: entry
title: Documentation for Lifestyle Relation Annotation
---

## Annotation scope

The scope of this annotation is to detect lifestyle factors which affect the risk of disease onset and development. Below are some general examples of the guidelines that will be used in the annotation.

## General guidelines

* Annotations should be made according to the annotator’s best understanding of the __author’s intended meaning in context__. 
* Annotators should treat named entities as being __masked__, i.e. they shouldn't annotate relationships between entities just based on their names, when they would be unable to make the same annotations for two other entities.

### What to annotate:

1. Causal relationship: _LSF causes disease_ / _disease causes LSF_
Examples:
    * A __LSF__ causes a __disease__.
    * A __LSF__ is a recognized/reversible/know/common cause of a __disease__ 
    * A __disease__ is a result/side-effect of a __LSF__.
    * A __disease__ is attributed to / transmitted by / determined by a __LSF__.
    * A __disease__ survivors suffer from a __LSF__.


2. Statistically associated relationship: _LSF statistically associated with disease_. 
Examples:
    * A __LSF__ is associated with (a marked increase in risk for) a __disease__.
    * A __LSF__ incidence/carries a risk of a __disease__.
    * A __disease__ is characterized by a __LSF__.

    2.1 Positive statistical association:
    * A __LSF__ increases the risk of a __disease__.

    2.2 Negative statistical association:
    * A __LSF__ decreases the risk of a __disease__.
    * A __LSF__ used as defense for a __disease__. → implied risk reduction.
    * A __LSF__ could be critical in the current fight against __disease__.

3. Prevents relationship: _LSF prevents disease_ / _disease prevents LSF_
    * A __LSF__ is therefore imperative for preventing A __disease__ morbidity and mortality.
    * A __LSF__ is chemopreventive in a __disease__.

4. Therapeutic relationship: _LSF treats disease_.
    * The treatment of a __disease__ includes a __LSF__.
    * A __LSF__ is essential for treating a __disease__.
    * A __LSF__ is used for the therapy of a __disease__.

### What **NOT** to annotate:
1. Hypothetical statements: 

    “Here we study the link between LSF and disease”
2. Negative statements: 

    “A LSF is **not** associated with/**does not** increase the risk of disease”
<!-- 3. LSF is used for the **therapy** of disease. -->
3. No statistical significance: 

    “We **did not** find the relationship between LSF and disease to be statistically significant”

    _or_

    No statement about a correlation or statistical significance:
    
    “A majority percentage of HIV-positive MSM engage in unprotected sexual behavior”. → other individuals without HIV could have the same behavior → no statistical significance.

4. LSF that is a part of a bigger Named entity: sleep in multiple sleep latency test (MSLT)

### Special rules for relationships:
1. Across sentence boundaries should be annotated.
2. “Is believed” should be annotated.

    "Air pollutants are believed to induce or exacerbate a range of inflammatory diseases (atopic dermatitis..."
3. Expression like "limited evidence" should be annotated.

    "Results provide limited evidence for an association of early-life mobile source air pollution with childhood asthma incidence ..."
4. Animal experiments should be annotated, as they are supposed to be a model for a human disease.

5. Be careful with an occupation + a clause with LSFs. 

    In the following examples, farmers __should not__ be linked with acute lymphatic or chronic lymphatic leukemia. 

    "Farmers from major corn-producing, hog- and chicken-raising, and pesticide- and fertilizer-using counties tended to be at higher risk of acute lymphatic.

    "Farmers from counties with large cattle inventories and significant dairy activity were at higher risk of chronic lymphatic leukemia."

6. Annotate what the sentence says, even if there are contradictory statement. Example:
    
    Previous study shows A causes B… : annotate A Cause B.

    In contrast to the previous study, A causes C, or C causes B or no relation… : annotate either A causes C, C causes B or nothing

7. Mentions of “the X-Y association” between an LSF X and a disease Y should be annotated as statistically associated relationships.

1. Indirect relations annotated as positive.

2. Relationships like the following: 

    __LSF1__ and __LSF2__ when present together cause disease __disease__, but when __LSF1__ is present alone it **does not** cause __disease__.
    
    Annotate as _LSF1 causes disease_, _LSF2 causes disease_  and negative for LSF1.

### Special rules for entities:
1. Top-level terms (e.g. nutrition) should be annotated – even if relationships cannot be annotated for these terms.

8. Standalone adjectives that are not part of named entities should be blacklisted (e.g. nutritional, occupational etc).

9. Adjectives that are used to describe a disease, but are not part of the official nomenclature should not be annotated (e.g. for “occupational asthma” only the word “asthma” should be annotated as a disease) – following from rule 8.

10. Chemical terms should be annotated as standalone entities, and “exposure” should not be annotated as part of these named entities.

11. Lifestyle factor or disease names are annotated when they are part of hyphenated compound words (e.g. **asthma**-causing) but **NOT** when they appear as a substring in a word not separated by a boundary such as a hyphen (e.g. **asthma**tic)

12.	Abbreviations are marked if the abbreviation stands for a disease or an LSF mention in scope of the annotation, but not if the full form merely includes an entity mentio (e.g. in modifier position. For example, the A in OA is not annotated despite it standing for asthma. http://ann.turkunlp.org:8088/index.xhtml#/300_abstracts_Dec_2021/16304318?focus=345~369 )

13. (Temporary) Common chemicals that are directly available for ingest as food/supplement (e.g., sugar, vitamins, sodium benzoate), and harmful chemicals directly expose to people should be considered as LSFs. Chemical elements that are normally metabolized in the body, or used as a measurement (e.g., NO, glucose and cholesterol) should not be considered LSFs.



### Detailed guidelines

For information on Annodoc, see <http://spyysalo.github.io/annodoc/>.
