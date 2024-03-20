---
layout: entry
title: Documentation for Disease-Lifestyle Relations Annotation
---

## Annotation scope

The scope of this annotation is to detect lifestyle factors which affect the risk of disease onset and development. Below are some general examples of the guidelines that will be used in the annotation.

## General guidelines

* Annotations should be made according to the annotator’s best understanding of the __author’s intended meaning in context__. 
* Annotators should treat named entities as being __masked__, i.e. they shouldn't annotate relationships between entities just based on their names, when they would be unable to make the same annotations for two other entities.

### What to annotate:

1. Causal relationship: _LSF causes disease_ / _disease causes LSF_.
Examples:
    * A __LSF__ causes a __disease__.
    * A __LSF__  contributes to the development of a __disease__.  
    * A __LSF__  developed a __disease__.
    * A __LSF__ is a recognized/reversible/know/common cause of a __disease__
    * __LSF__-induced __DIS__
    * A __LSF__ may induce a __DIS__.
    * A __LSF__ increases a __disease__ mortality.
    * A __disease__ is a result/side-effect of a __LSF__.
    * A __disease__ is attributed to / transmitted by / determined by a __LSF__.
    * The consequences of a __LSF__ is a __disease__.

2. Statistically associated relationship: _LSF is statistically associated with disease_. 
Examples:
    * A __LSF__ is associated with a __disease__.
    * A __LSF__ is associated with the risk of a __disease__.

    2.1 Positive statistical association:
      * A __LSF__ increases the risk of a __disease__.
      * A __LSF__ is the risk factor a __disease__.
      * A __LSF__ carries a risk of a __disease__.
      * A __LSF__ is a predictor of a __disease__.
      * A __disease__ is characterized by a __LSF__.
      * survivors/patients with __disease__ were more had/likely to be __LSF__.
      * A __LSF__ increases incidence of a __disease__.
      * A __LSF__ increases prevalence of a __disease__. But prevalence without any statistical significance testing should not be annotated.
      * A __LSF__ contributes to the burden of a __disease__.
      *  A __LSF__ should be considered during risk stratification for a __disease__



    2.2 Negative statistical association:
      * A __LSF__ decreases the risk of a __disease__.
      * A __LSF__ decreases incidence of a __disease__.
      * A __LSF__ decreases prevalence of a __disease__.
      * A __LSF__ could be critical in the current fight against __disease__.
      * A __LSF__ is inversely associated with a __disease__.
      
3. Controls: _LSF controls disease_. Examples:
    * A __LSF__ play a regulatory role in __disease__.
    * A __LSF__ has beneficial effect for the control of __disease__. 
    * A __LSF__ is associated with __disease__ treatment and control.
    * A __LSF__ decreases/reduces/attentuates __disease__ (not the prevalence of __disease__).

    3.1 Prevents relationship: _LSF prevents disease_ / _disease prevents LSF_. Examples:
     * A __LSF__ is therefore imperative for preventing a __disease__ morbidity and mortality.
     * A __LSF__ is chemopreventive in a __disease__.
     * A __LSF__ is protected against a __disease__.
     * A __LSF__ reduce a __disease__ mortality.
     * A __LSF__ used as defense for a __disease__.

    3.2 Therapeutic relationship: _LSF treats disease_.
    Examples:
     * The treatment of a __disease__ includes a __LSF__.
     * A __LSF__ is essential for treating a __disease__.
     * A __LSF__ is used for the therapy of a __disease__.
     * The efficacy of a __LSF__  in a __disease__.
     * A __LSF__ is the relief of a __disease__.
     * A __LSF__ is was effective in a __disease__.
     * A __disease__ were eliminated by a __LSF__.
     * A __disease__ were improved after (using) a __LSF__.

4. No statistical association: _LSF is not associated with disease_. Examples:
    * A __LSF__ is **not** associated with a __disease__.
    * There is no association between __LSF__ and __disease__.

### What **NOT** to annotate:
1. Hypothetical statements: 

    “Here we study the link between LSF and disease”
    "It is possible to suspect a relationship between ESRD and insecticides or pesticides.
    "LSF might be involved". -> Take context into consideration.
   
3. No statistical significance but tendency: 

    “We **did not** find the relationship between LSF and disease to be statistically significant” / "There is an association between __LSF__ and __disease__, but **no significance**".

    _or_

    No statement about a correlation or statistical significance:
    
    “A majority percentage of HIV-positive MSM engage in unprotected sexual behavior”. → other individuals without HIV could have the same behavior.
    "LSF1 treated Disease in 4 individuals and LSF2 caused Disease in 7 individuals". -> do not annotate anything.

    _or_

    Observation:

    “Cannabis is the most widely used illicit substance in the United States with especially high prevalence of use among those with psychiatric disorders.”
   
    _or_
   
   Prevalence mentions:

   Do not annotate differences in prevalence (either as % or as number of people or as mentioned in text) unless statistical significance is mentioned (aka a statistical test is performed). 

