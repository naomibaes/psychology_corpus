# Information Sheet

## Title: Academic psychology corpus (1930-2019)

**Description:** This repository contains the psychology corpus, which contains 871,340 abstracts from 875 psychology journals, with a total of 144,366,128 words ranging from 1930 to 2019, sourced from E-Research and PubMed databases (Vylomova et al., 2019). The journals are relatively evenly distributed across subdisciplines of psychology, including journals from overlapping Scimago journal classifications: developmental and educational psychology (24.7%), clinical psychology (19.5%), social psychology (18.1%), psychology (miscellaneous) (17.8%), applied psychology (16.5%), experimental and cognitive psychology (11.3%), and neuropsychology and physiological psychology (5.1%). 

## Data Collection Methodology
* See Vylomova, E., Murphy, S., & Haslam, N. (2019, August). Evaluation of semantic change of harm-related concepts in psychology. In Proceedings of the 1st international workshop on computational approaches to historical language change (pp. 29-34). https://aclanthology.org/W19-4704/

## Data Structure
- **Format:** csv (but it is actually separated by a unique delimiter: IIIII and should be read in as such)
- **Columns:** `[text ||||| year ||||| new_journal ||||| old_journal]`
  - Example: `...those taking a high or low position in the consensus ratings. The judges showed higher variability in rating their own sex than when rating the opposite sex. ||||| 1933 ||||| The Journal of Social Psychology ||||| Journal of Social Psychology`
- **Schema**:
  - `text`: article abstracts
  - `year`: year of publication
  - `new_journal`: new normalized journal name
  - `old_journal`: origial journal name
    
## Data Volume 
- *Note*: Information is for "/data/projects/punim0322/Processed/abstract_year_journal.csv"
- **Size:** 951 MB (998,130,585 bytes)

- **Year range:** 1930-2019
- **Abstracts:** 871,340
  - (cat abstract_year_journal.csv | grep -P '\\|\\| (19[7-9][0-9]|200[0-9]|201[0-7]) ' | wc -l gives 825628)
- **Journals:** 875 psychology journals
- **Tokens (1970-2019):** 142157449
- **Lines (1970-2019):** 859704
 
*Note:* For more information, download the "corpus_statistics.xlsx" file which contains descriptives for processed versions of the corpus and counts for psychology journals. You can email me (naomi_baes@hotmail.com) if you are after processed versions of the corpus in the excel spreadsheet (e.g., dependency parsed or lemmatized versions). The processed files are too large to drop into this repository.
- scp baesn@spartan.hpc.unimelb.edu.au:/data/projects/punim0322/Processed/abstract_year_journal.csv "C:\Users\naomi\OneDrive\Desktop"   

## Usage and Licensing

- **Permissions**: You are permitted to download and use this corpus of article abstracts. The use of abstracts circumvent paywall and copyright issues.

## Data Quality and Limitations

- **Quality Control**: Articles have been cleaned to remove duplicates and incomplete entries.
- **Known Limitations**: As full-text articles are not available, tokens are limited, affecting the comprehensiveness of the dataset. However, abstracts also provide a sort of standardized summary (without length bias) of the full-text article.

# Data Statement

### Purpose:
This data statement provides a comprehensive overview of the New York Times Article Corpus, which has been compiled for research and analysis purposes. The corpus aims to facilitate studies in various fields, including but not limited to, journalism, data science, natural language processing, and historical research.

### Scope:
- **Content**: Abstracts from scientific articles from 1930 to 2019 for each year.

