# Mathematical Reasoning Test Score Prediction
EFFECT OF ADDING OMITTED VARIABLES IN MEDIATION AND MODERATION ANALYSES: A CASE STUDY

Mediation and moderation analyses have been widely implemented in social sciences. Both techniques use regression analysis for modeling; consequently, these are subjected to assumptions of linearity, normality, constant variance, and independence of errors. When these assumptions are violated, models generate distorted results on the magnitude of effects and the causal relationships. To remediate the appearing inconsistencies, a common practice is the inclusion of variables that exert specific effects given their nature. In this project, a case study is analyzed based on the work developed by Mukuka et al. (2021), where we explore the results of adding moderators to their model. In this work, we compare the robustness and assumptions fulfillment from the original model with our proposed model. Results show that the second model increases the coefficient of determination by approximately 43.96% and decreases Root Mean Square Error (RMSE) and Mean Absolute Error (MAE) by 7.9 and 6.12 units, respectively. In addition, all regression analysis assumptions are met.

## Problem Definition
This work is based on a case study from a quasi-experiment developed by Mukuka et al. (2021), where six public secondary schools from Zambia were analyzed; three were randomly allocated to the experimental group while the other three were allocated to the control group. Students assigned to the control group were taught using an expository instructional approach based on daily lectures and question-and-answer techniques. 

Meanwhile, those assigned to the experimental group were taught using the Student Teams-Achievement Division (STAD) model of cooperative learning, based on students working cooperatively in heterogeneous groups. They are faced with contextualized problems and hands-on activities, and at the end of each topic, a quiz is given to them in which they were not allowed to help one another. In the end, the group with the highest average or that attained the desired performance level earned an award or recognition.

The students’ scores from this study were collected after six weeks of exposure to the different learning methods. Three main results confirm these: Mathematical Reasoning Test (MRT), mathematical reasoning dimensions adequacy (conjecturing, justifying, and mathematizing), and self-efficacy beliefs. 

Firstly, the MRT was a test given to the students prior and posterior to the experiment based on two class topics: quadratic equations and quadratic functions. The MRT posterior to the experiment consisted of 16 test items organized under seven questions. Three mathematical reasoning dimensions conformed these 16 items: conjecturing, justifying, and mathematizing. 

Finally, the students were given a questionnaire prior and posterior to the experiment to measure their mathematics self-efficacy and task-specific self-efficacy beliefs. These scores were based on how often students felt confident to succeed in various aspects of mathematical learning and how confident they were in answering each of the mathematical reasoning questions on quadratic equations and functions, respectively. The student's results can be found on the MR Dataset.sav (available on http://dx.doi.org/10.17632/3472zggczv.1). Demographic variables such as a respondent’s identity, gender, school type, and age have equally been specified in the dataset. 

By making use of this dataset, Mukuka et al. (2021) developed an analysis based on a “Parallel Multiple Mediation Model” where an independent variable, (*group*), was modeled as influencing the dependent variable (*posttest*), both directly and indirectly through two mediators, (*post_efficacy*) and (*post_specific*). Parameters were obtained using the PROCESS custom dialogue version 3.4 embedded in SPPS, resulting in the regression coefficients shown in the figure below. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/90649106/184549225-1032be6b-0a84-40a7-b093-8787d630a635.png">
</p>

Further results in their mediation analysis are summarized in the next Table. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/90649106/184549344-ba3687d7-6351-4600-89e5-bbbc1e16ee07.png">
</p>

It is noticeable that its coefficient of determination $R^2$, is barely over 40% which means that the predictor variables do not reduce the uncertainty on predicting the posttest scores. In addition, K-fold cross-validation was performed, where the results confirm that this model has low coefficient stability and a low ability to generalize inferences. Additionally, its Root Mean Square Error (RMSE) conveys that, in general, the model’s prediction of the posttest score is 16.09 points off. Similarly, its Mean Absolute Error showed that, on average, the forecast of this model has a 12.84 point difference from its actual value.

Also, we analyzed the satisfiability of the Multiple Linear Regression assumptions: linearity, errors' independence, homoscedasticity, and normality. These were tested graphically on the model (see Table below), and it is visible that the homoscedasticity assumption is not met, which leads to the conclusion that this model has a high risk of generating distortion in the interpretation of results and weakening the overall statistical power of the analysis. In other words, the results of this model have an increased possibility of Type I error and inconsistent F-test results, leading to erroneous conclusions (Aguinis et al., 1999; Osborne & Waters, 2002). 

<p align="center">
  <img src="https://user-images.githubusercontent.com/90649106/184549462-1b52111c-15cf-44a4-aaaf-d0a58c32fc49.png">
</p>

