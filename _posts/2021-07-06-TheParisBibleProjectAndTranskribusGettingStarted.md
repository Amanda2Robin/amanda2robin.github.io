---
layout: post
title: "The Paris Bible Project and Transkribus: Getting Started"
subtitle: Each post also has a subtitle
gh-repo: daattali/beautiful-jekyll
tags: [PBP]
comments: false
---

# **The Paris Bible Project and Transkribus: Getting Started**

## **Using Transkribus in the Paris Bible Project**

<br>

The Paris Bible Project began with experiments into the machine transcription of some folios of a Paris Bible held in a local collection, that of the Louvre Abu Dhabi (LAD 2013.051). From these initial forays into handwritten text recognition (HTR) using high quality digitization and the clear hand of this single Latin Bible beginning with a public model in [Transkribus](https://readcoop.eu/transkribus/) available for Gothic manuscripts (Hodel), we have significantly expanded our thinking about the Paris Bible genre using AI-based transcription. We have included many other manuscripts held in collections around the world and we have also trained, and retrained, our own models to produce higher quality results. 

<br>

If you have not had the opportunity to take a look at the progress made in text recognition in various European (and non-European) languages of both printed and handwritten materials using neural methods with the Transkribus platform, it is worth a glance. In the words of the READ-COOP team, Transkribus is "a comprehensive platform for the digitisation, AI-powered text recognition, transcription and searching of historical documents – from any place, any time, and in any language”. It originated at the University of Innsbruck as part of a EU-funded research project READ and has grown into a European Cooperative Society (SCE), with individual and institutional [members](https://readcoop.eu/members/) worldwide. (Disclosure: one of the PBP project directors is a READ COOP SCE member). Most of the features of model training, layout analysis, and manual transcription are free; however, to carry out text recognition, Transkribus operates as a platform as service model, with nominal per-page costs.

<br>

Past and present initiatives of Transkribus include a wide variety of textual research. There are models for many languages, including projects in Arabic (Fawzi, Pastor, Martínez-Hinarejos, 2017), Finnish/Swedish (National Library of Finland, 2021), and Slovak (Katuščák, 2020). The scholarly literature based on the use of Transkribus is correspondingly wide, and has not yet, at the time of writing this post, been published in a critical bibliography. Handwritten or typographic styles can be so different from document to document, yet HTR as practiced by many in the world, and not only with Transkribus, promises to be able to combine different styles into singular "generic" models with the careful training of a multilingual community of scholars. In the case of PBP, we began with a model trained to work on Gothic hands in both German and Latin, and we have trained it to work with certain features of the Latin scripts which interest us most. 

<br>

## **Our Starting point**

<br>

How did our project start in Transkribus ? First, we began with uploading manuscript scans into a collection onto the platform (you can also use IIIF manifests if they are available and the version of the API is the same). Transkribus works well with high-quality pictures (around 2000x pixels) but it can give good results also with lower resolutions, as long as the picture is sufficiently zoomable. A future of working with bad, lower resolution scans is also probably not far off (Dietrich, 2021). 

<br>

We did not experience a significant difference between colour and black and white (usually microfilm digitization) pictures. The next step was to divide the manuscript images into text regions and lines, so the model will understand where to find the text to be transcribed. This can be done easily through the platform’s own tool, CITLab Advance, or manually by adding text regions (i.e. where the text is present) and then moving to the layout analysis, which finds the lines of the text. The new tool P2PaLA can be used to create a model for the recognition of text regions, although we have not yet used it for the PBP.

<br>

Then, the training can start. If a model for your language (in our case Latin) is already prepared, you can begin with that one as a base model to "boost" performance. We began with a transcription using Hodel's Gothic_Book_Scripts_XIII-XV_M4 model producing admittedly a flawed text, but avoiding having to manually transcribe all the text. Such a first transcription may require a lot of work of script correction, depending on the type of research to conduct. Generally, after 20-40 pages of corrected script (“Ground Truth”), you can retrain the model and apply it to the rest of the manuscript and already see improvements in the transcription. It is truly amazing to notice how the machine “reads” the manuscript even without a great amount of pages corrected. We noticed that certain features of interest to us, such as special letter forms, the insular "ꝺ", the long "ſ" and the rotund "ꝛ", were read very well from the very first try. 

<br>

Working with the LAD 2013.051, we created ground truth (human verified transcriptions) for 24 of folios, resulting in our first model. We corrected the results of the HTR and retrained, resulting in a reduction of character error rate. The third model was created by adding more textual data. The process is summarized in the table below: 

<br>

| Name of Model | Number of Lines/Words | CER (Training Set) | CER (Validation Set) |
| ------------- | --------------------- | ------------------ | -------------------- |
| LAD 1.1       | 1592/9632             | 11.89%             | 7.20%                |
| LAD 1.2       | 1592/9632             | 0.62%              | 4.14%                |
| LAD 1.3       | 2516/15258            | 0.51%              | 3.01%                |

<br>

Thus, after around forty pages corrected for our first manuscript, the Bible preserved at the Louvre Abu Dhabi, the LAD 1.3 model was already able to provide a good transcription of the text. We then applied this model to other manuscripts sourced from libraries around the world that provide a digitized version of Parisian Bibles. After trying our model on three of them, we found very interesting results with promising perspectives once the model will improve. As we expand our work, we hope to make the models public to Transkribus users as well. 

**Niccolò Acram Cappelletto, David Joseph Wrisley, and Estelle Guéville**

<br>



**Useful Links:**


https://parisbible.github.io/datasets/

https://parisbible.github.io/participate/

https://readcoop.eu/transkribus/?sc=Transkribus 

How to Use Transkribus in 10 Steps: https://readcoop.eu/transkribus/howto/use-transkribus-in-10-steps/

<br>

### **Further videos:**


- Transkribus Tutorials: https://www.youtube.com/watch?v=ezx79GxVoCI&list=PL7UbQtd4qlhIMP1KfdjGW3C-KXTxw4KYb
- *Transkribus Webinar* by Annemieke Romein: https://www.youtube.com/watch?v=5YCfaFNMol4&t=6342s
- *Transkribus Webinar 2 - Advanced Use* by Annemieke Romein: https://www.youtube.com/watch?v=yxLyzRZaff8&t=5458s
- *Transkribus Webinar 3 - Pylaia and Updated* by Annemieke Romein: https://www.youtube.com/watch?v=axYRvhgcVF4 

<br>

### **Scholarly articles on Transkribus:**


- Bazzaco, S. (2018). El Progetto Mambrino y las tecnologías OCR: Estado de la cuestión = Mambrino Project and OCR technologies: state of the art. *Historias Fingidas*, *6*. 257–272.[ https://doi.org/10.13136/2284-2667/89](https://doi.org/10.13136/2284-2667/89)
- Bazzaco, S. (2020). El reconocimiento automático de textos en letra gótica del Siglo de Oro: Creación de un modelo HTR basado en libros de caballerías del siglo XVI en la plataforma Transkribus. *Janus: estudios sobre el Siglo de Oro*, 9. 534–561.
- Dietrich, F. (2021). Can AI Save Bad Scans? READ COOP Insights Blog. https://readcoop.eu/insights/can-ai-save-bad-scans/. 
- Fawzi, A., Pastor, M., Martínez-Hinarejos, C.D. (2017). ‘Baseline Detection on Arabic Handwritten Documents’, in Proceedings of the ACM Symposium on Document Engineering. 193–6.
- Katuščák, D. (2020). DIGITAL HUMANITIES A AUTOMATICKÁ TRANSKRIPCIA RUKOPISNÝCH TEXTOV. (Slovak). *ITlib: Informacne Technologie a Kniznice*, *1*, 6–16.
- Muehlberger, G., Seaward, L., Terras, M., Ares Oliveira, S., Bosch, V., Bryan, M., Colutto, S., Déjean, H., Diem, M., Fiel, S., Gatos, B., Greinoecker, A., Grüning, T., Hackl, G., Haukkovaara, V., Heyer, G., Hirvonen, L., Hodel, T., Jokinen, M., … Zagoris, K. (2019). Transforming scholarship in the archives through handwritten text recognition: Transkribus as a case study. *Journal of Documentation*, 75(5). 954–976.[ https://doi.org/10.1108/JD-07-2018-0114](https://doi.org/10.1108/JD-07-2018-0114)
- Schlagdenhauffen, R. (2020). Optical Recognition Assisted Transcription with Transkribus: The Experiment concerning Eugène Wilhelm’s Personal Diary (1885-1951). *Journal of Data Mining & Digital Humanities*, *Atelier Digit_Hum*.[ https://jdmdh.episciences.org/6736/pdf](https://jdmdh.episciences.org/6736/pdf)
- Ventresque, V., Sforzini, A., & Massot, M.-L. (2019). Transcribing Foucault’s handwriting with Transkribus. *Journal of Data Mining & Digital Humanities*, *Atelier Digit_Hum*.[ https://jdmdh.episciences.org/5218/pdf](https://jdmdh.episciences.org/5218/pdf)
  Vukcevic, M. M. (2020). Turns of the centuries. The Transkribus automated tool for recognition, transcription and translation of handwritten historical documents A German-Serbian case study. *BABEL-REVUE INTERNATIONALE DE LA TRADUCTION-INTERNATIONAL JOURNAL OF TRANSLATION*, *66*(2), 294–310.[ https://doi.org/10.1075/babel.00159.vuk](https://doi.org/10.1075/babel.00159.vuk)

<br>

**Further readings**: https://readcoop.eu/publications/


<br>
<br>

## **Suggested citation:**

Cappelletto, Niccolò Acram, Wrisley, David Joseph, Guéville, Estelle. (07 July 2021). The Paris Bible Project and Transkribus: Getting started. *Paris Bible Project.*
