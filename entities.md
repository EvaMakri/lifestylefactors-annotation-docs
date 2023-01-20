---
layout: entry
title: Documentation for Lifestyle Entities Annotation
---

## Annotation scope

The scope of this annotation is to detect lifestyle factors which affect the risk of disease onset and development. Below are some general examples of the guidelines that will be used in the annotation.

## General guidelines

* Top-level terms (e.g. nutrition) should be annotated – even if relationships cannot be annotated for these terms.


* Standalone adjectives that are not part of named entities should be blacklisted (e.g. nutritional, occupational etc).


* Adjectives that are used to describe a disease, but are not part of the official nomenclature should not be annotated (e.g. for “occupational asthma” only the word “asthma” should be annotated as a disease).


* Chemical terms should be annotated as standalone entities, and “exposure” should not be annotated as part of these named entities.


* Lifestyle factor or disease names are annotated when they are part of hyphenated compound words (e.g. asthma-causing) but NOT when they appear as a substring in a word not separated by a boundary such as a hyphen (e.g. asthmatic)


* Abbreviations are marked if the abbreviation stands for a disease or an LSF mention in scope of the annotation, but not if the full form merely includes an entity mention (e.g. in modifier position. For example, the A in OA is not annotated despite it standing for asthma.)


* Pregnancy, menopause and puberty are not LSF.


* Chemicals should be annotated as LSF if they are common, or directly available for ingest as food/supplement, or exposure (even indirect). Examples:
  * sugar intake
  * concentrations of Vitamins A
  * Vitamin D supplements
  * serum Vitamin D levels
  * exposure to dioxins

* Chemicals should NOT be annotated as LSF if they are normally metabolized in the body. Examples:
  * HDL-cholesterol concentrations
  * serum Vitamin D 25-OH levels
  * fasting glucose

* Score/index related to diseases can be annotated as disease and score/index related to LSF can be annotated as LSF. Examples:
  * peripheral neuropathy score
  * sleep quality score

* Do not annotate all treatments. Only keep psychotherapy and entities related to it (e.g., CBT).




For information on Annodoc, see <http://spyysalo.github.io/annodoc/>.