Furthermore, there is a lack of error independence, leading to an underestimation of standard errors and the labeling variables as statistically significant when not (Keith, 2006). To correct these unsatisfiability of assumptions and attain higher predictability on the results of students' posttest scores, a new model has to be developed. 

## Methodology
For the new model development, we considered that Mukuka et al. (2021) excluded some important post-experiment scores. These correspond to the adequacy of the student's mathematical reasoning dimensions (conjecturing, justifying, and mathematizing). These variables are considered post-treatment moderating variables because they are consequences of the treatment and directly affect the dependent variable (Koschate-Fischer & Schwille, 2018). 

In experimental studies, the omission of a mediator-response confounding factor variable likely leads to an inadequate estimation of the indirect effect (Fritz et al., 2016). Therefore, adding these omitted variables into the model is necessary to avoid this issue. Moreover, the Table below shows a high linear association between these moderating variables and the dependent variable, indicating that they are necessary for the model.

<p align="center">
  <img src="https://user-images.githubusercontent.com/90649106/184549464-00dfe801-5802-4e2a-ad54-304ae8b3dc7e.png">
</p>

## Results
Parameters for the modified model ( $Y=X+M_1+M_2+W_1+W_2+W_3$ ) were obtained, resulting in the regression coefficients shown in the Figure below.

<p align="center">
  <img src="https://user-images.githubusercontent.com/90649106/184549704-71acfb27-43b6-42c2-9b7b-ffb936773b53.png">
</p>

Comparison of the original model and the one developed in this work appears in the next table. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/90649106/184549757-6ec2662e-b2ca-4fdd-ad15-164a6dca9af6.png">
</p>

In this work, it is visible that the coefficient of determination $R^2$ increased significantly in the modified model. This situation means that by adding the moderating variables, the total variability of the posttest scores that is explained by the regression model corresponds to 84.8%.

Additionally, the robustness of the regression is tested by performing K-fold cross-validation. The results conveyed a higher coefficient of determination $R^2$ of 84.80% compared to the original model of 40.84%. Also, the RMSE and MAE resulted in lower values from the original model (see Table below).

<p align="center">
  <img src="https://user-images.githubusercontent.com/90649106/184549825-136c8cf5-4e5e-4c25-a920-ab9695e52000.png">
</p>

Finally, the multiple linear regression model assumptions were tested and compared to the original model. Table below shows that by adding the Mathematical Reasoning Dimensions into the model, the assumptions of homoscedasticity and independence of error are met. This result leads us to conclude that the modified model has significantly lower distortions on the findings, higher stability in the results, and a higher ability to predict posttest scores.

<p align="center">
  <img src="https://user-images.githubusercontent.com/90649106/184549873-44df3f58-c31c-4efb-8ff0-137214e1e307.png">
</p>

## Discussion
The analysis undertaken through the assumptions’ testing showed that the original model developed by Mukuka et al. (2021) has some critical inconsistencies since the model does not meet the homoscedasticity and independent error assumptions nor has a trustworthy ability to predict posttest scores. 
Through these findings, the initial mediation analysis was modified so that the Mathematical Reasoning Dimensions are included in the model, which implied new findings regarding the study:

- Enhancing conjecturing, justifying, and mathematizing skills in students is the most influential factor that affects their mathematical reasoning abilities.
- When the assumptions are met, there is higher stability in the predicted results.
- The modified model has a higher coefficient of determination and prediction while decreasing RMSE and MAE. Hence, it has a higher ability to predict posttest scores.

It is essential to mention that even though posttest scores seem highly affected by the Mathematical Reasoning Dimensions, they are not directly related. According to a study developed by Mukuka et al. (2020a), even if the students had correctly answered a question, most of them were not able to justify their answers neither by deductive nor inductive reasoning. Inductive reasoning was based on citing numerical values to expressions or giving examples of numbers that can satisfy a given expression, and deductive reasoning was based on logical deductions to arrive at a valid generalization of a given algebraic statement or argument (Mukuka et al., 2020a). For example, in question number 4, 79% of the students answered correctly, yet only 14% of those properly justified their answer. The other 86% had misconceptions about the topic or did not correctly reference the statement (Mukuka et al., 2020a). These results mean that although a student may have a higher test score, it does not necessarily mean that they have correctly developed the conjecturing, justifying, and mathematizing skills.

## Conclusion
The initial mediation analysis was modified so that the students’ Mathematical Reasoning Dimensions adequacy (*conjecturing*, *justifying*, and *mathematising*) were included as variables that directly influence the post-test score. The findings of this study revealed that the inclusion of such factors increases $R^2$ while decreasing MAE and MSE; which means that teachers must focus in improving students’ conjecturing, justifying, and mathematising skills while applying the STAD model of cooperative learning. With this students will have a better probability of attaining a higher score in the final test.
