---
layout: post
title: "PBP Correct-a-thon Besançon #2: the case of BM Besançon Ms 5"
subtitle: HTR for Paris Bibles at Besançon
gh-repo: daattali/beautiful-jekyll
tags: [Correct-a-thon , Besançon]
comments: false
---
<base target="_blank">


# **PBP Correct-a-thon Besançon: BM Besançon Ms 5**
<br>
<p>
<img src="/assets/PBP_MS5_Bibles.png" style="zoom:100%;" /> 
<br>
Fig. 1. Ms 5 of the Bibliothèque Municipale de Besançon
</p>
  <br>
<br>

## Introduction

This blogpost was written in the context of the Paris Bible Challenge which took place in Besançon, France in January 2023. 

In this post, we intend to describe the revision process of the automatically generated transcriptions of two text columns in  Besançon Ms 5. These transcriptions were obtained through the application of the Paris Bible Project model for Tranksribus (PBP 2.1) 

<br>
<p>
<img src="/assets/PBP_MS5_Bible.png" style="zoom:100%;" /> 
<br>
Fig. 2. Photo by David Joseph Wrisley
  </p>
<br>
<br>

## Physical description of the BM Besançon Ms 5

The pages we transcribed came from a Bible held by the Besançon Municipal Library, described in the catalog as  *Ms 5 - Biblia sacra, ex translatine S. Hieronymi, cum epistola ad Paulinum, prologhi et capitulis*. It is a rather large volume 369x260mm, with a weight close to 4 kilograms. The cover and the later binding is in leather on wooden boards sealed with bolts (some of which are missing on the upper board), in a rather degraded condition.The manuscript's vellum, uneven in their original density, is somewhat warped, giving a wavy appearance to the book's spine. It is certainly these deformations that have caused the distortion of the text lines over time. We started to transcribe page 9, at  the beginning of Genesis. This page is characterized by a rubric, an inscription in red characters at the beginning of the text. This is followed by a long illumination made for the Lettrine of the first sentence, *Incipit principio*. This decoration is done in a repetitive floral pattern, apparently rinceaux, which is combined with two additional branches, one at the top of the text and one at the bottom, both starting with griffins, half lion and half bird. [Mémoire Vive Besançon.](https://memoirevive.besancon.fr/ark:/48565/89v21z4370ns)


## The revision of the transcriptions

During the correct-a-thon, we compared the transcription produced by the model against an edition of the [Vulgate](https://www.sacred-texts.com/bib/vul/gen001.htm) of Genesis available online. On the one hand, we noticed that the model was able to identify correctly most of the words, and that the most abundant abbreviations were ꝺ́s (deus), ꝙ (quod), eſt (est), ꝰ (us), fcm̄ (facem), eēt (esset), t́rā (terram), qꝫ (que):

<br>
<p>
<img src="/assets/PBP_MS5_Visuel.png" style="zoom:100%;" />
<br>
Fig. 3. Genesis transcription wordcloud of the most common abbreviations
  </p>
<br>
<br>

On the other hand, the model often mistook the clusters in which an “r” was present for an “n” like in the word “ariꝺā” transcribed as “inda” or “mrēm” as “inrēm” or even “tigris” taken as “tigns”. Additionally, we observed an inversion in the order of “i” and “u”, like in “aꝺuitoꝛiuꝫ” being “aꝺiutoꝛiuꝫ” in the transcription.

In the line of difficulties related to abbreviations, two words showed up for which the symbol was absent from the Transkribus virtual keyboard, but was found in the extended version provided by the Expert Client installation: ẜm (secundum) and ẜpens (serpens), the long s with an extra line in the middle. ẜ is not a very frequent abbreviation, but is a significant one, it seemed to us, because of its appearance in the word referencing the representation of evil.

Regarding the generation of text regions, our team encountered a major problem, because the text region for the second column of every page overlapped the first, hence the software was unable to process them. That is the reason why we focus our efforts on revising the first columns of pages 9 and 10, achieving in this way the amount of text required for the correct-a-thon. Also, this inconvenience draws attention to  the importance of double-checking each of the stages in this kind of workflow.

<br>
<p>
<img src="/assets/PBP_MS5_Trkb.png" style="zoom:100%;" />
<br>
Fig. 4. Transkribus Expert Client
  </p>
<br>
<br>

Regarding other issues related to the use of Transkribus, learning to use the Expert Client version expanded our range of action, such as editing text regions, using the export button that allows creating txt, pdf, or xml in TEI format files, function that increases interoperability; as well as extending the above-mentioned virtual keyboard.


## Analytical Observations

An analysis of the text of the manuscript with that of the editions of the Vulgate reveals that the  significant role that abbreviations and special letter forms play in the manuscript text. Many of the medieval Latin abbreviations can be found in our manuscript (Ms. Besançon 5).

<br>
<p>
<img src="/assets/PBP_MS5_Page_9.png" style="zoom:100%;" />
<br>
Fig. 5. Genesis first column page 9
  </p>
<br>
<br>

| Transcription      | Vulgate Bible |
| ----------- | ----------- |
| Expliciunt capitula libri geneſis Incipit pꝛincipio creauit liber geneſis. ꝺeus celū et t́rā. T́ra aut̄ erat inanis ⁊ ua- cua. et tenebꝛe erant ſuꝑ faciē ābyſſi; et ſic̄ ꝺei fėbat˜ ſuꝑ aq˜s. Dixitqꝫ ꝺ́s. Fiat lux. Et ftā eſt lux. Et uiꝺit ꝺ́s lucem ꝙ eēt bōa; et ꝺiuiſit lucē a tenebꝛis. Appella uitqꝫ lucē ꝺiem; et tenebꝛas noctē. Fcm̄ qꝫ ē ueſꝑe et mane; ꝺies unꝰ. Dix̄ quoqꝫ ꝺ́s.| In principio creavit Deus cælum et terram. 2 Terra autem erat inanis et vacua, et tenebræ erant super faciem abyssi: et spiritus Dei ferebatur super aquas. 3 Dixitque Deus: Fiat lux. Et facta est lux. 4 Et vidit Deus lucem quod esset bona: et divisit lucem a tenebris. 5 Appellavitque lucem Diem, et tenebras Noctem: factumque est vespere et mane, dies unus. 6 Dixit quoque Deus.|


## Conclusions

Being part of this project to develop a HTR model of for abbreviated medieval Latin has made us realize how difficult it is to create and improve a model. Such an international collaborative project gave us an opportunity to have hands-on practice to work with Transkribus and on the other hand, to understand how the scribes used to interact in the context of the manuscript tradition, and about how the preservation and diffusion of knowledge have been important preoccupations across centuries.

Finally, practicing with an AI related software was the opportunity to begin a path of learning and exploring of a completely new dimension of possibilities regarding the textual analysis in various forms that we might encounter in the future. 


## Team
Kateri Soulard, Sonaj Kailas, David Macchi. 

## Suggested Citation
Soulard, Kateri; Kailas, Sonaj; Macchi, David. (19 May 2023). PBP Correct-a-thon Besançon: Besançon Ms 5.  *Paris Bible Project.*



