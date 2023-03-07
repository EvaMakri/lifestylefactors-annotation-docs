---
layout: entry
title: Documentation for Lifestyle Entities Annotation
---

## Annotation scope

The scope of this annotation is to detect lifestyle factor named entities in text. Below are some general examples of the guidelines that will be used in the annotation.

Definition for LSF to be added here:


## General guidelines

* Annotations should be made according to the annotator’s best understanding of the __author’s intended meaning in context__.  The attribute "LSF out of context" has been added for cases where the annotators judge that a term can appear as an LSF in text, but the intended meaning in context is not that of a Lifestyle factor.

* For a __Lifestyle_factor__ the following attributes can be selected (None of them, only one, or more if applicable)
  * Beauty and Cleaning    
  * Nutrition    
  * Drugs     
  * Environmental exposures     
  * Non physical leisure time activities    
  * Physical activity   
  * Sleep    
  * Socioeconomic factors   
  * Mental health practices   


### What to annotate:

There are two levels in the annotation process that the annotators should keep in mind. The first level is defining which terms to annotate and in which class they potentially belong too, so annotating an LSF named entity and deciding on which branch it belongs to, to add the proper attribute. The second level is which ones appear as LSFs in context and deciding whether the __"LSF out of context"__ attribute should be added as well.

* If an LSF is a part of non-LSF entity (e.g. _substance abuse_ in __substance abuse disorder__ or _chicken_ in __chicken embryo__ or _tobacco_ in __tobacco industry__), it should be annotated as LSF with the attribute: "LSF out of context".

* Top-level terms (e.g. nutrition) should be annotated.

* Standalone adjectives that are not part of named entities should not be annotated (e.g. nutritional, occupational etc).

* Chemical terms should be annotated as standalone entities, and “exposure” is not necessarily annotated as part of these named entities.

* Lifestyle factor names are annotated when they are part of hyphenated compound words (e.g. sleep-related) but NOT when they appear as a substring in a word not separated by a boundary such as a hyphen (e.g. asthmatic)

* Abbreviations are marked if the abbreviation stands for an LSF mention in scope of the annotation, but not if the full form merely includes an entity mention (e.g. in modifier position). For example, the F and D in FDA is not annotated despite it standing for food and drug.).

* Abbreviations should be annotated in all instances that they appear in a document

* Pregnancy, menopause and puberty are not annotated as LSFs.

* Chemicals should be annotated as LSF if they are common, or directly available for ingest as food/supplement, or exposure (even indirect). Examples:
  * sugar intake
  * concentrations of Vitamins A
  * Vitamin D supplements
  * serum Vitamin D levels
  * dioxins

* Chemicals should NOT be annotated as LSF if they are normally metabolized in the body. Examples:
  * HDL-cholesterol concentrations
  * serum Vitamin D 25-OH levels
  * fasting glucose

* Score/index score/index related to LSF can be annotated as LSF. Examples:
  * sleep quality score

* Do not annotate treatments as LSFs. The only form of treatment that is annotated is psychotherapy and entities related to it (e.g., CBT therapy) or treatments with a cosmetic effect (e.g. liposuction).

* Food names should be annotated only if the common taxonomic names (e.g. banana) are actual foods. The Linnean names (e.g. _Citrus sinensis_) should not be annotated. 

* Occupations should generally be annotated as Lifestyle Factors. 

* Sports and doing sports should generally be annotated and the attribute should be decided case-by-case.

* Different carcinogens should be annotated as Lifestyle Factors (e.g. "exposure to exhaust fumes"). 

* The actual word "carcinogen" should not be annotated.

* If an LSF is a part of another LSF, the left-longest match should be annotated

* _Energy content_ is a synonym for _caloric intake_ and should be annotated as __LSF__

* Terms like __comment toxicity__, __insult__, __threat__, and __identity attack__ are considered as LSFs in this annotation effort, as they are forms of __bullying__ which is a __Socioeconomic factor__ (describes interpersonal relationships)

* social media should be annotated as LSFs when they appear as standalone entities with a tag __"Non physical leisure time activities  "__, e.g. _Twitter_, but if they are not referring to the usage of these and the potential effect on human health (i.e. they are not discussed as LSFs), then they should receive an "LSF out of context" attribute.

* Entities that have an __"LSF out of context"__ attribute and an __"Environmental exposures"__, __"Non physical leisure time activities"__ or __"Physical activity "__ attribute will be removed from the final annotated corpus, as they are not expected to constitute LSFs on their own right. Specifically,  __"Non physical leisure time activities"__ and __"Physical activity "__ need an action to happen or at least be implied to be considered as Lifestyle Factors (e.g. __internet__ on each own is not an LSF, but __internet use__ is), while __"Environmental exposures"__ are only LSFs, if one is exposed to them, not necessarily as standalone entities (e.g. __acrylamide exposure__ is an LSF, but not __acrylamide__).


## To Discuss:
* cultural factors


For information on Annodoc, see <http://spyysalo.github.io/annodoc/>.
