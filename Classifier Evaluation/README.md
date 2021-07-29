# To replicate the tests follow the steps below:

- First, you must have Java installed and configured. 
Chekout a brief tutorial here: https://www.computersciencemaster.com.br/configurando-o-ambiente-java/

Next, you must:

- Step 1: Download and install Weka (3.8.5). Access link: https://waikato.github.io/weka-wiki/downloading_weka/
- Step 2: Open weka Explorer
- Step 3: In "Pre-process" tab click in "open file", locate the data.arff file and click "open".
- Step 4: After loading the dataset, remove the attribute "Title" from dataset
- Step 5: Click on "classify" tab and choose the algorithm which you want to use and change the parameters.
- Step 6: Click on start and checkou the results.

--- 

Weka contains many classifiers implemented and ready to use. However, there is many parameters to be adjusted and it may become a little bit hard to setup everything. Therefore, to facilitate this process we provide in folder "configs" a file to automatically setup Weka classifier.

To load this files:
- Step 1: in Classify tab, click on text box where algorithm selected appears.
- Step 2: in the pop up window click on "open".
- Step 3: select the config file and click ok
- Step 4: run training and evaluation

So far, we provide configs for:

- j48
- Naive Bayes Multinomial
- Random Forest
- Decision stump
- Hoeffding tree
- REPtree

---

Most recent (29/07/2021) results for these classifiers:

TL;DR: 

j48 → Acuracy: 83% 
Naive Bayes Multinomial → Acuracy: 84% 
Random Forest → Acuracy: 79% 
Decision stump → Acuracy: 86% 
Hoeffding tree → Acuracy: 72% 
REPtree → Acuracy: 85%  

## J48 Classifier

```plaintext

=== Stratified cross-validation ===
=== Summary ===

Correctly Classified Instances         417               83.7349 %
Incorrectly Classified Instances        81               16.2651 %
Kappa statistic                          0.5752
Mean absolute error                      0.2219
Root mean squared error                  0.3805
Relative absolute error                 54.1588 %
Root relative squared error             84.0907 %
Total Number of Instances              498     

=== Detailed Accuracy By Class ===

                 TP Rate  FP Rate  Precision  Recall   F-Measure  MCC      ROC Area  PRC Area  Class
                 0,608    0,070    0,777      0,608    0,682      0,583    0,748     0,599     Quantitative
                 0,930    0,392    0,855      0,930    0,891      0,583    0,748     0,826     Qualitative
Weighted Avg.    0,837    0,299    0,832      0,837    0,831      0,583    0,748     0,760     

=== Confusion Matrix ===

   a   b   <-- classified as
  87  56 |   a = Quantitative
  25 330 |   b = Qualitative

```

## Random Forest Classifier

```plaintext

=== Stratified cross-validation ===
=== Summary ===

Correctly Classified Instances         419               84.1365 %
Incorrectly Classified Instances        79               15.8635 %
Kappa statistic                          0.5581
Mean absolute error                      0.279 
Root mean squared error                  0.3481
Relative absolute error                 68.0846 %
Root relative squared error             76.9412 %
Total Number of Instances              498     

=== Detailed Accuracy By Class ===

                 TP Rate  FP Rate  Precision  Recall   F-Measure  MCC      ROC Area  PRC Area  Class
                 0,517    0,028    0,881      0,517    0,652      0,591    0,895     0,817     Quantitative
                 0,972    0,483    0,833      0,972    0,897      0,591    0,895     0,938     Qualitative
Weighted Avg.    0,841    0,352    0,847      0,841    0,827      0,591    0,895     0,903     

=== Confusion Matrix ===

   a   b   <-- classified as
  74  69 |   a = Quantitative
  10 345 |   b = Qualitative


```



## Naive Bayes Multinomial Classifier