![image](https://github.com/user-attachments/assets/57031fad-082f-4040-9187-80255a3b17d6)

### Methodology:
- Data was collected from E-Research and PubMed databases.

### Usage:
- **Research and Analysis**: This corpus can be used for text analysis, trend identification, and other research purposes.
- **Development**: Can be utilized in developing machine learning models and natural language processing applications.

### Quality and Limitations:
- **Quality Control**:
  - The dataset has undergone cleaning to remove duplicates and some non-English journals.

### Ethical Considerations:
- No major ethical considerations come to mind.

### Acknowledgements: 
- Sean Murphy, an alumni postdoc in Nick Haslam's concept creep lab constructed the corpus with help from the team at the University of Melbourne's Research Computing Services.
  
### Contact Information:
- **Email**: [naomi_baes@hotmail.com](mailto:naomi_baes@hotmail.com). You can contact with questions.

### Citation:
Please cite the first paper introducing this corpus as follows:  `Vylomova, E., Murphy, S., & Haslam, N. (2019, August). Evaluation of semantic change of harm-related concepts in psychology. In Proceedings of the 1st international workshop on computational approaches to historical language change (pp. 29-34). https://aclanthology.org/W19-4704/`

# Applications of the Corpus

The corpus has been used in the following papers. You may find processing scripts in associated repositories or email the first author when this is not the case to share them.

[1] Vylomova, E., Murphy, S., & Haslam, N. (2019, August). Evaluation of semantic change of harm-related concepts in psychology. In Proceedings of the 1st international workshop on computational approaches to historical language change (pp. 29-34). https://aclanthology.org/W19-4704/

[2] Haslam, N., Dakin, B. C., Fabiano, F., McGrath, M. J., Rhee, J., Vylomova, E., ... & Wheeler, M. A. (2020). Harm inflation: Making sense of concept creep. European Review of Social Psychology, 31(1), 254-286. https://psycnet.apa.org/record/2020-55134-001

[3] Ekaterina Vylomova & Nick Haslam. 2021. Semantic changes in harm-related concepts in English. In Nina Tahmasebi, Lars Borin, Adam Jatowt, Yang Xu & Simon Hengchen (eds.), Computational approaches to semantic change, 93–121. Berlin: Language Science Press. DOI: 10.5281/zenodo.5040304

[4] Haslam, N., Vylomova, E., Zyphur, M., & Kashima, Y. (2021). The cultural dynamics of concept creep. American Psychologist, 76(6), 1013. https://doi.org/10.1037/amp0000847

[5] Wheeler, M.A., Vylomova, E., McGrath, M.J. et al. More confident, less formal: stylistic changes in academic psychology writing from 1970 to 2016. Scientometrics 126, 9603–9612 (2021). https://doi.org/10.1007/s11192-021-04166-9

[6] Haslam N, Vylomova E, Murphy SC, Wilson SJ. The Neuroscientification of Psychology: The Rising Prevalence of Neuroscientific Concepts in Psychology From 1965 to 2016. Perspect Psychol Sci. 2022 Mar;17(2):519-529. [doi: 10.1177/1745691621991864. Epub 2021 Jul 20. PMID: 34283670.](https://journals.sagepub.com/doi/10.1177/1745691621991864)

[7] Baes, N., Vylomova, E., Zyphur, M., & Haslam, N. (2023). The semantic inflation of “trauma” in psychology. Psychology of Language and Communication, 27(1), 23-45. https://doi.org/10.58734/plc-2023-0002

[8] Xiao, Y., Baes, N., Vylomova, E., & Haslam, N. (2023). Have the concepts of ‘anxiety’and ‘depression’been normalized or pathologized? A corpus study of historical semantic change. Plos one, 18(6), e0288027. https://doi.org/10.1371/journal.pone.0288027

[9] Naomi Baes, Nick Haslam, and Ekaterina Vylomova. 2023. Semantic Shifts in Mental Health-Related Concepts. In Proceedings of the 4th Workshop on Computational Approaches to Historical Language Change, pages 119–128, Singapore. Association for Computational Linguistics. https://aclanthology.org/2023.lchange-1.13/

[10] Naomi Baes, Nick Haslam, and Ekaterina Vylomova. 2024. A Multidimensional Framework for Evaluating Lexical Semantic Change with Social Science Applications. In Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), pages 1390–1415, Bangkok, Thailand. Association for Computational Linguistics. https://aclanthology.org/2024.acl-long.76/

[11] Baes, N., Merx, R., Haslam, N., Vylomova, E., & Dubossarsky, H. (2025). A General Framework to Evaluate Methods for Assessing Dimensions of Lexical Semantic Change Using LLM-Generated Synthetic Data. arXiv preprint arXiv:2503.08042. https://arxiv.org/abs/2503.08042
