# Automatic Concept Map Creation - Approach Validation

This project was created by the research group of the Federal Technological University of Paraná - Cornélio Procópio Campus.

Before you start, you need to understand a bit of the context in which this experiment was conducted. Our main goal is to support secondary studies, such as Systematic Literature Reviews (SLR) and Systematic Mappings (SM). This type of study has been increasingly used in Software Engineering (SE) since they allow the identification of available evidence related to a research topic. One of the main activities of the process of conducting a secondary study is the primary studies selection, which involves, at first, the reading of the abstracts of the candidate studies. However, the growing number of scientific publications, coupled with the poor quality of their abstracts, it makes this activity increasingly difficult for researchers. Some solutions have been proposed to mitigate the problem, among them, the use of structured abstracts and graphic summaries. Previous studies have proposed guidelines for the construction of graphic summaries. However, these summaries continue to be created manually.

In this repository, you will find the replication kit used to evaluate our approach to automatically build graphic abstracts using NLP techniques. In the next sections, we describe the experimental setup used to evaluate if the concept maps created automatically are similar to those created manually. In addition, we also evaluated the efficiency of the classifier used in our approach using machine learning techniques and this data is available too.


# 1. Classifier evaluation

In this folder, we provide the assets necessary to perform the classifier training:

- **Raw Corpus (compressed)**: contains more than 200 abstracts in txt files and manually tagged by our team.
- **Corpus parsed**: Software engineering corpus already parsed in arff format.
- **Models previously trained**: J48, Random Forest and Naive Bayes trained in Weka
- **Config Files**: Configurations for training a model in weka. 

To audit these results you must download weka and import these data for explorer and use the configurations. The arff data was generated by a feature of our tool placed in:
https://github.com/csm-applications/CSM-CMtoolkit


# 2. Survey

In this folder, you will find:
- Forms used to survey the participants
- Excel spreadsheet containing the results collected

This experiment was conducted in UTFPR in 2017 and its participants were graduate students. We surveyed the participants regarding the quality of concept maps generated and the concept maps created by humans. Finally, we compared the results to verify if there are significant differences between them. The results indicate that no significant statistical differences were found and the maps generated by our approach can create comprehensible concept maps.