```plaintext
=== Stratified cross-validation ===
=== Summary ===

Correctly Classified Instances         395               79.3173 %
Incorrectly Classified Instances       103               20.6827 %
Kappa statistic                          0.4155
Mean absolute error                      0.2732
Root mean squared error                  0.3828
Relative absolute error                 66.6691 %
Root relative squared error             84.6062 %
Total Number of Instances              498     

=== Detailed Accuracy By Class ===

                 TP Rate  FP Rate  Precision  Recall   F-Measure  MCC      ROC Area  PRC Area  Class
                 0,413    0,054    0,756      0,413    0,534      0,447    0,825     0,669     Quantitative
                 0,946    0,587    0,800      0,946    0,867      0,447    0,825     0,914     Qualitative
Weighted Avg.    0,793    0,434    0,787      0,793    0,771      0,447    0,825     0,843     

=== Confusion Matrix ===

   a   b   <-- classified as
  59  84 |   a = Quantitative
  19 336 |   b = Qualitative
```

## Decision Stump Classifier

```Plaintext

=== Stratified cross-validation ===
=== Summary ===

Correctly Classified Instances         430               86.3454 %
Incorrectly Classified Instances        68               13.6546 %
Kappa statistic                          0.6344
Mean absolute error                      0.236 
Root mean squared error                  0.3439
Relative absolute error                 57.5897 %
Root relative squared error             75.9997 %
Total Number of Instances              498     

=== Detailed Accuracy By Class ===

                 TP Rate  FP Rate  Precision  Recall   F-Measure  MCC      ROC Area  PRC Area  Class
                 0,615    0,037    0,871      0,615    0,721      0,651    0,759     0,652     Quantitative
                 0,963    0,385    0,861      0,963    0,910      0,651    0,759     0,837     Qualitative
Weighted Avg.    0,863    0,285    0,864      0,863    0,856      0,651    0,759     0,784     

=== Confusion Matrix ===

   a   b   <-- classified as
  88  55 |   a = Quantitative
  13 342 |   b = Qualitative

```

## Hoeffding tree Classifier

```plaintext

=== Stratified cross-validation ===
=== Summary ===

Correctly Classified Instances         362               72.6908 %
Incorrectly Classified Instances       136               27.3092 %
Kappa statistic                          0.0738
Mean absolute error                      0.389 
Root mean squared error                  0.4437
Relative absolute error                 94.9129 %
Root relative squared error             98.0637 %
Total Number of Instances              498     

=== Detailed Accuracy By Class ===

                 TP Rate  FP Rate  Precision  Recall   F-Measure  MCC      ROC Area  PRC Area  Class
                 0,056    0,003    0,889      0,056    0,105      0,180    0,543     0,335     Quantitative
                 0,997    0,944    0,724      0,997    0,839      0,180    0,543     0,740     Qualitative
Weighted Avg.    0,727    0,674    0,771      0,727    0,628      0,180    0,543     0,624     

=== Confusion Matrix ===

   a   b   <-- classified as
   8 135 |   a = Quantitative
   1 354 |   b = Qualitative

```

## REPtree classifier

```plaintext

=== Stratified cross-validation ===
=== Summary ===

Correctly Classified Instances         427               85.743  %
Incorrectly Classified Instances        71               14.257  %
Kappa statistic                          0.626 
Mean absolute error                      0.2298
Root mean squared error                  0.3493
Relative absolute error                 56.0692 %
Root relative squared error             77.2018 %
Total Number of Instances              498     

=== Detailed Accuracy By Class ===

                 TP Rate  FP Rate  Precision  Recall   F-Measure  MCC      ROC Area  PRC Area  Class
                 0,636    0,054    0,827      0,636    0,719      0,636    0,781     0,666     Quantitative
                 0,946    0,364    0,866      0,946    0,904      0,636    0,781     0,851     Qualitative
Weighted Avg.    0,857    0,275    0,855      0,857    0,851      0,636    0,781     0,798     

=== Confusion Matrix ===

   a   b   <-- classified as
  91  52 |   a = Quantitative
  19 336 |   b = Qualitative

```