4. LSF that is a part of a bigger Named entity: sleep in multiple sleep latency test (MSLT)
5. Do NOT annotate "... in/among LSF/DIS":

    __Dairy farmers__ is not part of relation: Among __dairy farmers__, moreover, __lung cancer__ SMRs showed a significant downward trend across the quartiles of increasing __length of work__.

6. Statistical associations should not be annotated if p-value is greater than 0.05.
7. Statistical associations should not be annotated if CI encompasses 1.0. (23391765)

   "An increase of 10 mug/m(3) of 2-day moving average concentrations of sulfur dioxide and nitrogen dioxide corresponded to 0.54% (95% posterior intervals, 0.28-0.81) and 0.88% (95% posterior intervals, 0.54-1.22) increase of stroke mortality".

### Special rules for relationships:
1. Across sentence boundaries should be annotated.
2. “Is believed” should be annotated.

    "Air pollutants are believed to induce or exacerbate a range of inflammatory diseases (atopic dermatitis..."
3. In cases where "Limited/Weak/Poor/Little evidence" is mentioned: Judge the author’s intention: If the author makes you understand that the evidence is inadequate, do not annotate. In the opposite case, annotate. However, do not annotate when there are mentions of inconsistent evidence.

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

1. Indirect relations should be annotated. However, in cases like “__LSF__ was not independently associated with __disease__” do not annotate unless it specifically mentions that the LSF was dependently associated.


2. Relationships like the following: 

    __LSF1__ and __LSF2__ when present together cause disease __disease__, but when __LSF1__ is present alone it **does not** cause __disease__.
    
    Annotate as _LSF1 causes disease_, _LSF2 causes disease_ (for the first sentence) and no annotations between LSF1 and disease in the second sentence.


4. Compared/comparison: a) if the comparison is between LSF/not having LSF or Dis/not having Dis then annotate only LSF to Dis with the appropriate relationship (not the not-LSF or not-Dis).

   "The seizure rate was significantly higher in cocaine users (37 [26%] of 142 patients) than in non-cocaine users (151 [15.2%] of 992 patients, p = 0.001).
   
   b) if the comparison is between separate things (eg one type of cancer to another) then annotate based on the direction you would assume could be applied in comparison to not having Dis or do not annotate at all if assuming is not possible.

   "The proportion of patients working in professions with exposures to known carcinogens was 33.5% for lung cancer, and 17.1% for large bowel cancer (p=0.000)".

6. Annotate relationships even when they are not independent.
7. Also consider numbers in ORs, HRs, RRs for the direction of the association, even if not specifically written in words as “positive” or “negative” (eg OR>1 means positive association and OR<1 means negative association).
   
   "__SO2__ was also significantly associated with __birth defects__ in the second month before the pregnancy (aOR = 1.31; 95% CI: 1.20 ~ 3.22)."
8. Annotate LSF and Disease mortality associations in as LSF and Disease.



### Special rules for entities:
1. Top-level terms (e.g. nutrition) should be annotated – even if relationships cannot be annotated for these terms.

8. Standalone adjectives that are not part of named entities should be blacklisted (e.g. nutritional, occupational etc).

9. Adjectives that are used to describe a disease, but are not part of the official nomenclature should not be annotated (e.g. for “occupational asthma” only the word “asthma” should be annotated as a disease) – following from rule 2.

10. Chemical terms should be annotated as standalone entities, and “exposure” should not be annotated as part of these named entities.

11. Lifestyle factor or disease names are annotated when they are part of hyphenated compound words (e.g. **asthma**-causing) but **NOT** when they appear as a substring in a word not separated by a boundary such as a hyphen (e.g. **asthma**tic)

12. Abbreviations are marked if the abbreviation stands for a disease or an LSF mention in scope of the annotation, but not if the full form merely includes an entity mention (e.g. in modifier position. For example, the A in OA is not annotated despite it standing for asthma.)

13. Pregnancy, menopause and puberty are not LSF.

14. Chemicals should be annotated as LSF if they are common, or directly available for ingest as food/supplement, or exposure (even indirect). Examples:
    * sugar intake
    * concentrations of Vitamins A
    * Vitamin D supplements
    * serum Vitamin D levels
    * exposure to dioxins
   
15. Chemicals should NOT be annotated as LSF if they are normally metabolized in the body. Examples:
    * HDL-cholesterol concentrations
    * serum Vitamin D 25-OH levels
    * fasting glucose
   
16. Score/index related to diseases can be annotated as disease and score/index related to LSF can be annotated as LSF. Examples:
    * peripheral neuropathy score
    * sleep quality score

17. Do not annotate all treatments. Only keep psychotherapy and entities related to it (e.g., CBT).
   



### Detailed guidelines

For information on Annodoc, see <http://spyysalo.github.io/annodoc/>.
