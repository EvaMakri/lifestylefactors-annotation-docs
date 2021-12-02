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

1. Causal relationship: _LSF causes disease_.
Examples:
    * A __LSF__ causes the __disease__.
    * A __LSF__ is a recognized/reversible/know/common cause of a __disease__ 
    * A __disease__ is a result/side-effect of a __LSF__.
    * A __disease__ is attributed to / transmitted by / determined by a __LSF__.

2. Statistically associated relationship: _LSF statistically associated with disease_. 
Examples:
    * A __LSF__ decreases/increases/carries a risk or incidence of a __disease__.
    * A __LSF__ is associated with (a marked increase in risk for) a __disease__.
    * A __LSF__ used as defense for a __disease__. → implied risk reduction.

### What **NOT** to annotate:
1. Hypothetical statements: 

    “Here we study the link between LSF and disease”
2. Negative statements: 

    “LSF is **not** associated with/**does not** increase the risk of disease”
3. LSF is used for the **therapy** of disease.
4. No statistical significance: 

    “We **did not** find the relationship between LSF and disease to be statistically significant”

    _or_

    No statement about a correlation or statistical significance:
    
    “A majority percentage of HIV-positive MSM engage in unprotected sexual behavior”. → other individuals without HIV could have the same behavior → no statistical significance.

5. LSF that is a part of a bigger Named entity: sleep in multiple sleep latency test (MSLT)

### NB!
1. Indirect relations annotated as positive.
2. Relationships like the following: 

    __LSF1__ and __LSF2__ when present together cause disease __disease__, but when __LSF1__ is present alone it **does not** cause __disease__.
    
    Annotate as _LSF1 causes disease_, _LSF2 causes disease_  and negative for LSF1.


### Detailed guidelines

For information on Annodoc, see <http://spyysalo.github.io/annodoc/>.
