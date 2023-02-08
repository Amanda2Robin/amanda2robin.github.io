---
layout: page
title: Research and Data
permalink: /datasets/
---
<base target="_blank">

# Bibliography

The bibliography of the project is available on [Zotero](https://www.zotero.org/groups/2466765/paris_bible_project/library).



# Models

- **5** models trained in Transkribus
- Public models are stored in Transkribus.

| Model_name | Date_trained | Base_model              | Number_epochs | Number_GT_pages | Train_set | Validation_set | Number_lines | Number_words | CER (training set) | CR (validation set) | Comments                                                     |
| ---------- | ------------ | ----------------------- | ------------- | --------------- | --------- | -------------- | ------------ | ------------ | ------------------ | ------------------- | ------------------------------------------------------------ |
| LAD 1.0    | 15/08/2020   | Gothic Books (Hodel)    | 50            | 8               | 7         | 1              | 588          | 3547         | 0.27%              | 4.52%               | Based only on the LAD manuscript (LAD 2013.051).  Bias towards Genesis, Exodus, Mark and Matthew |
| LAD 1.1    | 22/08/2020   | LAD bible 1.0           | 50            | 24              | 19        | 5              | 1592         | 9632         | 11.89%             | 7.20%               | Based only on the LAD manuscript (LAD 2013.051).  Same GT as 1.2 with a different base model |
| LAD 1.2    | 22/08/2020   | Charter Scripts (Hodel) | 50            | 24              | 19        | 5              | 1592         | 9632         | 0.62%              | 4.14%               | Based only on the LAD manuscript (LAD 2013.051).  Same GT as 1.1 with a different base model |
| LAD 1.3    | 26/10/2020   | Gothic Books (Hodel)    | 100           | 39              | 30        | 9              | 2516         | 15258        | 0.51%              | 3.01%               | Based only on the LAD manuscript (LAD 2013.051).             |
| PBP 1.0    | 29/06/2021   | LAD bible 1.3           | 50            | 25              | 16        | 9              | 152          | 8840         | 2.04%              | 12.76%              | Composite model based on Paris Bibles from around Europe in the 13th and 14th centuries. |
| PBP 2.0    | Upcoming     |                         |               |                 |           |                |              |              |                    |                     |                                                              |



# Manuscripts

- **More than 320** manuscripts from **76** institutions in **14** countries
- The list of manuscripts and their metadata are downloadable on [Github](https://github.com/parisbible/mss).

[View where the manuscripts are kept today!](https://view-awesome-table.com/-NAecAbDIDjxCaxCO2Mb/view)



# Transcriptions

- **186** pages of ground truth
- Ground truth is available and downloadable on [Github](https://github.com/parisbible/ground_truth).



<br>

*Last update: 05/02/2023*